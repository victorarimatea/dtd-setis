# Staging Area — DTD/SETIS/SES-DF

**Repositório:** hub-entrada
**Mantenedor:** victorarimatea
**Alimentado por:** S04 `skl-github-orquestracao` (registros automáticos) e qualquer sessão Claude (ideias)
**Processado por:** W04 `wkf-roadmap-geral` — sessões de sexta-feira à tarde

> Este arquivo NÃO contém informações oficiais do ROADMAP.
> Tudo aqui aguarda processamento e decisão do mantenedor.
> Nenhum item é deletado — itens processados vão para a Seção D.

---

## Seção A — Registros automáticos (S04)

*Entregáveis implementados no ecossistema aguardando curadoria no ROADMAP.*
*Alimentado pela S04 ao final de cada operação.*

| Data | Entregável | Tipo | Repositório | Depositado por |
|---|---|---|---|---|
| 2026-06-04 | S04 v2.2 — Verificação 5-A: reconciliação obrigatória com ROADMAP | Atualização de skill | skl-github-orquestracao | S04 |
| 2026-06-04 | W03 v1.1 — Etapa 2-A: reconciliação com ROADMAP antes do relatório | Atualização de workflow | wkf-registro-sessao | S04 |
| 2026-06-04 | W04 wkf-roadmap-geral v1.0 — criação do workflow de gestão de roadmap | Criação de workflow | wkf-roadmap-geral | S04 |
| 2026-06-04 | staging.md — criação da staging area do ecossistema | Novo artefato | hub-entrada | S04 |

---

## Seção B — Ideias sinalizadas

*Ideias capturadas por sinalização explícita do mantenedor durante sessões.*
*Formato: o mantenedor diz "registra isso como ideia" e o Claude deposita aqui.*

| Data | Hora | Autor | Ideia | Contexto de origem | Status |
|---|---|---|---|---|---|
| — | — | — | — | — | — |

---

## Seção C — Ideias mineradas (aguardam validação)

### Por que esta seção existe

Boas ideias raramente chegam com aviso prévio. Elas surgem nas interlinhas
de uma conversa técnica, num comentário lateral durante uma implementação,
numa frase que começa com "seria interessante se..." no meio de uma sessão
sobre outra coisa. Se nenhum mecanismo as captura naquele momento, elas se
perdem nos textos de dezenas de conversas ao longo do tempo.

Esta seção existe para que isso não aconteça. O agente de IA — operando como
minerador ativo de contexto — varre o histórico de cada sessão em busca de
manifestações que têm características de ideia embrionária. Ele não espera
que o mantenedor lembre de sinalizar. Ele busca, apresenta os candidatos,
aguarda validação, e só então elabora e registra formalmente.

O resultado é um pipeline de inovação contínuo, de baixa fricção, que amplia
o escopo de resgate de ideias e quase inviabiliza que boas propostas sejam
desperdiçadas por falta de um lugar adequado para pousarem.

---

### Instrução para agentes de IA — mineração ativa de contexto

**Quando executar:** ao final de qualquer sessão que resulte em plano de ação
de edição de repositórios ou documentações — ou seja, toda sessão que aciona
a S04. A mineração ocorre antes do depósito final, ainda com o contexto
completo da conversa disponível.

**O que fazer, passo a passo:**

**Passo 1 — Varredura do histórico**
Releia o histórico completo da conversa que gerou o plano de ação atual.
Não apenas as decisões formais — leia também os comentários laterais,
as frases exploratórias, os problemas identificados ao longo do caminho.
O objetivo é encontrar manifestações que não foram tratadas como decisão
mas que têm potencial estratégico.

**Passo 2 — Aplicação dos critérios de elegibilidade**
Para cada trecho candidato, aplique as perguntas orientadoras abaixo.
Um candidato é elegível se responder afirmativamente a pelo menos duas:

