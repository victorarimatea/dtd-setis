# Diretoria de Transformação Digital — DTD/SETIS/SES-DF

> **Tecnologia pública a serviço da saúde das pessoas.**

Este repositório é a porta de entrada pública do ecossistema de automação
e governança documental desenvolvido pela Diretoria de Transformação Digital
da Secretaria Executiva de Tecnologia da Informação em Saúde (SETIS) da
Secretaria de Estado de Saúde do Distrito Federal (SES-DF).

---

## O que é a DTD

A Diretoria de Transformação Digital (DTD) é uma unidade da SETIS/SES-DF
criada para liderar a agenda de inovação tecnológica em saúde no Distrito
Federal, com foco em:

- Governança documental de instrumentos de planejamento de TIC e transformação digital
- Automação de processos institucionais com uso de inteligência artificial
- Padronização de fluxos de análise e aprovação de documentos estratégicos
- Construção de memória institucional auditável e consultável

---

## O Ecossistema DTD/SETIS

O ecossistema é um conjunto integrado de repositórios, skills de IA e
instrumentos padronizados que trabalham juntos para automatizar a gestão
de conhecimento e a produção de documentos institucionais.

```
Matrizes (M)          Skills (S)              Documentos (D)
─────────────         ──────────────          ──────────────
M01 ecossistema-      S01 skill-criador-      D01 governanca-
    sumario               de-skills               ses-df
                                              (em construção)
M02 saude-digital-    S02 skill-iac-
    taxonomia             pdtic

                      S03 skill-poc-
                          saude-digital
```

### Como funciona

Toda skill consulta o repositório âncora (`ecossistema-sumario`) antes de
executar qualquer tarefa. As matrizes são fontes de verdade compartilhadas.
Os documentos são produzidos automaticamente, com acentuação correta,
estrutura padronizada e registro em backlog auditável.

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

### Prova de Conceito em Saúde Digital — PoC

Padrão institucional de avaliação de soluções tecnológicas em saúde criado pela DTD.
Baseado na PoC MedNear, caso zero do Marco Regulatório Interno de PoCs da SES-DF.

Documentos gerados seguem estrutura com 11 seções obrigatórias: contexto, objetivos,
escopo, fluxo operacional, governança, cronograma, métricas, gestão de riscos,
aspectos regulatórios, deliberações pendentes e resultado esperado.

---

## Repositórios do ecossistema

| Repositório | Tipo | Visibilidade | Descrição |
|---|---|---|---|
| [ecossistema-sumario](https://github.com/victorarimatea/ecossistema-sumario) | Matriz | Público | Âncora do ecossistema: sumário, nomenclatura e contexto |
| [saude-digital-taxonomia](https://github.com/victorarimatea/saude-digital-taxonomia) | Matriz | Público | Taxonomia estruturada de saúde digital |
| [skill-criador-de-skills](https://github.com/victorarimatea/skill-criador-de-skills) | Skill | Público | Cria novos repositórios de skill via API GitHub |
| [skill-iac-pdtic](https://github.com/victorarimatea/skill-iac-pdtic) | Skill | Privado | Gera IAC-V e IAC-H do PDTIC da SES-DF |
| [skill-poc-saude-digital](https://github.com/victorarimatea/skill-poc-saude-digital) | Skill | Público | Gera documentos de PoC em saúde digital no padrão SES-DF/DTD |

---

## Navegação neste repositório

| Arquivo | Conteúdo |
|---|---|
| [MANIFESTO.md](./MANIFESTO.md) | Propósito, visão, objetivos e princípios do projeto |
| [ROADMAP.md](./ROADMAP.md) | O que está planejado e em que ordem |
| [CHANGELOG.md](./CHANGELOG.md) | Histórico completo do que foi construído |
| [DECISOES.md](./DECISOES.md) | Registro das grandes decisões e seus motivos |
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

