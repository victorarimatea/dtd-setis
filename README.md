```
▄█████╗ ████████╗██╗      █████╗ ███████╗
██╔══██╗╚══██╔══╝██║     ██╔══██╗██╔════╝
███████║   ██║   ██║     ███████║███████╗
██╔══██║   ██║   ██║     ██╔══██║╚════██║
██║  ██║   ██║   ███████╗██║  ██║███████║
╚═╝  ╚═╝   ╚═╝   ╚══════╝╚═╝  ╚═╝╚══════╝
```

**Automação e Governança do Conhecimento Institucional**
DTD/SETIS/SES-DF

**Versão:** v2.2 — 2026-06-23

> **Tecnologia pública a serviço da saúde das pessoas.**

Este repositório é a porta de entrada pública do ecossistema ATLAS —
uma metodologia de gestão do conhecimento institucional desenvolvida pela
Diretoria de Transformação Digital da Secretaria Executiva de Tecnologia
da Informação em Saúde (SETIS) da Secretaria de Estado de Saúde do
Distrito Federal (SES-DF).

---

## O que é o ATLAS

O ATLAS é uma metodologia de gestão do conhecimento estruturada em torno
de uma arquitetura de repositórios, matrizes de conhecimento, skills de
automação e workflows institucionais versionados e auditáveis.
A DTD/SETIS/SES-DF é a primeira instância do ecossistema ATLAS.

---

## O Ecossistema ATLAS
```
Camada 4 — Portfólio Institucional e Infraestrutura de Conhecimento
    hub-entrada: porta de entrada, ROADMAP, CHANGELOG, vitrine
    hub-aprendizagem: memória intelectual, boas práticas, benchmarks

Camada 3 — Conhecimento Estrutural (Matrizes M)
    M01 hub-fonte      M02 mat-saude-digital-taxonomia

Camada 2 — Instrumentos Operacionais (Skills S + Workflows W)
    S01 skl-criador-de-skills      S02 skl-iac-pdtic (privado)
    S03 skl-poc-saude-digital      S04 skl-github-orquestracao
    S05 skl-transcricao-documental S06 skl-registro-reuniao
    S07 skl-briefing-saude-digital
    W01 wkf-transcricao-documental
    W02 wkf-registro-reuniao (privado)
    W03 wkf-registro-sessao
    W04 wkf-roadmap-geral
    W05 wkf-auditoria-consistencia
    W06 wkf-sessao-agente

Camada 1 — Conteúdo Institucional (Documentos D + Agendas A + Projetos P)
    D01 doc-governanca-ses-df            D02 mat-cadastro-ses-setis-dtd
    D03 hub-aprendizagem
    A01 agd-dtd (privado)
    P01 prj-telessaude-poc-prisional (privado)
    P02 hub-memoria (privado)
```

---

## Repositórios do ecossistema

---

### Matrizes (M) — fontes de verdade estruturais

