## [2026-06-15] — Frente 1 operacional: atualizações de workflow e consolidação de conhecimento

### Adicionado
- `hub-aprendizagem` v1.3: Seção 8 e Lição 6 adicionadas ao cap-02 — corolário E1 "O auditor não escreve o próprio log" (conhecimento consolidado depositado após aprovação W04)
- `hub-fonte/GLOSSARIO.md` v2.3: 4 definições formais — PTD-SES, SGTD, CIG/SES, Fórum de Subsecretários (termos de governança normativa SES-DF aprovados B1–B4)

### Atualizado
- `wkf-sessao-agente` W06 v1.4: ergonomia de fechamento (C5) — entrega de Pacote 2 e Bloco 1 em code fence copiável; declaração de token (C6)
- `wkf-registro-sessao` W03 v1.4: Handoff com diagnóstico causal (C8) — pendências declaram "por que" além de "o que"
- `wkf-roadmap-geral` W04 v1.1: princípio da staging formalizado (C9); critério de maturação 3-sessões adicionado à Etapa 5 (C10)
- `skl-github-orquestracao` S04 v2.10: delay obrigatório de 3s pós-PUT antes do GET de CONFIRMAR (C3 / Erro #015 SEV2)
- `hub-entrada/PROTOCOLO-SESSAO.md` v1.1: declaração explícita de tipo de token nos blocos copiáveis (C6)


## [2026-06-16]

### Adicionado
- `hub-aprendizagem` cap-04: API vs raw.githubusercontent.com — cache coherence,
  read-after-write consistency e doutrina de dois tokens (item I5 da fila herdada) 🔒
- `hub-aprendizagem` benchmarks.md: entrada Cache Coherence / Read-After-Write Consistency
- `DECISOES.md` D007: Modelo APPEND para depósito W03 — formalização da decisão doutrinária

- - `hub-client-side` (S08) v0.1: repositório criado — pacotes instaláveis do ecossistema ATLAS; S06-CS (registro de reunião client-side) + S-CSC 🧪 proto (meta-skill criador de client-sides, ID S08 reservado); README com bloco-para-agentes e disclosure de compatibilidade 📊

### Corrigido / fechado
- ROADMAP.md: I2 e I3 fechados como concluídos empiricamente
- ROADMAP.md: I4 corrigido — `wkf-resumo-executivo` = W07; `wkf-iac-conformidade` = W08
- ROADMAP.md: I5 fechado — cap-04 adicionado ao D03
- staging.md Seção E: T1 (API vs raw) marcado como `registrado`
- ROADMAP.md: hub-client-side marcado ✅ (Frente 2 concluída)

---
## [Não versionado] — 2026-06-14 (correção pós-reauditoria W05)

### Correção de 6 SEV2 + 2 SEV3 + 4 SEV4 detectados no fechamento

A reauditoria W05 independente da sessão de propagação dos dois tokens detectou
12 divergências (zero SEV1). Decisão do mantenedor: corrigir todas, sem agendar.

#### SEV2 — READMEs fora do grafo de versões (sincronizados ao sumario.md)
- `wkf-auditoria-consistencia/README.md` v1.2 -> v1.3
- `wkf-sessao-agente/README.md` v1.2 -> v1.3 (estes dois introduzidos na própria
  sessão — ver Erro #014 da S04)
- `skl-github-orquestracao/README.md` v2.7 -> v2.9
- `hub-fonte/README.md` v0.31 -> v0.36
- `hub-entrada/README.md` v2.0 -> v2.1 (+ entrada de backlog v2.1 — fecha o SEV3)
- `hub-memoria` reconciliado v0.3 -> v0.4 (sumario + README; v0.4 já no backlog)

#### SEV3 — backlog e reconciliação
- `hub-entrada/backlog` recebe a entrada v2.1 ausente
- `mat-saude-digital-taxonomia` reconciliado para v1.1 (README + sumario);
  backlog histórico preservado (v1.1 já declarada lá desde 2026-06-04)

#### SEV4 — glossário (4 termos adicionados)
- Convergência; Doutrina de dois tokens; Grafo de dependências de versão; Defense in Depth

#### Prevenção da causa-raiz (S04 v2.8 -> v2.9)
- Erro #014 registrado; checklist OP-W ganha item README; regra universal de
  sincronização de README (nó do grafo de versões). CONTEXTO.md v3.10 -> v3.11;
  sumario.md v3.7 -> v3.8 (M01 v0.36, M02 v1.1, P02 v0.4, S04 v2.9).

#### Ideias mineradas (staging, com aval do mantenedor)
- Seção E: "o auditor não escreve o próprio log" (corolário da separação executor/auditor)
- Seção C: campo de token em blocos copiáveis deve declarar QUAL token

Reforço da separação executor/auditor: a autoverificação da S04 declarou
convergência, mas a auditoria independente expôs os READMEs defasados.

---

## [Não versionado] — 2026-06-14 (sessão de operação — doutrina ao W05/W06)

### Doutrina de dois tokens propagada ao W05 e W06 — I1 concluído

Concluído o item I1 do ROADMAP: a doutrina de dois tokens — antes consolidada
no PROTOCOLO-SESSAO.md, no S04 (ETAPA 0) e no CONTEXTO.md — foi propagada aos
workflows de sessão.

- **W05 `wkf-auditoria-consistencia` v1.2 -> v1.3:** o auditor opera
  exclusivamente sob o **token de leitura ampla** e **nunca recebe o token de
  edição**. Etapa 0 reescrita do enquadramento "API/raw + cache" para a
  doutrina. Etapa 8 redesenhada (decisão do mantenedor, Opção A): o log de
  execução é depositado pela **sessão executora** (S04, token de edição), nunca
  pelo auditor. Fecha o SEV3 de acesso herdado e a contradição interna
  "sem acesso a token" x "log com token ativo".
- **W06 `wkf-sessao-agente` v1.2 -> v1.3:** os Pacotes 1 (abertura) e 2
  (auditoria) passam a pedir o **token de leitura**; o token de edição entra só
  na conversão para escrita. Remove a ambiguidade que levava à colagem do token
  de edição na abertura.

#### Propagação
- hub-fonte: sumario.md v3.6 -> v3.7 (W05/W06 -> v1.3; M01 -> v0.35),
  CONTEXTO.md v3.9 -> v3.10, backlog v0.35
- ROADMAP: I1 marcado como concluído; "Versão do ecossistema" atualizada

---

## [Não versionado] — 2026-06-13 (correção pós-auditoria W05)

### Correção de 1 SEV2 + 2 SEV3 detectados no fechamento

A auditoria W05 independente da sessão do protocolo de sessão identificou e
corrigiu, na mesma data:
- **SEV2** — `hub-fonte/CONTEXTO.md`: a célula do S04 na tabela de repositórios
  mostrava v2.7 enquanto `sumario.md` (v3.6) e `SKILL.md` já estavam em v2.8;
  descrição também desatualizada. Último salto do grafo `sumario → CONTEXTO`
  ficou incompleto na propagação de v0.34. Corrigido para v2.8 + menção à
  ETAPA 0 de dois tokens (correção dentro da v3.9, sem novo bump).
- **SEV3** — `hub-fonte/CONTEXTO.md`: linha do W05 dizia "sem token"; sob a
  doutrina de dois tokens o W05 (Modo 2) usa token de leitura. Ajustado para
  "sem token de edição".
- **SEV3** — `hub-entrada/INDICE.md`: contagem corrigida de 13 → 12 (árvore
  real) e `staging.md` adicionada à tabela da raiz (estava omitida).

Reforça o ganho da separação executor/auditor: o CHANGELOG da sessão afirmava
a propagação ao CONTEXTO concluída, mas a auditoria independente mostrou o
número do S04 ausente na tabela. Mesma classe dos SEV2 de 2026-06-12 (D3/D4).

---

## [Não versionado] — 2026-06-13 (sessão de operação — protocolo de sessão)

### PROTOCOLO-SESSAO.md criado e doutrina de dois tokens adotada

Criado o `hub-entrada/PROTOCOLO-SESSAO.md` v1.0 — lar canônico dos ritos de
sessão (abertura, fechamento, leitura), consolidando as ideias de fluidez
mineradas em 2026-06-11 e 2026-06-12. Os blocos operacionais vivem no arquivo;
os blocos de notas viram ponteiros enxutos.

#### Doutrina de dois tokens (supera a regra "API/raw")
- **Token de leitura ampla** na abertura de toda sessão — alcança repositórios
  privados (o handoff mora no hub-memoria, privado), eleva o teto a 5000 req/h
  e elimina o cache CDN. Era a causa-raiz das falhas recorrentes de leitura.
- **Token de edição** apenas na conversão para escrita; revogado ao fim.
- `raw.githubusercontent.com` aposentado como canal de sessão.

#### Propagação
- S04 v2.7 → v2.8 (ETAPA 0 reescrita); hub-fonte CONTEXTO.md v3.8 → v3.9,
  sumario.md v3.5 → v3.6, backlog v0.34; hub-entrada v2.1
- Item I1 do ROADMAP resolvido para CONTEXTO e S04 (raw → API); resta
  propagar ao W05/WORKFLOW.md
- Reconciliada a versão do M01 no sumario (v0.31 → v0.34), defasagem de
  propagação herdada

---

## [Não versionado] — 2026-06-12 (correção pós-auditoria W05)

### Correção de divergências SEV2 detectadas no fechamento

A auditoria W05 independente de 2026-06-12 identificou 4 divergências SEV2 de
propagação de versão, todas corrigidas na mesma sessão:
- D1: `wkf-sessao-agente/README.md` v1.1 → v1.2
- D2: `wkf-registro-sessao/README.md` v1.2 → v1.3
- D3: `wkf-registro-sessao/WORKFLOW.md` tabela Seção 1, campo Versão v1.0 → v1.3
- D4: `hub-entrada/ROADMAP.md` campo "Versão do ecossistema" → sumario v3.5 |
  S04 v2.7 | W06 v1.2; "Última atualização" → 2026-06-12

Todas eram divergências de propagação: a operação principal atualizou os
arquivos canônicos (WORKFLOW.md, sumario, CONTEXTO) mas não propagou para
READMEs, tabela interna e campo de versão do ROADMAP. Lição reforçada — relação
direta com a ideia "Consulta de previsão na abertura" e com a ordem de
dependência de sincronização de versões.

---

## [Não versionado] — 2026-06-12 (sessão de operação)

### Formalização do ciclo de sessão implementada — W03 v1.3 e W06 v1.2

**Execução das 3 metas desenhadas na sessão de design de 2026-06-11.**

#### W03 v1.3 — estrutura do relatório de sessão
- Seção 6 reorganizada em três blocos: (I) narrativa; (II) ciclo de qualidade
  [operações S04, ciclo auditoria→correção, declaração de convergência];
  (III) Bloco de Handoff como seção final
- Frontmatter expandido com `convergencia` (atingida/nao-atingida) e
  `residuo_tolerado` [SEV3/SEV4], ancorando a convergência na escala SEV existente

#### W06 v1.2 — localização automática do handoff
- Etapa 2 reescrita: a abertura lê o Bloco de Handoff do último relatório no
  hub-memoria via API, sem cola manual — elimina o atrito diário de abertura
- Regra de fallback: falha na extração do handoff aciona auditoria W05 nova do
  zero, nunca reverte ao processo manual de colagem
- Pacote 1 (mensagem de abertura) atualizado para refletir a leitura automática

#### Propagação
- hub-fonte: sumario.md v3.5, CONTEXTO.md v3.8, backlog v0.33
- ROADMAP: bloco "Formalização do ciclo de sessão" concluído (Fase 8); removido
  do médio prazo

---

## [Não versionado] — 2026-06-11 (sessão de design)

### Design do ciclo de sessão — relatório de encerramento, Handoff e ritos

**Sessão de design conceitual conduzida por etapas, como discussão de princípios.**

#### Decisões de arquitetura amadurecidas
- O rito de condução mora no W06 (roteiro); o W03 define a forma do relatório (ata)
- O Handoff é a seção final do relatório, vivendo no hub-memoria — localizado pela
  abertura via API, eliminando o atrito de colá-lo manualmente a cada sessão
- Convergência declarada como estado + resíduo SEV (não rótulo novo); sessão sem
  convergência entrega dívida prioritária
- Classificação de sessão por modos coexistentes (escreve / não-escreve), não por
  tipos rígidos; sessão de leitura dispensa o rito completo de auditoria

#### Roteado ao ROADMAP (Médio prazo)
- Bloco "Formalização do ciclo de sessão" — 3 metas fechadas
- Meta autônoma "Reclassificação W03 e fronteira skill↔workflow" — contém decisão
  de design pendente; deixada separada para amadurecer

#### Roteado à staging (Seção C — pendentes)
- Memória de domínio do briefing de saúde digital (1ª categoria de registro de conteúdo)
- Contribuição externa via issues públicas (viabilidade técnica confirmada)
- Disciplina de Arquitetura do Conhecimento (3ª camada de governança, do anexo)

#### Princípio metodológico registrado
- "A velocidade pode ser nossa inimiga" — sistema robusto se constrói passo a passo;
  a staging existe para reter ideias que atropelam o fluxo, não para deixá-las
  sequestrar o trabalho corrente

## [Não versionado] — 2026-06-08 (W04)

### W04 — Primeira sessão de roadmapping

**Primeira execução formal do workflow W04 `wkf-roadmap-geral`.**

#### Curadoria realizada
- 10 registros automáticos (Seção A) processados — Seção A limpa
- 21 ideias mineradas (Seção C) curadas:
  - 13 aprovadas → ROADMAP (ações imediatas, médio prazo ou longo prazo)
  - 5 maturando → permanecem na Seção C
  - 3 maturando por decisão explícita do mantenedor (aguardam colaborador externo ou projeto ativo)
- 2 entradas duplicadas do `wkf-resumo-executivo` consolidadas em 1

#### Atualizado
- `ROADMAP.md` — Fase 7 criada; próxima missão estruturada (I1–I6);
  médio prazo reorganizado; seção Maturando criada; legenda de curadoria adicionada
- `staging.md` — Seção A limpa; Seção D populada com 12 entradas históricas;
  itens curados com decisão e curadoria registradas
- `GLOSSARIO.md` (hub-fonte) → v2.2 — 5 termos novos adicionados à Categoria 17

#### Decisões de design registradas
- Filosofia da staging area formalizada: idéias em excesso são preferíveis
  a idéias perdidas — a curadoria é o momento da consolidação, não o registro
- `wkf-resumo-executivo` definido como ativo estratégico permanente em
  amadurecimento, não entregável pontual
- Wiki-ecossistema aprovado como projeto formal de médio prazo
- Timestamp ISO 8601 adotado para entradas novas — sem refatoração retroativa

## [Não versionado] — 2026-06-05 (W05)

### Adicionado
- `wkf-auditoria-consistencia` (W05) — Workflow de Auditoria de Consistência:
  processo independente da S04 que verifica o estado real do ecossistema em
  5 camadas (versões, arquivos obrigatórios, hub-entrada, backlogs, glossário).
  Resposta estrutural ao GAP 1 identificado no exercício de engenharia reversa.
  Não executa operações — detecta, classifica por SEV e reporta.


## [Não versionado] — 2026-06-05

### Adicionado
- `hub-aprendizagem` — repositório de memória intelectual do ecossistema:
  boas práticas, benchmarks externos e lições aprendidas. Primeiro capítulo:
  "Engenharia Reversa de um Ecossistema Vivo" — diagnóstico completo de
  falhas sistêmicas, 4 GAPs estruturais identificados, benchmarks (AAR, ADR,
  Defense in Depth, SEV, DORA) e respostas aplicadas.
- S04 v2.5: escala de severidade SEV1–SEV4 adotada; 13 erros classificados
  retroativamente
- S04 v2.6: verificações embutidas obrigatórias (CONFIRMAR) em todas as
  checklists OP-X; regra de dois registros para erros novos; padrão de
  campos obrigatórios na seção de erros


## [3.2] — 2026-06-05

### Corrigido
- Drifts de nomenclatura legada em três arquivos operacionais do M01
  (`ONBOARDING.md` v1.0 → v1.1, `INDICE.md`, `README.md` v0.10 → v0.11):
  campos de metadados e URL de sessão ainda referenciavam `ecossistema-sumario`
  e `dtd-setis` (nomes anteriores de `hub-fonte` e `hub-entrada`)
- Seção IDENTIDADE DO ECOSSISTEMA da S04 corrigida para nomenclatura atual

### Adicionado
- Seção "Intenção do Comandante" à S04 — princípio arbitrador para situações
  não cobertas pelos procedimentos: texto operacional (corrigir) versus texto
  histórico (preservar). Formaliza que registros em CHANGELOG e backlogs que
  referenciam nomenclaturas legadas são imutáveis por representarem o estado
  real do sistema no momento em que foram escritos

### Atualizado
- `skl-github-orquestracao` (S04) → v2.4: Intenção do Comandante adicionada;
  ONBOARDING.md incluído na Verificação 5 como item 6; Erro #012 documentado
- `hub-fonte` (M01) → v0.11 (README): título, tabela de arquivos e URL de sessão
  atualizados para nomenclatura atual

---

## [3.1] — 2026-06-04

### Adicionado
- W04 `wkf-roadmap-geral` v1.0 — workflow de gestão de roadmap genérico e replicável;
  ciclo semanal de revisão estratégica com três camadas (interna, estratégica, pública),
  staging area, diálogo estratégico com perguntas provocadoras e geração de Resumo Executivo
- `hub-entrada/staging.md` v1.0 — staging area com quatro seções: registros automáticos (S04),
  ideias sinalizadas, ideias mineradas (Etapa 6-A) e arquivo histórico; política de limpeza
  e ciclo de vida completo das ideias

### Atualizado
- S04 `skl-github-orquestracao` → v2.3: Etapa 6-A adicionada — mineração ativa de ideias
  com 7 perguntas orientadoras de elegibilidade, procedimento de 6 passos e depósito na
  staging.md/Seção C. Erro #011 registrado.

---

## [3.0] — 2026-06-04

### Atualizado
- `skl-github-orquestracao` (S04) → v2.2: Verificação 5-A adicionada —
  reconciliação obrigatória com ROADMAP ao final de toda operação. Itens
  previstos marcados ✅ com data; itens não previstos incluídos retroativamente
  já como ✅ com data. Erro #010 registrado.
- `wkf-registro-sessao` (W03) → v1.1: Etapa 2-A adicionada — reconciliação
  com ROADMAP antes da redação do relatório narrativo. Etapas 3 e 4 atualizadas
  para incluir validação e atualização do ROADMAP.
- `ROADMAP.md`: W03 `wkf-registro-sessao` e P02 `hub-memoria` adicionados à
  Fase 4 como concluídos (drift corrigido). Fase 5 criada registrando esta
  correção estrutural. `wkf-iac-conformidade` renomeado para W04 no médio prazo
  (W03 já estava ocupado pelo wkf-registro-sessao).

### Corrigido
- Drift: ROADMAP não tinha instrução para registrar entregáveis não previstos —
  causava acúmulo silencioso de histórico incompleto. Causa raiz corrigida
  na S04 (Verificação 5-A) e no W03 (Etapa 2-A).

---

## [2.9] — 2026-06-04

### Adicionado / Melhorado
- `hub-fonte/CONTEXTO.md` v2.1→v2.2: seção "Taxonomia e Glossário — distinção
  essencial" adicionada com exemplos concretos, tabela de coexistência e regra
  de uso para agentes de IA. Elimina ambiguidade histórica entre M01 e M02.
- `mat-saude-digital-taxonomia/README.md` v1.0→v1.1: reescrito com preâmbulo
  explicativo, distinção vs. glossário com exemplo prático (Interoperabilidade),
  guia de uso para classificação e regra para agentes de IA.

---

## [2.8] — 2026-06-04

### Adicionado
- `hub-fonte/GLOSSARIO.md` v1.5→v1.6: 5 novas categorias com 32 termos.
  Cat. 13 — Monitoramento e Inteligência Organizacional (8 termos, com
  pergunta orientadora por tipo). Cat. 14 — Análise de Dados e BI (6 termos).
  Cat. 15 — Gestão Orientada a Dados (5 termos). Cat. 16 — Arquitetura de
  Dados (5 termos). Cat. 17 — Conceitos Proprietários do Ecossistema (8 termos
  de autoria DTD/SETIS: Radar Institucional, Mapa Cognitivo Institucional,
  Sistema de Consciência Situacional, Ativo Informacional, Memória Institucional,
  Conhecimento Operacional, Conhecimento Estratégico, Observabilidade
  Organizacional). Índice Alfabético Unificado atualizado: 62 → 91 entradas.

---

## [2.7] — 2026-06-04

### Adicionado
- `hub-fonte/GLOSSARIO.md` v1.4→v1.5: Parte II — Saúde Digital incorporada com
  26 termos normativos (Cat. 9–12) extraídos do corpus documental do D01 via
  NotebookLM. Criada Cat. 13 (Monitoramento e Inteligência Organizacional) como
  placeholder. Índice Alfabético Unificado com 62 entradas adicionado.

### Corrigido / Adaptado
- Termo "Auditabilidade" renomeado para "Auditabilidade de IA" (Cat. 11) para
  evitar ambiguidade com "Auditoria de glossário" (Cat. 5). Cross-references
  cruzados entre as duas entradas. Decisão aprovada pelo mantenedor.

### Regra implementada
- Análise de conflitos de terminologia passa a ser etapa obrigatória antes de
  qualquer complementação, modificação ou correção do GLOSSARIO.md. Conflitos
  identificados devem ser alertados ao mantenedor antes da execução.

---

## [2.6] — 2026-06-04

### Adicionado
- `skl-briefing-saude-digital` (S07, público): skill de briefing periódico de saúde digital
  para o Diretor de Transformação Digital. Formaliza no ecossistema uma skill que existia apenas
  no projeto Claude — cobrindo monitoramento de notícias, regulações, mercado e tecnologia,
  com classificação taxonômica via M02, gestão de histórico contínuo e formato mobile-first.

### Corrigido
- `hub-entrada/README.md`: diagrama ASCII e tabelas corrigidos — nomes de repositórios
  atualizados para o padrão atual (`skl-`, `wkf-`, `hub-`); seção Agendas (A01) adicionada
  (ausente desde o CHANGELOG [2.3]); S07 incluído.
- `hub-fonte/sumario.md` v1.9→v2.0: tabela de Links rápidos corrigida — duplicatas removidas,
  todos os 18 repositórios ativos listados com ID, tipo e visibilidade.

---

# CHANGELOG — Ecossistema DTD/SETIS

Histórico cronológico de tudo que foi construído.
Entrada mais recente no topo.

---

## [2.9] — 2026-06-04

### Alterado (refatoração estrutural de nomenclatura)
- **17 repositórios renomeados** para novo padrão de prefixos de tipo:
  - `hub-` : infraestrutura do ecossistema (entrada, fonte, memória)
  - `mat-` : matrizes de conhecimento
  - `doc-` : acervos documentais
  - `skl-` : skills
  - `wkf-` : workflows
  - `agd-` : agendas
  - `prj-` : projetos
- `hub-fonte/nomenclatura.md` → v1.1: Seção 1 reescrita com tabela de prefixos
  obrigatórios, exemplos e regras; revoga convenção anterior que proibia prefixos
- Todas as referências internas atualizadas: `sumario.md`, `CONTEXTO.md`,
  `ONBOARDING.md`, `README.md`, `ROADMAP.md`, `CHANGELOG.md` e 5 `SKILL.md`

**Motivação:** navegação no GitHub era difícil com 17 repositórios sem sinalização
visual de tipo. Prefixo de 3 letras resolve triagem imediata e agrupamento
alfabético natural. Decisão tomada após análise comparativa com sistema de
ficheiros do mantenedor e diagnóstico de que o item 4 (ausência de pistas de tipo)
era o maior problema de navegação.


## [2.8] — 2026-06-03

### Atualizado
- `ecossistema-sumario/CONTEXTO.md` → v2.0 (MAJOR): reescrita completa.
  Removidos todos os elementos transitórios acumulados desde maio/2026 —
  datas de reunião, processos SEI, versões específicas de documentos,
  próximos passos e tokens. Adicionada mensagem de boas-vindas do mantenedor
  para colaboradores e agentes externos. Estrutura de repositórios atualizada
  com os 15 repositórios ativos em 6 tipos (M, S, D, W, A, P). ONBOARDING.md
  registrado nos arquivos obrigatórios do M01.
- `ecossistema-sumario/sumario.md` → v1.9: M01 atualizado para v0.24.
- `ecossistema-sumario/backlog-versoes.md`: entrada v0.24 registrada.

---

## [2.7] — 2026-06-03

### Adicionado
- `ecossistema-sumario/ONBOARDING.md` (v1.0): porta de entrada para agentes de IA
  e colaboradores externos. Organiza o acesso ao ecossistema por propósito:
  A) entender o projeto, B) agente de IA iniciando sessão, C) executar tarefa
  específica, D) contribuir com o ecossistema. Cada propósito tem links diretos
  para os recursos corretos. Permite compartilhar um único link como ponto de
  entrada universal para o ecossistema.

