---
tipo: protocolo
id: PROTOCOLO-SESSAO
titulo: Ritos de sessão do ecossistema DTD/SETIS
versao: v1.0
data: 2026-06-13
mantenedor: victorarimatea
repositorio: hub-entrada
status: ativo
---

# PROTOCOLO-SESSAO.md — Ritos de sessão do ecossistema DTD/SETIS

> **O que é este arquivo.** É o lar canônico e versionado dos ritos de
> abertura, fechamento e leitura de sessão. As decisões que antes viviam
> dispersas na `staging.md` consolidam-se aqui como norma estável. Os blocos
> operacionais completos vivem neste arquivo; nos blocos de notas do celular
> bastam ponteiros de 3–4 linhas para cá.
>
> Este protocolo descreve *o que* fazer em cada modo de sessão. O **como**
> operacional — checklists, verificações, ordem de propagação — pertence à
> skill `skl-github-orquestracao` (S04), que este protocolo referencia mas
> não duplica.

---

## Princípio organizador — Ergonomia dos ritos

Eliminar atrito de transporte em processos recorrentes, nos dois lados da
fronteira: agente e humano. Todo artefato que cruza a fronteira
`chat → humano → chat` é entregue pronto para transporte de baixo atrito —
em **code fence copiável de um toque**, nunca como texto a ser selecionado
manualmente. É a contrapartida humana do que a leitura automática do handoff
(W06 v1.2) fez do lado do agente: ambos removem uma etapa manual frágil de um
rito que se repete todo dia.

---

## Doutrina de acesso — dois tokens

> Substitui e supera a antiga regra "API para operação / raw para leitura".
> O raw está **aposentado** como canal de sessão.

O ecossistema é lido e escrito **exclusivamente via GitHub Contents API**,
autenticada. O acesso é graduado por **dois tokens distintos**, segundo o
princípio de menor privilégio:

| Token | Escopo | Quando entra | Resolve |
|---|---|---|---|
| **Token de leitura ampla** | leitura (inclui repositórios privados) | na **abertura de toda sessão**, qualquer modo | alcança o handoff no hub-memoria (privado); 5000 req/h autenticadas; sem cache CDN |
| **Token de edição** | leitura + escrita | **só** quando a sessão converte para escrita (Modo 1) | habilita PUT; revogado ao fim da sessão |

**Por que dois tokens.** O handoff mora no `hub-memoria` (P02, privado);
`raw.githubusercontent.com` e a API não autenticada não leem repositório
privado — por isso a abertura "sem token" falhava de forma recorrente. A
leitura autenticada resolve isso de forma estrutural, eleva o teto de
60 → 5000 req/h e elimina o risco de SHA obsoleto por cache CDN. A edição
entra tarde, e sai cedo.

**Higiene.** O valor de qualquer token é carregado **pelo mantenedor**, na
hora da sessão. Nunca aparece em arquivo versionado (repositórios públicos
têm secret scanning que revoga segredos commitados) nem em blocos persistentes
— apenas o placeholder `[COLAR TOKEN ...]`. O token de edição é revogado em
`github.com/settings/tokens` ao fechar a sessão.

---

## Modo 1 — Sessão de Operação (escreve; token de edição)

1. **Leituras obrigatórias** (token de leitura ou de edição), via API:
   `hub-fonte/CONTEXTO.md`, `hub-fonte/sumario.md`,
   `skl-github-orquestracao/SKILL.md`.
2. **Absorção automática do handoff:** localizar o relatório `SESSAO-*` mais
   recente em `hub-memoria/documentos` (ordenação lexicográfica do nome) e ler
   seu Bloco III (Handoff). *Fallback:* falha na extração → auditoria W05 nova
   do zero; **nunca** cola manual (decisão de 2026-06-12 — fonte primária sobre
   estado derivado).
3. **Missão + regras operacionais.** Nenhuma escrita sem aprovação explícita do
   plano. SHA fresco imediatamente antes de cada PUT; CONFIRMAR (GET em chamada
   separada, ~3s) após cada PUT. Toda operação gera registro em backlog/changelog.
4. **Canal:** API Contents, autenticada (token de edição).

## Modo 2 — Fechamento (auditoria W05; sem token de edição)

- Execução exclusiva do W05, em **chat separado**, com **token de leitura**.
- **Regra absoluta:** o W05 só detecta e reporta — **nunca recebe token de
  edição**, nunca modifica arquivos. A separação executor/auditor é estrutural.
- O relatório de sessão (W03) inclui o **Bloco de Handoff** como seção final,
  depositado no `hub-memoria` após a auditoria confirmar convergência (zero
  SEV1/SEV2).
- **Canal:** API Contents (token de leitura).

## Modo 3 — Sessão de Leitura (token de leitura)

- **3a — leitura exploratória:** consulta sem escrita; pode **promover-se a
  operação** se surgir insight/correção a registrar (ver "Promoção de modo").
- **3b — demonstração read-only compartilhável:** apresentação do ecossistema
  a terceiros (chefia, colega, qualquer LLM com web), hub-entrada como anfitrião.
- **Canal:** API Contents (token de leitura). O raw permanece disponível apenas
  como recurso público externo de leitura tokenless de repositórios **públicos**
  (ex.: demonstração a um agente sem credencial) — fora do rito de sessão.

---

## Ergonomia de transporte — entrega de blocos no fechamento

No fechamento, o agente entrega, em code fence copiável:

1. **Pacote 2 — reauditoria W05:** instrução pronta para abrir o chat de
   auditoria independente (token de leitura).
2. **Bloco 1 — abertura da PRÓXIMA sessão de operação:** já contextualizado pela
   sessão que termina (missão provável + dívida prioritária do handoff),
   faltando apenas o token de edição.

O **bloco de leitura (Modo 3)** NÃO é entregue no fechamento — mora no bloco de
notas para uso pontual. Só o arco de operação é entregue, fechando a corrente
contínua entre sessões: handoff lido automaticamente (lado agente) + Pacote 2
copiável + Bloco 1 copiável (lado humano).

---

## Promoção de modo

**Leitura 3a → Operação (Modo 1):** quando, durante uma leitura, surge um
insight ou correção que merece registro. A promoção exige a introdução do
**token de edição** e a partir daí segue integralmente o rito do Modo 1
(plano, aprovação, SHA fresco, CONFIRMAR, registros).

---

## Intenção do Comandante deste protocolo

O estado final desejado é uma sessão sem atrito de transporte e sem ambiguidade
de acesso: abre-se com leitura ampla autenticada, escreve-se apenas sob token de
edição introduzido tarde e revogado cedo, e todo artefato que o humano precisa
mover entre chats chega pronto para um toque. Quando uma situação não estiver
coberta por este texto, decida pelo que **reduz atrito recorrente sem ampliar
privilégio nem expor segredo**.

---

*Mantido por victorarimatea — DTD/SETIS/SES-DF. Consolidação das ideias de
fluidez mineradas em 2026-06-11 e 2026-06-12 (staging Seção C). A doutrina de
acesso evoluiu, na sessão de 2026-06-13, da regra "API/raw" para o modelo de
dois tokens.*
