# Roadmap — DTD/SETIS/SES-DF

**Última atualização:** 2026-06-24
**Versão do ecossistema:** sumario v3.17 | S04 v2.10 | W05 v1.3 | W06 v1.4

> O histórico completo de fases concluídas está em
> [ROADMAP-HISTORICO.md](./ROADMAP-HISTORICO.md).

---

## Sobre este documento

O ROADMAP concentra o horizonte de trabalho ativo do ecossistema ATLAS —
o que está em execução, o que vem a seguir e o que está amadurecendo.
Não é um diário de bordo (papel do CHANGELOG) nem um arquivo histórico
(papel do ROADMAP-HISTORICO). É um instrumento de navegação.

**Estrutura de camadas:**

| Camada | Significado |
|---|---|
| 🎯 Próxima ação | Missão definida — execução na próxima sessão |
| 🔄 Em andamento | Iniciado, aguardando condição externa ou continuação |
| 📅 Médio prazo | Aprovado, sem bloqueio técnico, aguarda priorização |
| 🌱 Maturando | Ideia validada, ainda sem forma de execução definida |
| 🔭 Longo prazo | Visão — sem prazo ou dependência não resolvida |

**Coluna Área:** tipos do ecossistema ATLAS —
`S` Skill · `W` Workflow · `D` Documento · `M` Material ·
`A` Agenda · `P` Projeto · `ALL` ecossistema inteiro

---

## 📊 Painel de Progresso

```
ATLAS — DTD/SETIS/SES-DF · Jun/2026

FASES CONCLUÍDAS ──────────────────────────────────────────── ATIVO

  F1          F2          F3          F4          F5
FUNDAÇÃO  INSTRUMENTOS  DOCUMENTAL  PROCESSOS  GOVERNANÇA
  ████        ████        ████        ████        ████

  F6          F7          F8          F9         F10
PROTOCOLO  ROADMAPPING   CICLO      DOUTRINA    ATLAS
 SESSÃO      W04        CANÔNICO    ACESSO     NOMEADO
  ████        ████        ████        ████        ████

────────────────────────────────────────────────────────────────
  AGORA  →  Frente 3 (source-only) · Frente 4 (núcleo/instância)
  HORIZONTE →  wiki-ecossistema · W07 · bloco-para-agentes
────────────────────────────────────────────────────────────────
  Repositórios: ~22     Tipos: S W D M A P
  Docs D01: 29          Capítulos D03: 4     Skills: 7
```

---

## 🎯 Próxima ação imediata

- **Frente 3 — Migração source-only:** remover coluna Versão do `sumario.md`
  (decisão aprovada em W04 sessão 2 — execução pendente)
- **Frente 4 — Inventário núcleo/instância ATLAS:** mapear o que é portável
  vs. específico-DTD (urgência estratégica — segunda instância iminente)

---

## 🔄 Em andamento

- **P01 `prj-telessaude-poc-prisional`** — PoC aguardando definição de unidade
  piloto (12 deliberações pendentes — ver README do P01)
- **D01 upload pendente** — transcrição dos documentos restantes
  (itens 10–17 do §9 do WORKFLOW-ESPECIFICACAO.md)

---

## 📅 Médio prazo

### Execução técnica

