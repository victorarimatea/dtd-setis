# Arquitetura do Ecossistema DTD/SETIS/SES-DF

**Versão:** v2.0 — 2026-06-02
**Repositório:** dtd-setis
**Mantenedor:** victorarimatea

> Este documento descreve a arquitetura atual do ecossistema de automação
> e governança documental da Diretoria de Transformação Digital (DTD/SETIS/SES-DF).
> Atualizar sempre que um novo tipo de repositório for criado ou a arquitetura
> for alterada significativamente.

---

## Visão geral

O ecossistema é composto por repositórios GitHub organizados em 6 tipos formais,
uma skill de orquestração (S04) que garante consistência, e um repositório de
portfólio público que serve como porta de entrada.

```
┌─────────────────────────────────────────────────────────────────┐
│                    dtd-setis (Portfólio público)                │
│         Porta de entrada — README, ROADMAP, CHANGELOG           │
└────────────────────────────┬────────────────────────────────────┘
                             │
        ┌────────────────────┼────────────────────┐
        │                   │                    │
        ▼                   ▼                    ▼
┌──────────────┐   ┌──────────────────┐   ┌─────────────────┐
│  Matrizes(M) │   │   Skills (S)     │   │  Documentos (D) │
│              │   │                  │   │                 │
│ M01 ecossist-│   │ S01 criador-de-  │   │ D01 governanca- │
│ ema-sumario  │   │     skills       │   │     ses-df      │
│ M02 saude-   │   │ S02 iac-pdtic    │   │ D02 doc-cadas-  │
│ digital-tax. │   │ S03 poc-saude    │   │     tro-ses-dtd │
│              │   │ S04 github-orch* │   │                 │
│              │   │ S05 transcricao  │   │                 │
│              │   │ S06 reg-reuniao  │   │                 │
└──────────────┘   └──────────────────┘   └─────────────────┘
        │
        ├──────────────────────────────────────────────────────┐
        │                                                      │
        ▼                   ▼                    ▼             ▼
┌──────────────┐   ┌──────────────────┐   ┌──────────────┐
│ Workflows(W) │   │   Agendas (A)    │   │ Projetos (P) │
│              │   │                  │   │              │
│ W01 transcr- │   │ A01 agenda-dtd   │   │ P01 telessau-│
│     icao-doc │   │ (privado)        │   │     de-poc-  │
│ W02 registro-│   │                  │   │     prisional│
│     reuniao  │   │                  │   │ (privado)    │
│ (privado)    │   │                  │   │              │
└──────────────┘   └──────────────────┘   └──────────────┘

* S04 skill-github-orquestracao: orquestra operações em todos os tipos
```

---

## Os 6 tipos de repositório

### Tipo M — Matrizes de conhecimento

Repositórios que contêm o conhecimento estrutural do ecossistema.
São fontes de verdade consultadas por skills e pelo Claude antes de qualquer ação.

| Característica | Valor |
|---|---|
| Prefixo de nome | livre (sem prefixo) |
| Visibilidade padrão | Público |
| Arquivo principal | `sumario.md` (M01) / `taxonomia.md` (M02) |
| Arquivo obrigatório | `backlog-versoes.md`, `README.md`, `INDICE.md` |
| Exemplos | `ecossistema-sumario` (M01), `saude-digital-taxonomia` (M02) |

### Tipo S — Skills

Repositórios com instruções técnicas estruturadas para o Claude (ou outra LLM)
executar tarefas específicas de forma padronizada e repetível.

| Característica | Valor |
|---|---|
| Prefixo de nome | `skill-` |
| Visibilidade padrão | Público |
| Arquivo principal | `SKILL.md` |
| Arquivo obrigatório | `backlog-versoes.md`, `README.md`, `INDICE.md` |
| Exemplos | `skill-github-orquestracao` (S04), `skill-registro-reuniao` (S06) |

### Tipo D — Documentos

Repositórios de armazenamento e versionamento de documentos institucionais
transcritos ou produzidos pela DTD.

| Característica | Valor |
|---|---|
| Prefixo de nome | livre (sem prefixo) |
| Visibilidade padrão | Público |
| Arquivo principal | varia por repositório |
| Arquivo obrigatório | `backlog-versoes.md`, `README.md`, `INDICE.md` |
| Exemplos | `governanca-ses-df` (D01) com 28 documentos transcritos |

### Tipo W — Workflows

Repositórios de memória organizacional de processos recorrentes da DTD.
Descrevem o processo do ponto de vista organizacional — por que existe, quem usa,
etapas humanas e automatizadas, histórico de problemas e roadmap de automação.
Distinto de skills: o workflow é anterior e superior à skill.