### Atualizado
- `ecossistema-sumario/INDICE.md`: ONBOARDING.md adicionado à tabela de arquivos
- `ecossistema-sumario/sumario.md` → v1.8: M01 atualizado para v0.23
- `ecossistema-sumario/backlog-versoes.md`: entrada v0.23 registrada

---

## [2.6] — 2026-06-03

### Corrigido
- `dtd-setis/README.md`: atualizado com estado completo do ecossistema derivado
  do `sumario.md` v1.6 — diagrama ASCII com 4 camadas e todos os tipos (M, S, D, W, A, P);
  tabela de repositórios expandida de 4 para 15 entradas organizadas por tipo (M, S, D, W, P);
  seção de navegação com orientação de leitura ("Leia primeiro"). Correção de drift
  acumulado desde as Fases 2, 3 e 4 do ecossistema (2026-06-01 a 2026-06-02).
- `dtd-setis/CHANGELOG.md`: cabeçalho de seção duplicado removido — o arquivo tinha
  o bloco de introdução repetido a partir da entrada [0.9], violando a convenção
  de entrada mais recente no topo.
- `skill-github-orquestracao/SKILL.md` → v2.1: Verificação 2 da Etapa 6 reescrita
  para comparação obrigatória contra o `sumario.md` (fonte de verdade) em vez de
  verificação auto-referencial da sessão atual; Erro #009 registrado com causa raiz
  e correção.
