# ROADMAP — Ecossistema DTD/SETIS

Planejamento das próximas entregas, em ordem de prioridade.
Atualizado em: 2026-05-28

---

## Legenda

| Símbolo | Status |
|---|---|
| ✅ | Concluído |
| 🔄 | Em andamento |
| 📋 | Planejado — próxima entrega |
| 🔮 | Planejado — médio prazo |
| 💡 | Ideia — a avaliar |

---

## Fase 1 — Fundação ✅

- ✅ Taxonomia de saúde digital (M02)
- ✅ Repositório âncora com sumário e nomenclatura (M01)
- ✅ Skill criadora de skills (S01)
- ✅ Skill IAC do PDTIC — modo IAC-V (S02 v1.0)
- ✅ Modelo IAC v0.1 — primeiro instrumento gerado
- ✅ Modelo IAC v0.2 — IAC-H adicionado, governança SES-DF incorporada
- ✅ Repositório mãe público como portfólio (este repositório)

---

## Fase 2 — Conhecimento institucional 📋

**Objetivo:** dotar o ecossistema de conhecimento normativo e institucional
permanente, reduzindo a necessidade de repassar contexto a cada sessão.

- ✅ Skill de elaboração de PoC em Saúde Digital (S03) — baseada na PoC MedNear,
  caso zero do Marco Regulatório Interno de PoCs da SES-DF; incorporada ao
  ecossistema em 2026-05-28

- 📋 Criar repositório `governanca-ses-df` (tipo D — público)
  - Portaria nº 193/2024 (CIG/SES, SGTD, Fórum de Subsecretários)
  - Portaria nº 718/2024 (CGTD/SEEC)
  - Decreto nº 48.503/2026 (PDTIC obrigatório)
  - PTD-SES 2024-2027
  - Base normativa de saúde digital (documento existente — migrar do Drive)
  - Matriz de competências: quem aprova o quê na SES-DF

- 📋 Atualizar `skill-iac-pdtic` → v2.1: consultar `governanca-ses-df` na Etapa 1

- 📋 Criar repositório `pdtic-historico` (tipo D — privado)
  - Uma pasta por versão aprovada do PDTIC
  - Cada pasta contém: documento + IAC correspondente

---

## Fase 3 — Expansão das skills 🔮

**Objetivo:** ampliar o ecossistema com skills que cubram outros processos
recorrentes da DTD/SETIS.

- 🔮 `skill-iac-generico` (S04) — IAC para qualquer par de documentos
  sem especialização temática; base para outras skills especializadas

- 🔮 `skill-briefing-semanal` (S05) — já existe como skill no projeto Claude;
  migrar para repositório GitHub dentro do padrão do ecossistema

- 🔮 `skill-monitoramento-ptd` (S06) — monitora execução das iniciativas
  do PTD-SES, cruza com prazos e gera relatório de status

- 🔮 Integração com GitHub MCP quando disponível nativamente no Claude
  (elimina necessidade de Personal Access Token para escrita)

---

## Fase 4 — Institucionalização 💡

**Objetivo:** transformar o ecossistema pessoal em recurso institucional
da SES-DF, com governança compartilhada.

- 💡 Proposta formal ao SGTD para adoção do modelo IAC como padrão
  permanente de governança documental do PDTIC e PTD

- 💡 Migração para organização GitHub da SES-DF (quando criada)

- 💡 Documentação do ecossistema como caso de uso de IA na gestão pública
  para compartilhamento com outras secretarias do GDF

- 💡 Expansão da equipe da DTD — onboarding facilitado pelo ecossistema:
  novos servidores leem o repositório mãe e já entendem como tudo funciona

---

## Próxima ação imediata

Criar o repositório `governanca-ses-df` com os instrumentos normativos
da SES-DF, começando pela Portaria nº 193/2024 e pelo PTD-SES 2024-2027
que já estão disponíveis.