| Item | Área | Registrado | Depende de |
|---|---|---|---|
| Formalizar bloco-para-agentes nos READMEs de todos os repositórios | ALL | 2026-06-15 | — |
| Atualizar W03/WORKFLOW.md — handoff com diagnóstico causal (C8) | W | 2026-06-15 | — |
| Atualizar W04/WORKFLOW.md — princípio staging (C9) e critério curadoria (C10) | W | 2026-06-15 | — |
| Atualizar W06/WORKFLOW.md — ergonomia de fechamento (C5) e declaração de token (C6) | W | 2026-06-15 | — |
| Atualizar S04 — delay 3s pós-PUT formalizado na Etapa 5 (C3) | S | 2026-06-15 | — |
| Adotar timestamp ISO 8601 completo em entradas novas de backlog/changelog | ALL | 2026-06-15 | — |
| Reorganizar `backlog-versoes.md` do M01 — 910+ linhas, numeração duplicada | M | 2026-06-11 | — |
| Depositar Seção 8 + Lição 6 no cap-02 do hub-aprendizagem (E1 redigido) | D | 2026-06-15 | — |
| Redigir 4 definições formais no GLOSSARIO.md: PTD/PTD-SES, SGTD, CIG/SES, Fórum de Subsecretários | M | 2026-06-15 | — |
| Renomear `backlog-versoes.md` → `historico-versoes.md` em todos os repositórios (~20 repos) | ALL | 2026-06-24 | Sessão W04 dedicada |

### Decisões de design

| Item | Área | Registrado | Depende de |
|---|---|---|---|
| Reclassificação W03 e fronteira skill↔workflow — pode resultar em renomear `wkf-registro-sessao` → `skl-registro-sessao` | W · S | 2026-06-11 | Sessão dedicada |
| DECISOES.md — registro formal da rejeição da proposta atlas-hub mirror | M | 2026-06-15 | — |

### Novos repositórios e instrumentos

| Item | Área | Registrado | Depende de |
|---|---|---|---|
| Criar `wiki-ecossistema` — camada de hipertexto navegável; arquitetura 3 camadas (C1/C2/C3) | D | 2026-06-07 | Sessão de design |
| Criar `wkf-resumo-executivo` (W07) — Resumo Executivo para SETIS e Secretário | W | 2026-06-11 | — |
| Criar `wkf-iac-conformidade` (W08) — análise de conformidade documental automatizada | W | 2026-06-11 | D01 completo |
| Criar `pdtic-historico` — versionamento histórico do PDTIC com IACs | D | 2026-06-11 | — |
| Evoluir S05 para fase sequencial autônoma | S | 2026-06-11 | PASSOU ≥ 95% em ≥ 10 docs |
| Integração SEI via API | S | 2026-06-11 | API disponível |

---

## 🌱 Maturando

| Item | Área | Registrado | Aguardando |
|---|---|---|---|
| ATLAS-moldura — tese de generalização núcleo/instância; registrar no DECISOES.md | ALL | 2026-06-15 | Sessão dedicada |
| Disciplina de Arquitetura do Conhecimento — ancorada sob ATLAS; exercida via IS/RD 🧪 | ALL | 2026-06-15 | Sessão evolutiva própria |
| Memória de domínio do briefing — primeira categoria de conteúdo; lar a definir | D · S | 2026-06-11 | Decisão de arquitetura |
| Processo de curadoria longitudinal do hub-aprendizagem — periodicidade trimestral/semestral | D | 2026-06-11 | Sessão dedicada |
| Campos autor/revisor nas entradas de backlog/changelog | ALL | 2026-06-11 | Primeiro colaborador externo |
| Perfis de acesso formais ao ecossistema | ALL | 2026-06-11 | Colaborador externo |
| Família de workflows derivados do W04 por projeto | W · P | 2026-06-11 | Projeto ativo |
| Contribuição externa via issues | ALL | 2026-06-11 | Perfis de acesso formais |

---

## 🔭 Longo prazo

| Item | Área | Registrado |
|---|---|---|
| GitHub MCP — operações autenticadas sem PAT manual | S | 2026-06-08 |
| Migração de PAT clássico para fine-grained com escopos mínimos | ALL | 2026-06-08 |
| Replicação do modelo ATLAS para outras unidades da SES-DF | ALL | 2026-06-11 |
| Case institucional documentado para publicação | D | 2026-06-11 |

---

> **Legenda de curadoria:** 🔒 interno · 📊 estratégico · 🌐 público
> *(itens sem símbolo = curadoria pendente)*