- `ecossistema-sumario/sumario.md` → v1.7: S04 atualizado de v2.0 para v2.1.

---

## [2.5] — 2026-06-02

### Adicionado
- `hub-memoria` (P02, privado): projeto que documenta a construção
  do ecossistema. Contém Resumo Executivo técnico completo (v1.0) e relatório
  narrativo da sessão fundacional de 2026-06-02 — história das decisões de
  design, percalços, soluções e aprendizados. O projeto que deveria ter sido P01.
- `wkf-registro-sessao` (W03, público): workflow de registro estruturado
  de sessões de trabalho intensivo — distinto do W02 (reuniões). Documenta
  como preservar a história de construção de sistemas em sessões de IA.

### Atualizado
- `ecossistema-sumario/sumario.md` → v1.6: P02 e W03 registrados
- `ecossistema-sumario/CONTEXTO.md` → v1.8: P02 e W03 adicionados
- `dtd-setis/projetos/monitoramento.md`: ecossistema adicionado como projeto ativo

---

## [2.4] — 2026-06-02

### Corrigido (saneamento de drifts — causa raiz: S04 sem cobertura de arquivos centrais)
- `ecossistema-sumario/CONTEXTO.md` → v1.7: versões de todos os componentes
  sincronizadas com `sumario.md` (fonte de verdade); M01 e S04 estavam com
  versões de meses atrás