| ID | Repositório | Visibilidade | Descrição |
|---|---|---|---|
| M01 | [hub-fonte](https://github.com/victorarimatea/hub-fonte) | Público | Âncora do ecossistema: sumário, nomenclatura, glossário e contexto |
| M02 | [mat-saude-digital-taxonomia](https://github.com/victorarimatea/mat-saude-digital-taxonomia) | Público | Taxonomia estruturada de saúde digital |

### Skills (S) — agentes de automação especializados

| ID | Repositório | Visibilidade | Descrição |
|---|---|---|---|
| S01 | [skl-criador-de-skills](https://github.com/victorarimatea/skl-criador-de-skills) | Público | Cria novos repositórios de skill via API GitHub |
| S02 | skl-iac-pdtic | Privado | Gera IAC-V e IAC-H do PDTIC da SES-DF |
| S03 | [skl-poc-saude-digital](https://github.com/victorarimatea/skl-poc-saude-digital) | Público | Gera documentos de PoC em saúde digital no padrão SES-DF |
| S04 | [skl-github-orquestracao](https://github.com/victorarimatea/skl-github-orquestracao) | Público | Garante consistência do ecossistema a cada operação |
| S05 | [skl-transcricao-documental](https://github.com/victorarimatea/skl-transcricao-documental) | Público | Converte PDFs regulatórios em Markdown estruturado |
| S06 | [skl-registro-reuniao](https://github.com/victorarimatea/skl-registro-reuniao) | Público | Transforma resumos de reunião em registros institucionais para o SEI |
| S07 | [skl-briefing-saude-digital](https://github.com/victorarimatea/skl-briefing-saude-digital) | Público | Briefing periódico de saúde digital para o Diretor de Transformação Digital |

### Documentos (D) — conteúdo institucional estruturado

| ID | Repositório | Visibilidade | Descrição |
|---|---|---|---|
| D01 | [doc-governanca-ses-df](https://github.com/victorarimatea/doc-governanca-ses-df) | Público | 28 documentos transcritos: legislação, portarias, resoluções e referências internacionais |
| D02 | [mat-cadastro-ses-setis-dtd](https://github.com/victorarimatea/mat-cadastro-ses-setis-dtd) | Público | Matriz de cadastros de referência da DTD/SETIS/SES-DF |
| D03 | [hub-aprendizagem](https://github.com/victorarimatea/hub-aprendizagem) | Público | Repositório documental reflexivo — boas práticas, benchmarks e lições aprendidas da construção do ecossistema DTD/SETIS |

### Workflows (W) — memória organizacional de processos

| ID | Repositório | Visibilidade | Descrição |
|---|---|---|---|
| W01 | [wkf-transcricao-documental](https://github.com/victorarimatea/wkf-transcricao-documental) | Público | Processo completo de transcrição de PDFs regulatórios |
| W02 | wkf-registro-reuniao | Privado | Processo de registro institucional de reunião (PLAUD NOTE → SEI) |
| W03 | [wkf-registro-sessao](https://github.com/victorarimatea/wkf-registro-sessao) | Público | Registro estruturado de sessões de trabalho intensivo |
| W04 | [wkf-roadmap-geral](https://github.com/victorarimatea/wkf-roadmap-geral) | Público | Gestão de roadmap: ciclo semanal, staging area, diálogo estratégico e três camadas de curadoria |
| W05 | [wkf-auditoria-consistencia](https://github.com/victorarimatea/wkf-auditoria-consistencia) | Público | Auditoria de consistência do ecossistema em 5 camadas — independente da S04; sem token; apenas detecta e reporta |
| W06 | [wkf-sessao-agente](https://github.com/victorarimatea/wkf-sessao-agente) | Público | Protocolo de Sessão Assistida por Agente — padroniza abertura, trabalho e fechamento; processo pai do W03 e W05 |

### Agendas (A) — acervos cronológicos

| ID | Repositório | Visibilidade | Descrição |
|---|---|---|---|
| A01 | agd-dtd | Privado | Acervo institucional de reuniões da DTD, ordenado por data de ocorrência |

### Projetos (P) — iniciativas formais da DTD

| ID | Repositório | Status | Descrição |
|---|---|---|---|
| P01 | prj-telessaude-poc-prisional | em execução | PoC de totem de telemedicina no Sistema Prisional do DF |
| P02 | hub-memoria | em execução | Memória viva da construção do próprio ecossistema |

---

## Principais entregas

### Instrumento de Análise Comparativa — IAC

Padrão institucional de governança documental criado pela DTD. Opera em dois modos:

| Modo | Nome | Pergunta central |
|---|---|---|
| IAC-V | Análise Comparativa Vertical | O que mudou entre versões do mesmo documento? |
| IAC-H | Análise Comparativa Horizontal | Os documentos estão alinhados entre si? |

O IAC foi aplicado ao PDTIC 2024-2027 da SES-DF, produzindo:
- **IAC-V v0.2** — Análise de Revisão do PDTIC v1.5 → v1.8
- **IAC-H v0.1** — Análise de Conformidade PDTIC v1.8 × PTD-SES 2024-2027 (índice: 69%)

---

## Navegação neste repositório

| Arquivo | Por onde começar |
|---|---|
| [MANIFESTO.md](./MANIFESTO.md) | **Leia primeiro** — propósito, visão e princípios do projeto |
| [ROADMAP.md](./ROADMAP.md) | O que foi construído e o que está planejado |
| [CHANGELOG.md](./CHANGELOG.md) | Histórico completo de tudo que foi entregue |
| [DECISOES.md](./DECISOES.md) | As grandes decisões e seus motivos |
| [docs/arquitetura.md](./docs/arquitetura.md) | Como o ecossistema funciona tecnicamente |

---

## Contexto institucional

**Unidade:** Diretoria de Transformação Digital — DTD
**Órgão:** Secretaria Executiva de Tecnologia da Informação em Saúde — SETIS
**Secretaria:** Secretaria de Estado de Saúde do Distrito Federal — SES-DF
**Governo:** Governo do Distrito Federal — GDF
**Responsável:** Victor Leonardo Arimatea Queiroz — Diretor de Transformação Digital

---

*Este ecossistema é construído e mantido por um único servidor público,
em paralelo com projetos institucionais de alta complexidade,
com o objetivo de demonstrar que é possível fazer mais com menos
quando tecnologia, método e propósito se encontram.*
