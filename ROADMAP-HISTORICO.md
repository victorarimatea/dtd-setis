# Roadmap Histórico — DTD/SETIS/SES-DF

**Origem:** extraído do ROADMAP.md em 2026-06-24
**Mantenedor:** victorarimatea

> Registro das fases concluídas do ecossistema ATLAS — DTD/SETIS/SES-DF.
> É append-only: cada fase concluída migra do ROADMAP para cá.
> O detalhe operacional de cada entrega está no [CHANGELOG.md](./CHANGELOG.md).
> O ROADMAP ativo está em [ROADMAP.md](./ROADMAP.md).

---

## Linha do tempo

| Fase | Nome | Período | Marco principal |
|---|---|---|---|
| F1 | Fundação | Mai/2026 | Repositório âncora, portfólio, taxonomia, skill criador |
| F2 | Instrumentos Institucionais | Mai/2026 | Briefing, IAC, PoC, orquestração, P01 |
| F3 | Camada Documental | Mai/2026 | 28 docs transcritos, pipeline PDF→Markdown |
| F4 | Memória de Processos | Jun/2026 | Workflows, agendas, glossário, hub-memoria |
| F5 | Governança e Rastreabilidade | Jun/2026 | W05, hub-aprendizagem, escala SEV |
| F6 | Protocolo de Sessão | Jun/2026 | W06, Handoff, separação executor/auditor |
| F7 | Primeiro Roadmapping | Jun/2026 | W04 sessão 1, staging, 21 itens curados |
| F8 | Ciclo de Sessão Canônico | Jun/2026 | W03 v1.3, Handoff automático, convergência |
| F9 | Doutrina de Acesso | Jun/2026 | Dois tokens, raw aposentado, PROTOCOLO-SESSAO |
| F10 | ATLAS Nomeado | Jun/2026 | Núcleo/instância, hub-client-side, bloco-para-agentes |

---

## Detalhamento por fase

### Sessão 2026-06-21 — amadurecimento da transcrição documental
- ✅ `skl-transcricao-documental` (S05) v1.1 — §LOA, §DESIGN, ETAPA 7.5, ETAPA 8, §BACKLOG (concluído 2026-06-21)
- ✅ `doc-governanca-ses-df` (D01) v1.1 — PAS SES-DF 2026 em nova categoria `07-instrumentos-planejamento` (concluído 2026-06-21)

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

### Fase 10 — W04 sessão 2: curadoria estratégica e fundação do ecossistema ATLAS
- ✅ **Curadoria completa da staging** — 24 pendentes processados; Seção B zerada; zero pendentes em B e C ao final da sessão (2026-06-15) 📊
- ✅ **Formalização do fluxo rascunhos-staging** — `hub-entrada/rascunhos-staging/` como espinha do processo de criação: rito de criação (critérios de elegibilidade), rito de atualização (seções datadas), ciclo de vida do rascunho (3 status: pendente/aprovado/rejeitado), transições rascunho→hub-memoria→hub-aprendizagem (2026-06-15) 🔒
- ✅ **hub-client-side** — repositório agregador de pacotes instaláveis do ecossistema ATLAS; primeiro pacote S06-CS (registro de reunião) + meta-skill S-CSC (proto 🧪, ID S08 reservado); README com instrução de instalação e disclosure de compatibilidade; versão client-side não tem papel de escrita no ecossistema (2026-06-16) 📊
- ✅ **Versionamento source-only** — decisão de design fechada: versão vive na ficha técnica do próprio arquivo; coluna Versão removida do sumario.md; CONTEXTO.md fora da cadeia de propagação. Execução dedicada pendente: M01 + W05 Camada 1 + S04 (2026-06-15) 🔒
- ✅ **ATLAS nomeado** — nome fantasia do empreendimento; "ecossistema" permanece como termo operacional interno. Formulação canônica: "o ecossistema ATLAS, no qual a DTD é a primeira instância." Segunda instância iminente (2026-06-15) 📊
- ✅ **Separação núcleo/instância ATLAS** — inventário do que é portável vs. específico-DTD; prazo curto justificado pela iminência da segunda instância (2026-06-15) 📊
- ✅ **Modelo de priorização 🧪** — IS/RD/ES (eixos auto-computáveis) em teste; query calculada na leitura, nunca gravada; orienta, não determina. DOU e camada humana aguardam calibração (2026-06-15) 🧪
- ✅ **Governança da inovação via estado `em teste` (🧪)** — categoria formal de experimentação reversível: não-vinculante, rastreável (token 🧪 greppável), critério de saída (validar/ajustar/descartar). Rito leve W06 + validação profunda W04 + registro W03 (2026-06-15) 🔒
- ✅ **Bloco-para-agentes no README** — convenção de arquivo obrigatório com legenda das marcações do sistema; auditada pela W05; formalizada em M01/nomenclatura.md (2026-06-15) 🔒
- ✅ **Consulta de previsão na abertura** — loop simétrico ao fechamento na S04 e W06: consulta ROADMAP antes de aceitar intervenção; urgência declarada sobrepõe; consome modelo 🧪 de priorização (2026-06-15) 🔒
- ✅ **E1 redigido** — corolário "o auditor não escreve o próprio log" redigido como Seção 8 + Lição 6 do cap-02 hub-aprendizagem; depósito pendente na próxima sessão operacional (2026-06-15) 🔒
- ✅ **Versionamento source-only — execução dedicada agendada** — migração M01 + W05 Camada 1 (reescrever auditoria de propagação para coerência interna) + S04 checklists (2026-06-15) 🔒
- ✅ **Operacional maduro aprovado em bloco** — C3 (delay 3s S04), C5 (ergonomia fechamento W06), C6 (token nos blocos copiáveis), C8 (handoff com diagnóstico causal W03), C9 (princípio staging W04), C10 (critério curadoria W04) (2026-06-15) 🔒
- ✅ **Glossário — 4 termos aprovados** — PTD/PTD-SES, SGTD, CIG/SES, Fórum de Subsecretários; redigir definições formais no GLOSSARIO.md do M01 (2026-06-15) 🔒

---

> **Legenda de curadoria:**
> 🔒 interno — relevante para rastreabilidade, sem valor comunicacional externo
> 📊 estratégico — tem narrativa de valor para SETIS e instâncias superiores
> 🌐 público — comunicável externamente