- `ecossistema-sumario/sumario.md` → v1.5: duplicações textuais removidas
  (S05/S06 e W01/W02 tinham descrições contaminadas); S04 atualizado para v1.8
- `docs/arquitetura.md` → v2.0: reescrita completa — descreve os 6 tipos
  (M, S, D, W, A, P), 4 camadas, relações entre tipos e papel da S04;
  versão anterior (v1.0) descrevia arquitetura de 3 camadas sem W, A, D01
- `ROADMAP.md`: reorganizado em 5 seções (concluído / em andamento / próxima
  ação / médio prazo / longo prazo); doc-governanca-ses-df e todos os entregáveis
  de 2026-06-02 marcados como ✅
- `INDICE.md`: data, contagem de arquivos e referência a arquitetura.md v2.0
  atualizados
- `backlog-versoes.md`: entradas retroativas v1.1–v2.0 adicionadas — histórico
  completo do portfólio desde a fundação

### Atualizado (blindagem estrutural)
- `skl-github-orquestracao` → v1.8: Verificação 5 (consistência cruzada
  obrigatória entre sumario × CONTEXTO × README × ROADMAP × arquitetura);
  OP-C recebe CONTEXTO.md; OP-W e OP-AG recebem ROADMAP.md e arquitetura.md;
  Erro #007 documentado com causa raiz e correção

