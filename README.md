# Diretoria de Transformação Digital — DTD/SETIS/SES-DF

---

## ⚠️ Instrução de inicialização — para o Claude

Se você é uma instância do Claude iniciando uma sessão de trabalho
no ecossistema DTD/SETIS, **leia o arquivo abaixo antes de qualquer ação**:

```
https://raw.githubusercontent.com/victorarimatea/ecossistema-sumario/main/CONTEXTO.md
```

Ele contém: estrutura completa do ecossistema, repositórios ativos,
convenções obrigatórias, protocolo de operações no GitHub (S04),
regras de aprendizado contínuo e instrução de inicialização de sessão.

**Sem a leitura do CONTEXTO.md, nenhuma operação deve ser iniciada.**

---


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
Matrizes (M)          Skills (S)              Documentos (D)        Projetos (P)
─────────────         ──────────────          ──────────────        ────────────
M01 ecossistema-      S01 skill-criador-      (em construção)       P01 telessaude-
    sumario               de-skills                                     poc-prisional
                                                                     (privado)
M02 saude-digital-    S02 skill-iac-
    taxonomia             pdtic

                      S03 skill-poc-
                          saude-digital

                      S04 skill-github-
                          orquestracao
```

### Como funciona

Toda skill consulta o repositório âncora (`ecossistema-sumario`) antes de
executar qualquer tarefa. As matrizes são fontes de verdade compartilhadas.
Os documentos são produzidos automaticamente, com acentuação correta,
estrutura padronizada e registro em backlog auditável.

Os projetos (tipo P) são repositórios privados com memória institucional
viva — atas, decisões, stakeholders e artefatos — consultáveis por
qualquer instância do ecossistema sob demanda.

---

## Principais instrumentos

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
| [dtd-setis](https://github.com/victorarimatea/dtd-setis) | Portfólio | Público | Este repositório — porta de entrada pública do ecossistema |
| [ecossistema-sumario](https://github.com/victorarimatea/ecossistema-sumario) | Matriz (M01) | Público | Âncora: sumário, nomenclatura, contexto e protocolo de atualizações |
| [saude-digital-taxonomia](https://github.com/victorarimatea/saude-digital-taxonomia) | Matriz (M02) | Público | Taxonomia estruturada de saúde digital |
| [skill-criador-de-skills](https://github.com/victorarimatea/skill-criador-de-skills) | Skill (S01) | Público | Cria novos repositórios de skill via API GitHub |
| skill-iac-pdtic | Skill (S02) | Privado | Gera IAC-V e IAC-H do PDTIC da SES-DF |
| [skill-poc-saude-digital](https://github.com/victorarimatea/skill-poc-saude-digital) | Skill (S03) | Público | Gera documentos de PoC em saúde digital no padrão SES-DF/DTD |
| [skill-github-orquestracao](https://github.com/victorarimatea/skill-github-orquestracao) | Skill (S04) | Público | Garante consistência do ecossistema a cada operação no GitHub |
| telessaude-poc-prisional | Projeto (P01) | Privado | PoC do Totem Health360 no Sistema Prisional do DF |

---

## Monitoramento de projetos

A DTD/SETIS/SES-DF mantém um painel público de acompanhamento dos projetos
em andamento, com visão panorâmica acessível a gestores e parceiros:

→ **[Ver monitoramento de projetos](./projetos/monitoramento.md)**

---

## Navegação neste repositório

Para uma visão completa de todos os arquivos e pastas, consulte o índice:

→ **[INDICE.md](./INDICE.md)** — mapa completo de conteúdo

| Arquivo / Pasta | Conteúdo |
|---|---|
| [MANIFESTO.md](./MANIFESTO.md) | Propósito, visão, objetivos e princípios do projeto |
| [ROADMAP.md](./ROADMAP.md) | O que está planejado e em que ordem |
| [CHANGELOG.md](./CHANGELOG.md) | Histórico completo do que foi construído |
| [DECISOES.md](./DECISOES.md) | Registro das grandes decisões e seus motivos |
| [projetos/monitoramento.md](./projetos/monitoramento.md) | Painel de projetos em execução e entregues |
| [docs/arquitetura.md](./docs/arquitetura.md) | Como o ecossistema funciona tecnicamente |

---

## Como utilizar as skills

As skills públicas do ecossistema podem ser utilizadas por qualquer membro
da DTD/SETIS diretamente no Claude, sem necessidade de configuração adicional.
Cada skill contém um `SKILL.md` com instruções completas de uso.

**Skills disponíveis para uso imediato:**

| Skill | O que faz | Como acionar |
|---|---|---|
| [skill-poc-saude-digital](https://github.com/victorarimatea/skill-poc-saude-digital) | Gera o documento completo de uma Prova de Conceito no padrão SES-DF/DTD | Descreva a solução e o problema — a skill conduz o processo |
| [skill-criador-de-skills](https://github.com/victorarimatea/skill-criador-de-skills) | Cria novos repositórios de skill com estrutura padronizada via API GitHub | Informe o nome e propósito da nova skill |
| [skill-github-orquestracao](https://github.com/victorarimatea/skill-github-orquestracao) | Garante que toda operação no ecossistema atualize todos os arquivos afetados — plano, aprovação, execução | Presente automaticamente em qualquer operação que altere repositórios |

**Skills de uso interno (requerem acesso privado):**

| Skill | O que faz |
|---|---|
| skill-iac-pdtic | Gera Instrumento de Análise Comparativa (IAC-V e IAC-H) para o PDTIC da SES-DF |

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