| Característica | Valor |
|---|---|
| Prefixo de nome | `workflow-` |
| Visibilidade padrão | Público (pode ser privado) |
| Arquivo principal | `WORKFLOW.md` (8 seções obrigatórias) |
| Arquivo obrigatório | `backlog-versoes.md`, `README.md`, `INDICE.md`, `execucoes/` |
| Exemplos | `workflow-transcricao-documental` (W01), `workflow-registro-reuniao` (W02) |

### Tipo A — Agendas

Repositórios de acervo cronológico de registros de reunião de uma unidade.
**Único tipo indexado por tempo de ocorrência** — não por ordem de criação.
A estrutura de pastas `reunioes/AAAA/MM/` e nomenclatura `AAAA-MM-DD-...`
garantem linha do tempo consultável.

| Característica | Valor |
|---|---|
| Prefixo de nome | `agenda-` |
| Visibilidade padrão | Privado |
| Arquivo principal | `INDICE.md` (índice cronológico) |
| Arquivo obrigatório | `backlog-versoes.md`, `README.md`, `INDICE.md`, `reunioes/AAAA/MM/` |
| Campos especiais | `data_reuniao` (ocorrência) + `data_registro` (inserção) |
| Exemplos | `agenda-dtd` (A01) |

### Tipo P — Projetos

Repositórios privados de memória institucional viva para projetos formais da DTD.
Acumulam atas, decisões, stakeholders, artefatos e log de workflows acionados.

| Característica | Valor |
|---|---|
| Prefixo de nome | livre (sem prefixo) |
| Visibilidade padrão | Privado |
| Arquivo principal | `README.md` com ficha técnica e deliberações pendentes |
| Arquivo obrigatório | `backlog-versoes.md`, `stakeholders.md`, `EXECUCOES.md`, `reunioes/`, `documentos/` |
| Exemplos | `telessaude-poc-prisional` (P01) |

---

## Camadas de operação

```
Camada 4 — Portfólio público
  dtd-setis: vitrine institucional, ROADMAP, CHANGELOG

Camada 3 — Conhecimento estrutural
  M01 ecossistema-sumario: sumário, nomenclatura, glossário, CONTEXTO
  M02 saude-digital-taxonomia: taxonomia de saúde digital

Camada 2 — Instrumentos operacionais
  Skills (S): instruções técnicas para IA
  Workflows (W): memória organizacional de processos
  Agendas (A): acervo cronológico de reuniões

Camada 1 — Conteúdo institucional
  Documentos (D): documentos transcritos e produzidos
  Projetos (P): projetos formais com memória viva
```

---

## Relações entre tipos

**W → S:** um workflow referencia a skill que automatiza suas etapas.
A skill não conhece o workflow — o workflow conhece a skill.

**A → P:** registros de reunião vivem no repositório A.
Quando associados a projeto, são referenciados em `P/EXECUCOES.md`.
O conteúdo não é duplicado — apenas referenciado.

**W → P (log de execução):** logs de execução de workflow vivem em `W/execucoes/`.
Quando associados a projeto, são referenciados em `P/EXECUCOES.md`.

**S04 → todos:** a skill de orquestração S04 garante consistência em todas
as operações que tocam qualquer repositório do ecossistema. Ela é acionada
automaticamente ao detectar operações no GitHub, após leitura do CONTEXTO.md.

---

## Skill de orquestração — S04

A `skill-github-orquestracao` (S04) é a guardiã de consistência do ecossistema.
Opera em 8 etapas separadas por aprovação explícita do mantenedor:

```
Etapa 0: Leitura do estado real (SHAs, versões atuais)
Etapa 1: Classificação da operação (OP-A a OP-AG)
Etapa 2: Mapeamento de impacto (todos os arquivos afetados)
Etapa 3: Construção do plano (tabela para aprovação)
Etapa 4: Solicitação do token (após aprovação)
Etapa 5: Execução (Python urllib — nunca curl/heredoc)
Etapa 6: Verificação pós-execução (5 verificações)
Etapa 7: Relatório de encerramento
```

Versão atual: v1.8 (em atualização nesta sessão)

---

## Repositório âncora e porta de entrada

**Repositório âncora:** `ecossistema-sumario` (M01)
Contém as fontes de verdade: `sumario.md`, `nomenclatura.md`, `GLOSSARIO.md`,
`CONTEXTO.md`. Todo Claude lê o CONTEXTO.md antes de qualquer ação.

**Porta de entrada:** `dtd-setis`
Repositório público com diagrama do ecossistema, tabela de repositórios,
links para skills disponíveis e instrução de inicialização para o Claude.

---

*Documento mantido pela DTD/SETIS/SES-DF.*
*Atualizar sempre que um novo tipo for criado ou a arquitetura evoluir.*