---

## [2.3] — 2026-06-02

### Adicionado
- Tipo A (Agenda) ao ecossistema: primeiro tipo indexado por tempo de ocorrência
  — não por ordem de criação. Repositórios `agenda-[unidade]` contêm acervos
  cronológicos de registros de reunião com estrutura `reunioes/AAAA/MM/` e
  campos distintos `data_reuniao` / `data_registro`.
- `agd-dtd` (A01, privado): acervo institucional de reuniões da DTD.
- `wkf-registro-reuniao` (W02, privado): memória organizacional do processo
  de transformação de gravações em registros formais — inclui histórico de
  problemas P01-P03 e roadmap de automação com integração SEI.
- `skl-registro-reuniao` (S06, público): skill que formaliza o prompt
  institucional desenvolvido com o PLAUD NOTE Pro — 5 etapas, 8 seções
  obrigatórias, depósito automático via S04.
- `skl-github-orquestracao` → v1.7: OP-AG adicionado com lógica específica
  de indexação cronológica do tipo A.

### Atualizado
- `ecossistema-sumario/nomenclatura.md` → v1.0: marco — Seção 4-C tipo A,
  Seção 7.6, indexação cronológica, campos data_reuniao/data_registro
- `ecossistema-sumario/sumario.md` → v1.3: tipo A, A01, S06, W02
- `ecossistema-sumario/GLOSSARIO.md` → v1.4: Categoria 8 com 6 termos
- `ecossistema-sumario/CONTEXTO.md` → v1.6: S06, W02, A01

