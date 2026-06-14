# Roadmap — DTD/SETIS/SES-DF

**Última atualização:** 2026-06-14
**Versão do ecossistema:** sumario v3.9 | S04 v2.9 | W05 v1.3 | W06 v1.3

---

## ✅ Concluído

### Fase 1 — Fundação do ecossistema
- ✅ Repositório âncora `hub-fonte` (M01) com sumário, nomenclatura,
  glossário, CONTEXTO.md e protocolo de operações
- ✅ Portfólio público `hub-entrada` com MANIFESTO, ROADMAP, CHANGELOG, DECISOES
- ✅ Taxonomia de saúde digital `mat-saude-digital-taxonomia` (M02)
- ✅ Skill criador de skills `skl-criador-de-skills` (S01)

### Fase 2 — Instrumentos institucionais
- ✅ Skill briefing `skl-briefing-saude-digital` (S07) — monitoramento periódico de saúde digital com taxonomia
- ✅ Skill IAC `skl-iac-pdtic` (S02) — IAC-V e IAC-H do PDTIC
- ✅ Skill PoC `skl-poc-saude-digital` (S03) — PoCs em saúde digital
- ✅ Skill orquestração `skl-github-orquestracao` (S04 v1.8) —
  consistência do ecossistema; 9 tipos de operação; 5 verificações pós-execução
- ✅ Projeto `prj-telessaude-poc-prisional` (P01) — PoC Totem Health360

### Fase 3 — Camada documental
- ✅ `doc-governanca-ses-df` (D01) — 28 documentos transcritos: legislação federal,
  distrital, portarias ministeriais, resoluções CFM/ANVISA, referências
  internacionais bilíngues EN+PT
- ✅ `skl-transcricao-documental` (S05) — pipeline de transcrição PDF→Markdown
- ✅ `mat-cadastro-ses-setis-dtd` (D02) — matriz de cadastros de referência
- ✅ Tipo D (Documentos) formalizado no ecossistema

### Fase 4 — Memória organizacional de processos
- ✅ Tipo W (Workflows) formalizado — WORKFLOW.md 8 seções, logs de execução,
  relação W↔P, referência cruzada via EXECUCOES.md
- ✅ `wkf-transcricao-documental` (W01) — caso zero do tipo W
- ✅ `wkf-registro-reuniao` (W02) — processo PLAUD NOTE → SEI
- ✅ `wkf-registro-sessao` (W03) — registro estruturado de sessões de trabalho intensivo (2026-06-02)
- ✅ Tipo A (Agendas) formalizado — indexação cronológica, data_reuniao vs
  data_registro, estrutura reunioes/AAAA/MM/
- ✅ `agd-dtd` (A01) — acervo cronológico de reuniões da DTD
- ✅ `skl-registro-reuniao` (S06) — transformação de resumos em registros
  institucionais padronizados para o SEI
