# Rascunho — Skills Client-Side e Pasta rascunhos-staging

**Data:** 2026-06-15
**Sessão de origem:** Experimento — design de acesso fluido ao ecossistema via pasta de projeto Claude
**Status:** rascunho de staging — aguarda processamento em W04
**Ideias relacionadas na Seção C:**
- Skills client-side / Skills portáteis (2026-06-15)
- Pasta rascunhos-staging no hub-entrada (2026-06-15)

---

## 1. Contexto da sessão

Esta sessão foi um experimento de abertura de chat dentro da pasta de projeto do Claude,
sem token, para explorar o que é possível fazer nesse modo de acesso. A partir do
experimento, emergiram dois conceitos novos para o ecossistema.

---

## 2. Conceito: Skills Client-Side

### Problema identificado

O ecossistema tem skills e workflows canônicos (server-side). Para usar uma skill no
dia a dia — ex: registrar uma ata de reunião — o usuário precisa abrir uma sessão W06
completa, com token, protocolo de abertura, leitura de contexto. Isso tem fricção alta
para operações rotineiras e rápidas.

### Solução proposta

Cada workflow do ecossistema pode ter uma **versão instalável** (client-side), projetada
para ser copiada na ferramenta do usuário (Claude, neste caso). Essa versão:

- Sabe onde buscar o padrão canônico no ecossistema via API
- Tem o padrão embutido como fallback para operação sem token
- Verifica automaticamente se houve atualização de versão e alerta o usuário
- Opera em três modos:
  - **Modo 1 — Sem token (fallback):** usa padrão local embutido, alerta sobre possível desatualização
  - **Modo 2 — Token leitura:** busca padrão atualizado, compara versões, alerta se divergente
  - **Modo 3 — Token escrita:** deposita o produto no ecossistema após aprovação

### Terminologia aprovada

| Termo | Definição |
|---|---|
| **Client-side** | Versão instalável da skill, vive na ferramenta do usuário |
| **Server-side** | Versão canônica da skill, vive no ecossistema (GitHub) |

### Princípio de design central

A skill client-side **não é uma cópia estática** do padrão canônico. É um
**acionador inteligente com endereço** — ela sabe onde buscar a verdade, verifica
se mudou, e opera com o melhor padrão disponível no momento. O fallback local
existe para garantir disponibilidade, não para substituir a fonte de verdade.

Isso aplica o princípio "conhecimento como query, não materialização" ao contexto
das ferramentas do usuário.

### Modelo de repositório

**Opção B aprovada:** repositório dedicado que agrega todas as versões instaláveis
em um único endereço. O usuário vai lá, encontra todas as skills client-side
disponíveis, escolhe as que precisa, instala no seu ambiente Claude.

Impactos a resolver em W04:
- Novo tipo na taxonomia do ecossistema? Ou subpasta de repositório existente?
- Nomenclatura do repositório dedicado
- Como o S01 (skl-criador-de-skills) incorpora a criação de versões client-side
- Documentação do processo de instalação para futuros usuários

### Protótipo construído nesta sessão

Skill client-side de registro de reunião — baseada na S06 (`skl-registro-reuniao` v1.0),
com os três modos de operação implementados. Arquivo: `SKILL-registro-reuniao-local.md`.
Disponível para download no chat desta sessão.

---

## 3. Conceito: Pasta rascunhos-staging

### Problema identificado

Ideias que chegam ao staging frequentemente são produto de sessões longas de
amadurecimento — às vezes uma hora ou mais de conversa, produzindo documentos MD
com análise detalhada, comparações, decisões de design. Ao registrar na tabela
da Seção C, esse material é comprimido em uma linha. Os elementos elaborados
se perdem.

Não havia local adequado para esses documentos aguardarem junto com a ideia.

### Solução proposta

Nova pasta `hub-entrada/rascunhos-staging/` como repositório temporário para
documentos MD de amadurecimento de ideias em staging.

**Princípios de design:**
- Entrada sem atrito — não é obrigatório ter rascunho para registrar ideia
- A tabela da Seção C ganha coluna `Rascunho` com valor `—` ou nome do arquivo
- Nomenclatura dos arquivos: `AAAA-MM-DD-[slug-da-ideia].md`
- Ciclo de vida: rascunho migra para destino definitivo quando ideia é aprovada em W04;
  permanece como registro histórico se arquivada

**Impactos a resolver em W04:**
- Alteração estrutural da tabela Seção C (nova coluna)
- Atualização do rito do agente ao registrar ideias (S04, possivelmente W04)
- Política de limpeza da pasta (rascunhos de ideias arquivadas ficam? por quanto tempo?)

### Por que hub-entrada?

O `hub-entrada` já agrega staging, roadmap e decisões — é a camada de governança
de ideias do ecossistema. Rascunhos de amadurecimento pertencem a essa camada,
não ao `hub-memoria` (que é histórico de sessões operacionais).

---

## 4. Conexão entre os dois conceitos

Ambos emergiram do mesmo problema raiz: **o ecossistema tem boa infraestrutura
para execução formal, mas alta fricção para operações rápidas e para preservação
de material em amadurecimento**. As soluções são complementares:

- Skills client-side reduzem fricção de acesso no uso diário
- rascunhos-staging preservam o material produzido nos momentos de amadurecimento

Juntos, fecham o ciclo: ideias nascem em sessões ricas → material é preservado em
rascunhos-staging → ideias são processadas em W04 → skills client-side tornam
os workflows aprovados acessíveis no dia a dia.

---

## 5. Próximos passos (para W04)

1. Decidir taxonomia e nomenclatura do repositório de skills client-side
2. Alterar estrutura da tabela Seção C (nova coluna Rascunho)
3. Atualizar rito do agente para verificar e depositar rascunho ao registrar ideia
4. Definir política de limpeza da pasta rascunhos-staging
5. Avaliar se S01 precisa de atualização para contemplar criação de versões client-side