---

## [2.2] — 2026-06-02

### Adicionado
- `wkf-transcricao-documental` (W01, público): primeiro repositório do
  tipo Workflow (W) no ecossistema. Contém o WORKFLOW.md com 8 seções
  obrigatórias — missão, estado final esperado, etapas, skills consumidas,
  histórico de problemas, roadmap de automação — e pasta `execucoes/` para
  logs de execução. O tipo W nasce para preservar o capital organizacional
  da DTD: workflows escritos, versionados e consultáveis por humanos e IA.
- `telessaude-poc-prisional/EXECUCOES.md`: registro retroativo dos workflows
  acionados no P01, com nota sobre registros anteriores ao tipo W.

### Atualizado
- `ecossistema-sumario/nomenclatura.md` → v0.9: Seção 4-B (estrutura tipo W),
  Seção 7.5 (backlog tipo W), WORKFLOW.md e EXECUCOES.md na tabela de arquivos
- `ecossistema-sumario/sumario.md` → v1.2: seção Workflows (W) criada; W01 registrado
- `ecossistema-sumario/GLOSSARIO.md` → v1.3: Categoria 7 com 5 termos
  (workflow, subprocesso, log de execução, estado final esperado, EXECUCOES.md)
- `ecossistema-sumario/CONTEXTO.md` → v1.5: W01 nos repositórios ativos
- `skl-github-orquestracao` → v1.6: OP-W adicionado; EXECUCOES.md na OP-P
- `dtd-setis/README.md`: diagrama ASCII e tabela com tipo W e W01

---

## [2.1] — 2026-06-02

### Atualizado
- `ecossistema-sumario/GLOSSARIO.md` → v1.2: Categoria 6 adicionada —
  Pipeline de Transcrição Documental. 4 novos termos definidos:
  "artefato de extração", "front matter YAML", "pipeline de transcrição"
  e "reflow". Total do glossário: 29 termos em 6 categorias.
  Primeiro ciclo de expansão por domínio técnico novo incorporado ao
  ecossistema (D01/S05).

---

## [2.0] — 2026-06-02

### Adicionado
- `doc-governanca-ses-df` (D01, público): primeiro repositório do tipo Documento
  no ecossistema. Contém 28 documentos transcritos em Markdown sobre saúde
  digital — 18 regulamentações nacionais (legislação federal, distrital,
  portarias ministeriais, resoluções CFM e ANVISA) + 10 referências
  internacionais bilíngues EN+PT. Estrutura com 6 subpastas + WORKFLOW-
  ESPECIFICACAO.md v1.1 (8 problemas documentados, protocolo de exceção,
  roadmap de automação).