- ✅ GLOSSARIO.md com 8 categorias e 34+ termos formais
- ✅ Saneamento de drifts e auditoria cruzada de consistência (Erro #007)
- ✅ `hub-memoria` (P02) — projeto de memória da construção do ecossistema (2026-06-02)

### Fase 5 — Governança e rastreabilidade cronológica
- ✅ `wkf-auditoria-consistencia` (W05) criado — Workflow de Auditoria de Consistência em 5 camadas; independente da S04; resposta estrutural ao GAP 1 (2026-06-05)
- ✅ `hub-aprendizagem` criado — repositório de memória intelectual: boas práticas, benchmarks e lições aprendidas (2026-06-05)
- ✅ S04 v2.5 — escala de severidade SEV1–SEV4; classificação retroativa de 13 erros — 2026-06-05
- ✅ S04 v2.6 — verificações embutidas CONFIRMAR em todas as checklists OP-X; regra de dois registros; padrão de campos de erro — 2026-06-05
- ✅ Exercício de engenharia reversa: 13 pontos de falha, 4 GAPs estruturais identificados — 2026-06-05
- ✅ S04 v2.2 e W03 v1.1 — gestão de ROADMAP para itens não previstos: reconciliação obrigatória a cada operação (2026-06-04)
- ✅ W04 `wkf-roadmap-geral` v1.0 — workflow de gestão de roadmap com staging area, três camadas de curadoria e ciclo semanal de revisão estratégica (2026-06-04) 📊
- ✅ `staging.md` — staging area criada no hub-entrada: receptor de registros automáticos (S04) e ideias mineradas (Etapa 6-A) (2026-06-04) 🔒
- ✅ Correção de drifts de nomenclatura legada no M01 (ONBOARDING.md v1.1, INDICE.md, README.md v0.11) — 2026-06-05
- ✅ S04 v2.4 — seção "Intenção do Comandante" adicionada; ONBOARDING.md incluído na Verificação 5; IDENTIDADE DO ECOSSISTEMA corrigida; Erro #012 documentado — 2026-06-05
- ✅ Princípio de integridade de registros históricos formalizado — texto operacional (corrigir) vs texto histórico (preservar) — 2026-06-05
- ✅ S04 v2.3 — Etapa 6-A: mineração ativa de ideias com 7 critérios de elegibilidade e procedimento de 6 passos (2026-06-04)

### Fase 6 — Protocolo de sessão e conformidade estrutural
- ✅ hub-aprendizagem reclassificado como D03 — repositório documental reflexivo (2026-06-06)
- ✅ 19 divergências corrigidas em duas rodadas de auditoria W05 independente (2026-06-06)
- ✅ Separação executor/auditor demonstrada empiricamente — auditoria independente encontrou erros introduzidos pela própria operação de correção (2026-06-06)
- ✅ `wkf-sessao-agente` (W06) criado — Protocolo de Sessão Assistida por Agente; processo pai do W03 e W05; governa abertura, trabalho e fechamento com Handoff entre sessões (2026-06-06)
- ✅ Conceito de Handoff introduzido formalmente no ecossistema como padrão arquitetural em amadurecimento (2026-06-06)
- ✅ Perguntas orientadoras como técnica de instrução incorporadas ao W06 (2026-06-06)
- ✅ Alerta de cache raw.githubusercontent.com protocolado no W05 (2026-06-06)
- ✅ Escala SEV1–SEV4 e Auditoria de Consistência adicionados ao GLOSSARIO.md (2026-06-06)
- ✅ S04 v2.7 — Etapa 6-A expandida com mineração de conhecimento consolidado (2026-06-05) 🔒
- ✅ W03 v1.2 — Etapa 2-B: identificação de aprendizados consolidados (2026-06-05) 🔒
- ✅ cap-03 hub-aprendizagem v1.1 — "Conhecimento como Query" + design wiki-ecossistema (2026-06-07) 📊

### Fase 7 — Primeira sessão de roadmapping (W04)
- ✅ Primeira execução do W04 `wkf-roadmap-geral` — 21 itens curados, ROADMAP estruturado por camadas, staging limpa (2026-06-08) 📊
- ✅ GLOSSARIO.md v2.2 — 5 termos novos adicionados à Categoria 17 (2026-06-08) 🔒

### Fase 8 — Formalização do ciclo de sessão
- ✅ W03 v1.3 — estrutura do relatório de encerramento formalizada em três blocos: (I) narrativa; (II) ciclo de qualidade [operações S04, ciclo auditoria→correção, declaração de convergência]; (III) Bloco de Handoff (2026-06-12)
- ✅ W03 v1.3 — convergência adotada como estado + resíduo SEV no frontmatter: campos `convergencia` (atingida/nao-atingida) e `residuo_tolerado` [SEV3/SEV4]; declaração que autoriza o encerramento (2026-06-12)
- ✅ W06 v1.2 — localização automática do handoff na abertura: a sessão lê o Bloco de Handoff como seção final do último relatório no hub-memoria via API; elimina a cola manual e o atrito diário de abertura (2026-06-12)
- ✅ W06 v1.2 — regra de fallback do handoff: falha na extração aciona auditoria W05 nova do zero, nunca reverte ao processo manual de colagem (decisão do mantenedor, 2026-06-12)

### Fase 9 — Protocolo de sessão canônico e doutrina de acesso
- ✅ `hub-entrada/PROTOCOLO-SESSAO.md` v1.0 — lar canônico e versionado dos ritos de sessão (abertura, fechamento, leitura); consolida as ideias de fluidez mineradas em 2026-06-11/06-12; blocos sempre em code fence copiável (2026-06-13)
- ✅ Doutrina de dois tokens adotada — token de leitura ampla na abertura (alcança privados; 5000 req/h; sem cache CDN) e token de edição só na conversão para escrita; raw aposentado como canal de sessão. Propagada ao S04 (ETAPA 0, v2.8) e ao CONTEXTO.md (v3.9) (2026-06-13)
- ✅ Doutrina de dois tokens propagada ao W05 (`wkf-auditoria-consistencia` v1.3 — auditor opera só com token de leitura, nunca edição; Etapa 8 redesenhada: log depositado pela sessão executora) e ao W06 (`wkf-sessao-agente` v1.3 — Pacotes 1/2 pedem token de leitura). Conclui o I1 e fecha o SEV3 de acesso herdado (2026-06-14)

---

## 🔄 Em andamento

- 🔄 P01 `prj-telessaude-poc-prisional` — PoC aguardando definição de unidade
  piloto (12 deliberações pendentes, ver README.md do P01)
- 🔄 Upload e transcrição dos documentos pendentes no D01 (itens 10–17 do §9
  do WORKFLOW-ESPECIFICACAO.md)

---

## 🎯 Próxima ação imediata

**Missão definida na sessão W04 de 2026-06-08 — correções técnicas remanescentes:**

- ✅ I1 — Concluído (2026-06-14): doutrina de dois tokens propagada ao W05/WORKFLOW.md (v1.3 — auditor só com token de leitura, nunca edição; Etapa 8 redesenhada: log depositado pela sessão executora) e aos Pacotes 1/2 do W06/WORKFLOW.md (v1.3). Leitura/escrita via API autenticada; raw aposentado como canal de sessão. CONTEXTO.md (v3.10), sumario.md (v3.7) e S04/ETAPA 0 (v2.8) alinhados. Fecha o SEV3 de acesso herdado no W05
- I2 — Padronizar "perguntas orientadoras" (substituir "ordenadoras") na S04 e W06
- I3 — Corrigir campo Versão da Seção 1 do W06/WORKFLOW.md (v1.0 → v1.1)
- I4 — Corrigir ID W07 do `wkf-iac-conformidade` no ROADMAP.md
- I5 — Adicionar entrada raw vs API ao hub-aprendizagem (aprendizado consolidado T1)
- I6 — Atualizar campo "Versão do ecossistema" no ROADMAP.md já refletido nesta versão

---

## 📅 Médio prazo

### Reclassificação W03 e fronteira skill↔workflow (meta autônoma)
- **Sessão evolutiva dedicada — contém DECISÃO DE DESIGN, não só execução.**
  Definir com clareza o critério que separa skill de workflow no ecossistema e
  aplicá-lo daqui em diante. Pode resultar em renomear
  `wkf-registro-sessao`→`skl-registro-sessao` OU em manter o nome e cravar o
  critério de classificação. Toca a fonte de verdade (sumario.md, nomenclatura,
  referências cruzadas). Vinculada à disciplina de Arquitetura do Conhecimento
  (staging Seção C) — provável abordagem conjunta

- Criar `wkf-resumo-executivo` (W07 reservado) — workflow para estruturar, aprovar
  e distribuir Resumo Executivo para SETIS e Secretário de Saúde; ativo estratégico
  em amadurecimento permanente
- Criar `wiki-ecossistema` — projeto formal; camada de hipertexto navegável do
  ecossistema; arquitetura de 3 camadas discutida em 2026-06-07
- Adotar timestamp ISO 8601 completo (`2026-06-08T14:00:00-03:00`) em entradas
  novas de backlog/changelog — aplicação prospectiva, sem refatoração retroativa
- Refinar critério de duplicata do W05 — duplicata = mesmo número de versão COM
  mesmo conteúdo/propósito (complementa timestamp ISO)
- Reorganização do `backlog-versoes.md` do M01 — missão dedicada; 910+ linhas
  com numeração duplicada e séries entrelaçadas
- Intenção do Comandante como princípio universal — declarar no `nomenclatura.md`
  e propagar às skills existentes
- Criar `pdtic-historico` (D — tipo Documento) — versionamento histórico do PDTIC
  com IACs gerados
- Criar `governanca-ses-df-fase3` — transcrição dos documentos 10–17 pendentes
- Evoluir S05 para fase sequencial autônoma (condição: PASSOU ≥ 95% em ≥ 10 docs)
- Criar `wkf-iac-conformidade` (W07) — análise de conformidade documental
  automatizada, consumindo D01 e S02 como subprocessos
- Integração SEI via API quando disponível

---

## 🌱 Maturando

- Campos autor/revisor nas entradas de backlog — aguarda primeiro colaborador externo
- Perfis de acesso formais do ecossistema — aguarda colaborador externo
- Família de workflows derivados do W04 por projeto (`wkf-roadmap-telessaude` etc.)
  — aguarda projeto em fase ativa

---

## 🔭 Longo prazo

- GitHub MCP para operações autenticadas sem PAT manual
- Migração de PAT clássico para fine-grained com escopos mínimos e expiração curta
- Replicação do modelo de ecossistema para outras unidades da SES-DF
- Case institucional documentado para publicação

---

> **Legenda de curadoria:**
> 🔒 interno — relevante para rastreabilidade, sem valor comunicacional externo
> 📊 estratégico — tem narrativa de valor para SETIS e instâncias superiores
> 🌐 público — comunicável externamente
> *(itens sem símbolo = curadoria pendente ou não aplicável)*