| # | Pergunta orientadora | Sinal típico no texto |
|---|---|---|
| 1 | O mantenedor identificou um problema recorrente ou uma lacuna no ecossistema? | *"ainda não temos..."*, *"falta um..."*, *"o problema é que..."* |
| 2 | O mantenedor expressou uma hipótese sobre algo que poderia existir? | *"seria interessante se..."*, *"imagino que..."*, *"poderia ser..."* |
| 3 | O mantenedor fez uma comparação com uma referência externa? | *"como fazem em..."*, *"seria como um..."*, *"semelhante ao..."* |
| 4 | O mantenedor formulou uma pergunta estratégica sem respondê-la? | *"e se..."*, *"por que não..."*, *"o que aconteceria se..."* |
| 5 | O mantenedor expressou um desejo ou intenção não convertida em ação? | *"quero pensar mais sobre..."*, *"no futuro..."*, *"seria bom ter..."* |
| 6 | O mantenedor nomeou algo que não existe ainda mas que faria sentido existir? | Substantivo novo seguido de descrição funcional |
| 7 | O Claude identificou uma implicação estratégica não explorada na conversa? | Conexão entre dois pontos que o mantenedor não conectou explicitamente |

**Passo 3 — Apresentação dos candidatos**
Para cada candidato elegível, apresente ao mantenedor antes de registrar:

```
💡 Ideia candidata identificada:
"[trecho ou paráfrase do que foi dito]"

Pergunta orientadora ativada: [número e texto da pergunta]
Contexto: [em que momento da conversa surgiu]

Você gostaria de registrar isso como ideia na staging area?
```

Aguarde confirmação. Não registre sem aprovação explícita do mantenedor.

**Passo 4 — Elaboração para registro**
Após confirmação, elabore a ideia no formato de registro abaixo antes de
depositar na tabela. A elaboração deve:
- Dar um nome descritivo à ideia (não apenas repetir a frase original)
- Contextualizar o problema que ela resolve
- Indicar a qual área do ecossistema se relaciona
- Manter linguagem objetiva, sem superestimar nem subestimar o potencial

**Passo 5 — Depósito na tabela**
Registre na tabela abaixo com todos os campos preenchidos.

> **Nota sobre automação:** a mineração ativa como instrução formal na S04
> será implementada após 3 execuções do wkf-roadmap-geral, para calibrar
> os critérios de elegibilidade com base em casos reais antes de automatizar.
> Por ora, o agente executa os passos acima ao identificar oportunidade,
> ainda que sem instrução explícita da S04.

---

### Tabela de ideias mineradas

| Data | Conversa de origem | Ideia candidata | Pergunta orientadora ativada | Validada pelo mantenedor | Aguardando desde |
|---|---|---|---|---|---|
| 2026-06-04 | Sessão de criação do W04 | `wkf-resumo-executivo` — workflow dedicado para estruturar, aprovar e distribuir o Resumo Executivo para SETIS e Secretário de Saúde; define linguagem executiva, critérios de aprovação e processo de distribuição | #6 — nomeação de algo que não existe mas faria sentido existir | ✅ confirmado | 2026-06-04 |
| 2026-06-04 | Sessão de criação do W04 | Estrutura formal de perfis de acesso do ecossistema — define quem pode visualizar, editar e criar em cada repositório; base para governança multiusuário quando a DTD crescer | #1 — lacuna identificada pelo mantenedor: *"não parei para sequer pensar em uma estrutura de perfil de acesso"* | ✅ confirmado | 2026-06-04 |

---

## Seção D — Arquivo histórico

*Ideias e registros já processados em sessões do W04.*
*Nunca deletados — o histórico de decisões tem valor institucional.*

| Data entrada | Data decisão | Item | Decisão | Motivo | Sessão |
|---|---|---|---|---|---|
| — | — | — | — | — | — |

---

### Legenda de status (Seções B e C)

| Status | Significado |
|---|---|
| `pendente` | Aguarda próxima sessão do W04 |
| `maturando` | Foi avaliada, tem potencial, precisa de mais reflexão |
| `aprovada` | Migrou para o ROADMAP confirmado |
| `arquivada` | Avaliada e não avança no momento — ver Seção D |
| `rejeitada` | Avaliada e descartada — ver Seção D |

### Política de limpeza

Após cada sessão do W04, toda a Seção A é processada e esvaziada.
Seções B e C: itens com decisão migram para a Seção D.
Itens com status `maturando` permanecem nas seções originais.
**Nenhum item é deletado — apenas movido.**