- `skl-transcricao-documental` (S05, público): pipeline de transcrição
  documental formalizado como skill do ecossistema — 7 etapas, auto-
  verificação programática, protocolo de exceção §3.1.

### Regularizado
- `mat-cadastro-ses-setis-dtd` (D02): repositório existente sem estrutura
  padrão — adicionados INDICE.md, backlog-versoes.md e ficha técnica.
  Registrado formalmente como D02 no sumário.
- `skl-iac-pdtic` (S02): estava ativo mas não registrado no sumário.
  Regularizado como S02 v2.0.

### Atualizado
- `ecossistema-sumario/sumario.md` → v1.1: seção Documentos (D) preenchida
  pela primeira vez; D01, D02, S05, S02 registrados
- `ecossistema-sumario/CONTEXTO.md` → v1.4: D01, D02, S05 nos repositórios ativos

---

## [1.9] — 2026-06-01

### Atualizado
- `ecossistema-sumario/GLOSSARIO.md` → v1.1: primeiro ciclo completo do
  mecanismo de manutenção automática do glossário — a Verificação 4 da S04
  identificou seus próprios termos como candidatos na operação de criação,
  e eles foram adicionados imediatamente. "Auditoria de glossário" e
  "termo candidato" agora têm definições formais.

---

## [1.8] — 2026-06-01

### Atualizado
- `skl-github-orquestracao` → v1.5: Verificação 4 adicionada à Etapa 6
  da S04 — auditoria obrigatória de termos novos ao final de cada operação,
  com comparação ao GLOSSARIO.md e proposta de atualização antes do
  encerramento. O GLOSSARIO.md criado em [1.7] passa a ter mecanismo
  automático de manutenção. Campo "Glossário verificado" adicionado ao
  relatório padrão da Etapa 7.

---

## [1.7] — 2026-06-01

### Adicionado
- `ecossistema-sumario/GLOSSARIO.md` (v1.0): glossário formal do ecossistema
  com 18 termos em 5 categorias — tipos de repositório, arquivos obrigatórios,
  instrumentos institucionais, operações/versionamento, conceitos de qualidade.
  Implementação identificada como essencial em sistema maduro.

### Atualizado
- `ecossistema-sumario/sumario.md` → v1.0: marco de maturidade do M01;
  GLOSSARIO.md registrado; S04 atualizado para v1.4
- `ecossistema-sumario/nomenclatura.md` → v0.8: referência ao GLOSSARIO.md
- `skl-github-orquestracao` → v1.4: INDICE.md adicionado às checklists
  OP-B, OP-C, OP-D, OP-E e OP-F (instrução condicional); Erro #006 incorporado

---

## [1.6] — 2026-06-01

### Adicionado
- `INDICE.md` criado em todos os repositórios públicos do ecossistema
  (M01, M02, S01, S03, S04, dtd-setis): navegação local padronizada que
  permite chegar a qualquer recurso sem leitura exaustiva do repositório

### Atualizado
- `README.md` de todos os repositórios públicos: link para INDICE.md adicionado
- `dtd-setis/README.md`: seção de navegação simplificada apontando para INDICE.md
- `ecossistema-sumario/nomenclatura.md` → v0.7: Seção 10 — INDICE.md obrigatório
  em todos os repositórios sem exceção
- `skl-github-orquestracao` → v1.3: OP-E com critério objetivo, INDICE.md
  nas checklists OP-A e OP-P, Erro #005 incorporado

---

## [1.5] — 2026-06-01

### Atualizado
- `skl-github-orquestracao` → v1.2: segundo ciclo de aprendizado
  contínuo na mesma sessão de criação — Erro #004 incorporado.
  Verificação de backlog agora aceita '## v' e '### v' como padrões
  válidos, eliminando falsos positivos em repositórios com subseções.
- `ecossistema-sumario/sumario.md` → v0.8: S04 atualizado para v1.2

---

## [1.4] — 2026-06-01

### Corrigido
- `README.md`: instrução obrigatória de inicialização adicionada ao topo —
  Claude deve ler o CONTEXTO.md do hub-fonte antes de qualquer ação;
  resolve falha crítica de navegação identificada no diagnóstico de maturidade

### Adicionado
- `backlog-versoes.md`: criado com histórico retroalimentado desde v0.5;
  corrige violação da nomenclatura.md (arquivo obrigatório ausente)

### Atualizado (em ecossistema-sumario)
- `protocolo-atualizacoes.md` → v2.0: descontinuado formalmente em favor da S04;
  conteúdo original preservado para rastreabilidade histórica
- `sumario.md` → v0.7: versão do M01 corrigida de v0.11 para v0.14

---

## [1.3] — 2026-06-01

### Atualizado
- `skl-github-orquestracao` → v1.1: primeiro ciclo completo de aprendizado
  contínuo da skill — Erro #003 identificado, corrigido e registrado na mesma
  sessão de criação. Python urllib definido como padrão obrigatório para chamadas
  à API GitHub; funções helper (api_put, api_get) documentadas na Etapa 5 da skill.
- `ecossistema-sumario/sumario.md` → v0.6: S04 atualizado para v1.1

---

## [1.2] — 2026-06-01

### Atualizado
- `ecossistema-sumario/CONTEXTO.md` → v1.3: adição do protocolo obrigatório
  para operações no GitHub com duas regras:
  - **Regra 1 — Autodescoberta:** o Claude aciona a S04 automaticamente ao
    identificar operações no GitHub, sem depender da memória do usuário
  - **Regra 2 — Aprendizado contínuo:** todo erro, aprendizado ou melhoria
    identificado na sessão atualiza a S04 antes do encerramento, garantindo
    que o ecossistema evolua a cada operação

---

## [1.1] — 2026-06-01

### Adicionado
- Repositório público `skl-github-orquestracao` (S04): skill de orquestração
  do ecossistema DTD/SETIS. Garante que toda operação no GitHub atualize todos
  os arquivos afetados — opera em duas fases separadas por aprovação explícita
  (planejamento sem token → aprovação → execução com token). Incorpora registro
  permanente de erros aprendidos que viram verificações adicionais.

### Atualizado
- `dtd-setis/README.md`: diagrama ASCII, tabela de repositórios e seção
  "Como utilizar as skills" atualizados com S04
- `ecossistema-sumario/sumario.md` → v0.5: S04 registrado
- `ecossistema-sumario/CONTEXTO.md` → v1.2: S04 adicionado

---

## [1.0] — 2026-06-01

### Adicionado
- Pasta `projetos/` com `README.md` e `monitoramento.md`: monitoramento público
  de projetos da DTD/SETIS/SES-DF; visão panorâmica curada para audiência externa;
  documentação técnica interna mantida em repositórios privados separados
- Repositório privado `prj-telessaude-poc-prisional` (P01): primeiro projeto formal
  do ecossistema, documentando a PoC do Totem Health360 no Sistema Prisional do DF

### Atualizado
- `ecossistema-sumario/nomenclatura.md` → v0.6: criação do tipo P (Projetos)
  com Seção 4-A (estrutura interna), Seção 7.4 (extensões de backlog) e
  política de visibilidade pública/privada
- `ecossistema-sumario/sumario.md` → v0.4: seção "Projetos (P)" adicionada;
  P01 registrado; tabela de links rápidos com coluna de visibilidade
- `dtd-setis/README.md` → v1.0: diagrama ASCII atualizado com tipo P;
  tabela de repositórios atualizada com P01

---


## [0.9] — 2026-05-29

### Atualizado
- `ecossistema-sumario/CONTEXTO.md` -> v1.1: separação entre contexto durável e estado operacional transitório; tabela de repositórios completada com a skill S03 (skill-poc-saude-digital) e com o repositório-mãe (dtd-setis)
- `ecossistema-sumario/nomenclatura.md` -> v0.5: arquivos obrigatórios do M01 completados; backlog de ações da DTD documentado
- `ecossistema-sumario/sumario.md` -> v0.3: hub-entrada registrado; versão do M01 reconciliada para v0.10

### Adicionado
- `ecossistema-sumario/backlog-acoes-dtd.md`: histórico retrospectivo de ações e produtos da DTD — fonte única para relatórios de atividade consolidados

### Corrigido
- Drift de índices: S03 e hub-entrada ausentes do sumário/contexto; versão do M01 desalinhada (índices em v0.5, backlog em v0.9) -> reconciliada para v0.10

---

## [0.8] — 2026-05-28

### Adicionado
- `protocolo-atualizacoes.md` criado no ecossistema-sumario: documento de referência
  com protocolo obrigatório de encerramento para qualquer operação no ecossistema.
  Define 6 tipos de operação (OP-A a OP-F) com checklists específicas e modelo de
  relatório de encerramento. Candidato a skill autônoma quando a lógica estiver madura.

---

## [0.7] — 2026-05-28

### Adicionado
- Repositório público `skl-poc-saude-digital` (S03) incorporado ao ecossistema
- Padrão de PoC em Saúde Digital formalizado como skill: 11 seções obrigatórias,
  protocolo de governança, análise normativa e instrumentos jurídicos
- Baseado na PoC MedNear, caso zero do Marco Regulatório Interno de PoCs da SES-DF
- `sumario.md` do hub-fonte estruturado pela primeira vez (v0.2)

---

## [0.6] — 2026-05-27

### Adicionado
- Repositório público `hub-entrada` como repositório mãe do ecossistema
- `README.md` com apresentação pública e portfólio da DTD
- `MANIFESTO.md` com propósito, visão, objetivos e princípios
- `ROADMAP.md` com planejamento das próximas entregas
- `CHANGELOG.md` (este arquivo)
- `DECISOES.md` com registro das grandes decisões do projeto
- `docs/arquitetura.md` com descrição técnica do ecossistema
- `CONTEXTO.md` no `hub-fonte` para inicialização rápida de sessões

### Atualizado
- `skl-iac-pdtic` → v2.0: adição do modo IAC-H, governança SES-DF,
  regras de linguagem institucional, protocolo de 7 etapas
- `ecossistema-sumario/sumario.md` → v0.5: modelo IAC documentado,
  skl-iac-pdtic registrada como v2.0
- `ecossistema-sumario/nomenclatura.md` → v0.3: seção 8 adicionada
  (Modelo IAC como padrão do ecossistema)
- `ecossistema-sumario/README.md`: instrução de nova sessão adicionada

---

## [0.5] — 2026-05-27

### Adicionado
- **IAC-V v0.2** — Instrumento de Análise Comparativa Vertical
  "Análise de Revisão do PDTIC 2024-2027" (PDTIC v1.5 → v1.8)
  Distribuído aos membros do SGTD para reunião de 11/06/2026
- **IAC-H v0.1** — Instrumento de Análise Comparativa Horizontal
  "Análise de Conformidade: PDTIC v1.8 × PTD-SES 2024-2027"
  Índice de alinhamento global: 69% — Parecer: CONFORME COM RESSALVAS
  8 conv
