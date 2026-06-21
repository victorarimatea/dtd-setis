# Staging Area — DTD/SETIS/SES-DF

**Repositório:** hub-entrada
**Mantenedor:** victorarimatea
**Alimentado por:** S04 `skl-github-orquestracao` (registros automáticos), Etapa 6-A (ideias mineradas e conhecimentos consolidados)
**Processado por:** W04 `wkf-roadmap-geral` — sessões de sexta-feira à tarde

> Este arquivo NÃO contém informações oficiais do ROADMAP.
> Tudo aqui aguarda processamento e decisão do mantenedor.
> Nenhum item é deletado — itens processados vão para a Seção D.

---

## Painel de Situação

> **Instrução para agentes de IA:** este painel é calculado dinamicamente
> a cada leitura. Nunca edite números manualmente — conte as entradas
> das tabelas de cada seção e calcule os totais no momento da leitura.
> Isso elimina por design qualquer possibilidade de drift entre o painel
> e o estado real das seções.

| Seção | Tipo | Pendentes | Maturando | Aprovadas/Registradas | Arquivadas |
|---|---|---|---|---|---|
| A | Registros automáticos (S04) | [contar linhas da tabela sem status "processado"] | — | — | — |
| B | Ideias sinalizadas | [contar status `pendente`] | [contar status `maturando`] | [contar status `aprovada`] | [contar status `arquivada`] |
| C | Ideias mineradas | [contar status `pendente`] | [contar status `maturando`] | [contar status `aprovada`] | [contar status `arquivada`] |
| E | Conhecimentos consolidados | [contar status `pendente`] | — | [contar status `registrado`] | [contar status `arquivado`] |

### Alertas — avaliar a cada leitura

**⚠️ Alerta de acúmulo:**
Some os pendentes das Seções B + C + E.
Se o total for ≥ 5: emitir recomendação ativa ao mantenedor para considerar
sessão dedicada ao roadmap (W04) ou ao hub-aprendizagem, conforme predominância
do tipo de item acumulado.

**⏰ Alerta de hiato de roadmapping:**
Confrontar a data atual com a data da entrada mais recente na Seção D
(coluna "Data decisão"). Se o intervalo for > 7 dias: alertar o mantenedor
que a última sessão de roadmapping foi há mais de uma semana e recomendar
agendamento. Este alerta é ativado por presença humana — não é agendado
autonomamente.

### Legenda de marcações do sistema (para agentes e LLMs)

> **Esta seção é de leitura obrigatória para qualquer agente que opere neste repositório.**
> Ela define as convenções ativas do ecossistema ATLAS — incluindo elementos
> em experimentação que devem ser reportados ao final de cada sessão.

| Marcação | Significado | Comportamento esperado do agente |
|---|---|---|
| 🔒 | Interno — relevância de rastreabilidade | Registrar normalmente |
| 📊 | Estratégico — valor narrativo para SETIS | Destacar em resumos executivos |
| 🌐 | Público — comunicável externamente | Incluir em materiais de divulgação |
| 🧪 | Em teste — experimentação ativa, não vinculante | **Ver instrução abaixo** |

**Instrução para elementos 🧪 (em teste):**
Elementos marcados com 🧪 são experimentações ativas do ecossistema. Eles:
- **Não bloqueiam** nenhuma operação — são orientativos, nunca determinativos
- **Não são gravados** como artefatos — são calculados na leitura
- **Devem ser reportados** ao final de toda sessão: o agente lista os elementos 🧪
  encontrados e faz nota rápida — "seguem em teste sem atrito" ou "elemento X
  mostrou comportamento Y"
- **São validados formalmente** em sessões W04 com um de três vereditos:
  `validar` (promove a definitivo) · `ajustar` (mantém em teste com mudança) · `descartar` (remove)

**Critério de saída do estado 🧪:** validação formal em W04, baseada em
comportamento observado em sessões reais. Sem prazo fixo — a prática calibra.

---

## Seção A — Registros automáticos (S04)

*Entregáveis implementados no ecossistema aguardando curadoria no ROADMAP.*
*Alimentado pela S04 ao final de cada operação.*

| Data | Entregável | Tipo | Repositório | Depositado por |
|---|---|---|---|---|

---

## Seção B — Ideias sinalizadas

*Ideias capturadas por sinalização explícita do mantenedor durante sessões.*

| Data | Hora | Autor | Ideia | Contexto de origem | Status |
|---|---|---|---|---|---|
| — | — | — | — | — | — |

---

## Seção C — Ideias mineradas (aguardam validação)

### Por que esta seção existe

Boas ideias raramente chegam com aviso prévio. Elas surgem nas interlinhas
de uma conversa técnica, num comentário lateral durante uma implementação,
numa frase que começa com "seria interessante se..." no meio de uma sessão
sobre outra coisa. Se nenhum mecanismo as captura naquele momento, elas se
perdem nos textos de dezenas de conversas ao longo do tempo.

Esta seção existe para que isso não aconteça. O agente de IA — operando como
minerador ativo de contexto — varre o histórico de cada sessão em busca de
manifestações que têm características de ideia embrionária. Ele não espera
que o mantenedor lembre de sinalizar. Ele busca, apresenta os candidatos,
aguarda validação, e só então elabora e registra formalmente.

---

### Instrução para agentes de IA — mineração ativa de contexto

**Quando executar:** ao final de qualquer sessão que resulte em plano de ação
de edição de repositórios ou documentações. A mineração ocorre antes do
relatório de encerramento, ainda com o contexto completo da conversa disponível.

**O que fazer, passo a passo:**

**Passo 1 — Varredura do histórico**
Reler o histórico completo da conversa. Não apenas as decisões formais —
incluir comentários laterais, frases exploratórias, problemas identificados
ao longo do caminho.

**Passo 2 — Aplicação dos critérios de elegibilidade**
Para cada trecho candidato, aplique as perguntas orientadoras abaixo.
Um candidato é elegível se responder afirmativamente a pelo menos duas:

| # | Pergunta orientadora | Sinal típico no texto |
|---|---|---|
| 1 | O mantenedor identificou um problema recorrente ou uma lacuna no ecossistema? | *"ainda não temos..."*, *"falta um..."*, *"o problema é que..."* |
| 2 | O mantenedor expressou uma hipótese sobre algo que poderia existir? | *"seria interessante se..."*, *"imagino que..."*, *"poderia ser..."* |
| 3 | O mantenedor fez uma comparação com uma referência externa? | *"como fazem em..."*, *"seria como um..."*, *"semelhante ao..."* |
| 4 | O mantenedor formulou uma pergunta estratégica sem respondê-la? | *"e se..."*, *"por que não..."*, *"o que aconteceria se..."* |
| 5 | O mantenedor expressou um desejo ou intenção não convertida em ação? | *"quero pensar mais sobre..."*, *"no futuro..."*, *"seria bom ter..."* |
| 6 | O mantenedor nomeou algo que não existe ainda mas que faria sentido existir? | Substantivo novo seguido de descrição funcional |
| 7 | O Claude identificou uma implicação estratégica não explorada na conversa? | Conexão entre dois pontos que o mantenedor não conectou explicitamente |

**Passo 3 — Apresentação dos candidatos**
Para cada candidato elegível, apresente ao mantenedor antes de registrar:

```
💡 Ideia candidata identificada:
"[trecho ou paráfrase do que foi dito]"

Pergunta orientadora ativada: [número e texto da pergunta]
Contexto: [em que momento da conversa surgiu]

Você gostaria de registrar isso como ideia na staging area?
```

Aguarde confirmação. Não registre sem aprovação explícita do mantenedor.

**Passo 4 — Elaboração para registro**
Após confirmação, elabore a ideia com nome descritivo, problema que resolve,
área do ecossistema relacionada, linguagem objetiva.

**Passo 5 — Depósito na tabela**
Registre com todos os campos preenchidos. Status inicial: `pendente`.

**Passo 6 — Rascunho (quando elegível)**
Criar rascunho MD em `hub-entrada/rascunhos-staging/AAAA-MM-DD-[slug].md` quando
a conversa de origem contiver pelo menos um dos seguintes: (a) raciocínio de
design com alternativas consideradas; (b) implicações mapeadas em outros
repositórios ou workflows; (c) protótipo ou esboço de solução; (d) discussão
com mais de 3 trocas substantivas sobre a ideia. Caso contrário, a linha da
tabela é suficiente. Preencher coluna `Rascunho` com nome do arquivo ou `—`.

**Atualização de rascunho existente (sessões futuras):**
Se a ideia já tem rascunho e novo material rico surgiu: abrir o arquivo e
adicionar seção `## Atualização AAAA-MM-DD` ao final, preservando histórico.
O rascunho é vivo enquanto a ideia está pendente ou maturando.

---

### Tabela de ideias mineradas

| Data | Conversa de origem | Ideia candidata | Pergunta orientadora ativada | Validada pelo mantenedor | Rascunho | Status | Aguardando desde |
|---|---|---|---|---|---|---|---|
| 2026-06-21 | Sessão operacional 2026-06-21 — S05 v1.1 + D01 v1.1 | **Retry/backoff no CONFIRMAR pós-PUT** — o delay fixo de 3s pós-PUT da S04 v2.10 (Erro #015) mostrou-se insuficiente em pelo menos uma escrita desta sessão (SKILL.md: CONFIRMAR inicial falhou; passou com ~8s acumulados). Um valor fixo de 3s é frágil para escritas grandes ou sob carga; retry com backoff progressivo (ex: 3s → 5s → 8s) seria mais robusto sem aumentar latência média. Pode ser incorporado à S04 como ajuste do Erro #015 ou como refinamento operacional independente. | #1, #4 | ✅ confirmado | — | ⏳ pendente | 2026-06-21 |
| 2026-06-15 | W04 sessão 2 — curadoria da staging area | **Processo de curadoria longitudinal para o hub-aprendizagem** — processo dedicado (distinto do W04 regular) para avaliar quando um documento do hub-memoria está maduro para se tornar capítulo do hub-aprendizagem. Requer leitura cruzada do hub-memoria, acervo de relatórios de sessão (P02) e ROADMAP/CHANGELOG para triangular maturidade real. Periodicidade provável: trimestral ou semestral. Insumos: (1) hub-memoria — quais documentos existem, em que estado; (2) relatórios P02 — quantas vezes o conceito foi referenciado em sessões distintas; (3) ROADMAP — o conceito virou estrutura real implementada em múltiplos repositórios? Derivado da formalização do fluxo rascunhos-staging (C2). | #4, #7 | ✅ confirmado | — | ⏳ pendente | 2026-06-15 |
| 2026-06-15 | W04 sessão 2 — C7 ATLAS / mecanismo em teste | **Governança da inovação via estado `em teste` (🧪)** — categoria formal de experimentação reversível: não-vinculante (nada em teste bloqueia ou corrompe operação), rastreável (token 🧪 greppável por varredura), com critério de saída explícito (validar/ajustar/descartar em W04). Rito em dois tempos: leve no W06 (listar elementos 🧪 e notar comportamento) e profundo no W04 (veredito formal). Registrado no W03. O próprio mecanismo nasce marcado 🧪. Pré-requisito: bloco-para-agentes no README (ver próximo item). | #6, #7 | ✅ confirmado | — | ⏳ pendente | 2026-06-15 |
| 2026-06-15 | W04 sessão 2 — C7 ATLAS / mecanismo em teste | **Bloco-para-agentes no README** — convenção nova de arquivo obrigatório: toda seção README dos repositórios ganha um bloco voltado a LLMs com legenda das marcações do sistema (🔒📊🌐🧪) e instrução sobre como se comportar frente a cada uma, especialmente 🧪. Auditada pela W05 (todo README tem o bloco?). Formalizada no M01/nomenclatura.md. Solução para a ausência de ponto de entrada único no ecossistema: a entrada é por repositório, e é o README. Inaugural: `hub-entrada/staging.md` já contém o bloco na Seção de Painel. | #1, #6 | ✅ confirmado | — | ⏳ pendente | 2026-06-15 |
| 2026-06-04 | Sessão de criação do W04 | Estrutura formal de perfis de acesso do ecossistema — define quem pode visualizar, editar e criar em cada repositório; base para governança multiusuário | #1 — lacuna identificada | ✅ confirmado | — | maturando | 2026-06-04 |
| 2026-06-04 | Sessão de criação do W04 | Família de workflows derivados do W04 para projetos específicos — `wkf-roadmap-telessaude`, `wkf-roadmap-pdtic` e outros, sem alterar o W04 base | #6 — nomeação de algo que não existe | ✅ confirmado | — | maturando | 2026-06-04 |
| 2026-06-06 | Fechamento sessão 2026-06-06 — visão de Victor | Antecipar cenário multi-contribuidor: campos autor/revisor nas entradas de backlog | Visão de longo prazo de Victor | ✅ confirmado | — | maturando | 2026-06-06 |
| 2026-06-07 | Sessão de design do wiki-ecossistema | Definir a anatomia do cabeçalho de metadados de documento normativo (YAML frontmatter) | #1 e #2 | ✅ confirmado | — | maturando | 2026-06-07 |
| 2026-06-07 | Sessão de design do wiki-ecossistema | Workflow de ingestão assistida de norma (N1) — ao subir documento novo, gera relatório de impacto | #1 e #6 | ✅ confirmado | — | maturando | 2026-06-07 |
| 2026-06-07 | Sessão de design do wiki-ecossistema | Workflow de vigília de conformidade (N2) — cruza a base: lei federal nova → portarias/normas locais potencialmente desatualizadas | #1 e #4 | ✅ confirmado | — | maturando | 2026-06-07 |
| 2026-06-07 | Sessão de design do wiki-ecossistema | Template padronizado de página-tema do wiki | #6 e #1 | ✅ confirmado | — | maturando | 2026-06-07 |
| 2026-06-11 | Sessão de design do ciclo de sessão | Memória de domínio do briefing de saúde digital — cada acionamento do briefing deposita registro datado do que viu (classificado pela `taxonomia-saude-digital`); o acervo vira consultável, aplicando "conhecimento como query" (cap-03) a conteúdo noticioso. Três usos: anti-repetição, curva de destaque temporal, staging de investigação. PRIMEIRA categoria de registro de CONTEÚDO/domínio. Notas de design: (1) lar próprio a definir — provavelmente vinculado à S07 ou repositório de acervo de briefings; (2) conexão com wiki-ecossistema camada C3 — acervo de briefings como matéria-prima para capítulos temáticos. | #2, #7 | ✅ confirmado | — | maturando | 2026-06-11 |
| 2026-06-11 | Sessão de design do ciclo de sessão | Contribuição externa via issues públicas — repositório público porta-de-entrada dedicado recebe sugestões sem acesso de escrita; fluxo: issue externa → triagem → staging interna. VIABILIDADE TÉCNICA CONFIRMADA. **Dependência declarada: aguarda definição da estrutura formal de perfis de acesso.** | #1, #6 | ✅ confirmado | — | maturando | 2026-06-11 |
| 2026-06-11 | Sessão de design do ciclo de sessão (anexo de amadurecimento) | Disciplina de Arquitetura do Conhecimento — terceira camada de governança ortogonal à auditoria: W05 verifica CONFORMIDADE; esta verifica SAÚDE ESTRUTURAL. Princípios qualificadores: complexidade, coesão, acoplamento, duplicação, fragmentação, ownership. **Ancorada sob ATLAS-moldura — sessão evolutiva própria prevista. Exercida na prática via eixos IS/RD do modelo de priorização 🧪.** | #1, #7 | ✅ confirmado | — | maturando | 2026-06-11 |

---

## Seção D — Arquivo histórico

*Ideias e registros já processados em sessões do W04.*
*Nunca deletados — o histórico de decisões tem valor institucional.*

| Data entrada | Data decisão | Item | Decisão | Motivo | Sessão | Rascunho |
|---|---|---|---|---|---|---|
| 2026-06-04 | 2026-06-08 | S04 v2.2 — Verificação 5-A: reconciliação obrigatória com ROADMAP | aprovado 🔒 | Maturidade interna — rastreabilidade | W04 sessão 1 | — |
| 2026-06-04 | 2026-06-08 | W03 v1.1 — Etapa 2-A: reconciliação com ROADMAP | aprovado 🔒 | Maturidade interna — rastreabilidade | W04 sessão 1 | — |
| 2026-06-04 | 2026-06-08 | W04 wkf-roadmap-geral v1.0 — criação do workflow de gestão de roadmap | aprovado 📊 | Narrativa estratégica para SETIS | W04 sessão 1 | — |
| 2026-06-04 | 2026-06-08 | staging.md — criação da staging area do ecossistema | aprovado 🔒 | Implementação técnica interna | W04 sessão 1 | — |
| 2026-06-05 | 2026-06-08 | S04 v2.5 — escala de severidade SEV1–SEV4 | aprovado 🔒 | Maturidade interna | W04 sessão 1 | — |
| 2026-06-05 | 2026-06-08 | S04 v2.6 — verificações embutidas CONFIRMAR | aprovado 🔒 | Maturidade interna | W04 sessão 1 | — |
| 2026-06-05 | 2026-06-08 | hub-aprendizagem v1.0 — repositório de memória intelectual criado | aprovado 📊 | Narrativa de valor para SETIS | W04 sessão 1 | — |
| 2026-06-05 | 2026-06-08 | S04 v2.7 — Etapa 6-A expandida com mineração de conhecimento consolidado | aprovado 🔒 | Maturidade interna | W04 sessão 1 | — |
| 2026-06-05 | 2026-06-08 | W03 v1.2 — Etapa 2-B: identificação de aprendizados consolidados | aprovado 🔒 | Maturidade interna | W04 sessão 1 | — |
| 2026-06-07 | 2026-06-08 | cap-03 hub-aprendizagem v1.1 — "Conhecimento como Query" + 5 ideias na staging | aprovado 📊 | Visão de longo prazo da camada de conhecimento | W04 sessão 1 | — |
| 2026-06-04 | 2026-06-08 | `wkf-resumo-executivo` (1ª e 2ª entradas — unificadas) | aprovado 📊 | Ativo estratégico permanente; médio prazo | W04 sessão 1 | — |
| 2026-06-13 | 2026-06-15 | PTD / PTD-SES | aprovado 🔒 | Definições formais pendentes no GLOSSARIO.md | W04 sessão 2 | — |
| 2026-06-13 | 2026-06-15 | SGTD | aprovado 🔒 | Definições formais pendentes no GLOSSARIO.md | W04 sessão 2 | — |
| 2026-06-13 | 2026-06-15 | CIG/SES | aprovado 🔒 | Definições formais pendentes no GLOSSARIO.md | W04 sessão 2 | — |
| 2026-06-13 | 2026-06-15 | Fórum de Subsecretários | aprovado 🔒 | Definições formais pendentes no GLOSSARIO.md | W04 sessão 2 | — |
| 2026-06-13 | 2026-06-15 | CONFIRMAR com delay mínimo 3s — S04 Etapa 5 | aprovado 🔒 | Formalizar sub-passo pós-PUT na S04 | W04 sessão 2 | — |
| 2026-06-13 | 2026-06-15 | Simplificação do modelo de propagação de versões — source-only | aprovado 🔒 — design fechado, execução dedicada | Decisão: versão vive na ficha técnica do arquivo; sumario.md sem coluna Versão; CONTEXTO.md fora da cadeia de propagação. Execução toca M01 + W05 Camada 1 + S04. | W04 sessão 2 | — |
| 2026-06-08 | 2026-06-15 | Handoff qualificado com diagnóstico causal | aprovado 🔒 | Nova etapa no W03/WORKFLOW.md | W04 sessão 2 | — |
| 2026-06-08 | 2026-06-15 | Princípio staging area: ideias em excesso > ideias perdidas | aprovado 🔒 | Formalizar na Seção 2 do W04/WORKFLOW.md | W04 sessão 2 | — |
| 2026-06-08 | 2026-06-15 | Critério de curadoria Etapa 5: prioridade × factibilidade × tempo | aprovado 🔒 | Formalizar na Etapa 5 do W04/WORKFLOW.md | W04 sessão 2 | — |
| 2026-06-14 | 2026-06-15 | Ergonomia de fechamento — ambos os pacotes em sequência | aprovado 🔒 | Atualizar W06/WORKFLOW.md | W04 sessão 2 | — |
| 2026-06-14 | 2026-06-15 | Declaração explícita de qual token nos blocos copiáveis | aprovado 🔒 | Atualizar PROTOCOLO-SESSAO.md + W06 | W04 sessão 2 | — |
| 2026-06-15 | 2026-06-15 | Skills client-side / hub-client-side | aprovado 📊 | Repositório agregador de pacotes instaláveis; primeiro pacote S06-CS + meta-skill S-CSC (proto); README com instrução de instalação e disclosure de compatibilidade | W04 sessão 2 | `2026-06-15-skills-client-side-e-rascunhos-staging.md` |
| 2026-06-15 | 2026-06-15 | Pasta rascunhos-staging + fluxo completo de ciclo de vida | aprovado 🔒 | Formalização do fluxo como espinha do processo de criação: rito de criação (critérios de elegibilidade), rito de atualização (seções datadas), ciclo de vida do rascunho (3 status: pendente/aprovado/rejeitado), transição 1 (rascunho aprovado → hub-memoria), transição 2 (registrada como ideia derivada — curadoria longitudinal), Seção D ganha coluna Rascunho | W04 sessão 2 | `2026-06-15-skills-client-side-e-rascunhos-staging.md` |
| 2026-06-11 | 2026-06-15 | PROTOCOLO-SESSAO (baixa formal — já consolidado em v1.0 em 2026-06-13) | aprovado 🔒 | Consolidado em PROTOCOLO-SESSAO.md v1.0 | W04 sessão 2 | — |
| 2026-06-12 | 2026-06-15 | Entrega de artefatos em bloco copiável (baixa formal — já consolidado) | aprovado 🔒 | Consolidado em PROTOCOLO-SESSAO.md v1.0 | W04 sessão 2 | — |
| 2026-06-12 | 2026-06-15 | Bloco de abertura da próxima sessão no fechamento (baixa formal — já consolidado) | aprovado 🔒 | Consolidado em PROTOCOLO-SESSAO.md v1.0 | W04 sessão 2 | — |
| 2026-06-12 | 2026-06-15 | Consulta de previsão na abertura — loop simétrico ao fechamento | aprovado 🔒 | Adicionar à S04 (rito de execução) e W06 (rito de sessão); consome modelo 🧪 de priorização | W04 sessão 2 | — |
| 2026-06-12 | 2026-06-15 | Princípio da fonte primária sobre o estado derivado | aprovado 🔒 | Formalizar em nomenclatura.md; Seção E permanece pendente até curadoria longitudinal | W04 sessão 2 | — |
| 2026-06-05 | 2026-06-15 | Intenção do Comandante como princípio universal do ecossistema | aprovado | Já em execução | W04 sessão 1 | — |
| 2026-06-05 | 2026-06-15 | Visão de longo prazo — ecossistema empoderado por APIs externas | aprovado 📊 | Longo prazo | W04 sessão 1 | — |
| 2026-06-06 | 2026-06-15 | Modularização da S04 por tipo de operação | aprovado 🔒 | Médio prazo | W04 sessão 1 | — |
| 2026-06-06 | 2026-06-15 | Reorganização completa do backlog-versoes.md do M01 | aprovado 🔒 | Médio prazo | W04 sessão 1 | — |
| 2026-06-06 | 2026-06-15 | Correção das instruções raw.githubusercontent.com remanescentes | aprovado 🔒 | Concluído | W04 sessão 1 | — |
| 2026-06-06 | 2026-06-15 | Inconsistência terminológica orientadoras vs ordenadoras | aprovado 🔒 | Concluído | W04 sessão 1 | — |
| 2026-06-06 | 2026-06-15 | Lote de termos GLOSSARIO.md | aprovado 🔒 | Concluído | W04 sessão 1 | — |
| 2026-06-06 | 2026-06-15 | Versão W06 (campo Versão Seção 1) | aprovado 🔒 | Concluído | W04 sessão 1 | — |
| 2026-06-06 | 2026-06-15 | ID W04 reutilizado — atribuir W07 ao wkf-resumo-executivo | aprovado 🔒 | Concluído | W04 sessão 1 | — |
| 2026-06-06 | 2026-06-15 | Timestamp ISO 8601 em entradas de backlog/changelog | aprovado 🔒 | Médio prazo | W04 sessão 1 | — |
| 2026-06-06 | 2026-06-15 | Critério de duplicata W05 | aprovado 🔒 | Médio prazo | W04 sessão 1 | — |
| 2026-06-07 | 2026-06-15 | Tipo wiki + wiki-ecossistema | aprovado 📊 | Médio prazo | W04 sessão 1 | — |

---

## Seção E — Conhecimentos consolidados (hub-aprendizagem)

### Intenção do Comandante desta seção

O hub-aprendizagem existe para que o conhecimento adquirido na prática não
se dissipe em backlogs e históricos de conversa. Ele não é documentação
operacional — é memória intelectual. A diferença é fundamental: backlogs
registram *o que* foi feito; o hub-aprendizagem registra *o que foi aprendido*,
*por que importa* e *como se compara com o que o mundo já sabe*.

Um aprendizado consolidado é diferente de uma ideia embrionária (Seção C).
Ele já passou pelo crivo da prática — foi testado, observado, confrontado com
benchmarks, e resultou em uma lição que vale ser sedimentada em linguagem
narrativa. Ele responde à pergunta: *"se tivéssemos sabido isso antes,
o que teríamos feito diferente?"*

Esta seção é o pré-estágio do hub-aprendizagem. Itens aqui aguardam
apenas redação final e inserção formal no repositório.

---

### Instrução para agentes de IA — identificação de conhecimento consolidado

**Quando executar:** após a mineração de ideias da Etapa 6-A, antes do
relatório de encerramento. Também executada no W03 (Etapa 2-B) ao final
de sessões que produzam diagnóstico, decisão arquitetural ou mudança estrutural.

**Critério de elegibilidade — o aprendizado é consolidado se:**

| # | Critério | Pergunta de teste |
|---|---|---|
| 1 | Resolveu um problema que se repetia sem solução definitiva | *"este problema voltará a aparecer se não registrarmos o aprendizado?"* |
| 2 | Revelou uma causa raiz que não era óbvia antes | *"antes desta sessão, a causa raiz era conhecida?"* |
| 3 | Produziu uma decisão arquitetural com raciocínio documentável | *"existe contexto, alternativas consideradas e consequências que merecem registro?"* |
| 4 | Chegou intuitivamente a algo que benchmarks de mercado validam | *"o que fizemos tem nome, padrão ou literatura de referência?"* |
| 5 | Gerou uma lição que muda como operamos daqui para frente | *"o ecossistema operará diferente por causa do que aprendemos hoje?"* |

Um aprendizado é elegível se atender **pelo menos dois** critérios.

**Procedimento:**

**Passo 1 — Identificação**
Após a varredura de ideias da Seção C, fazer segunda varredura com foco
em aprendizados — não em ideias. O sinal é diferente: não é "seria
interessante se..." mas "aprendemos que...", "descobrimos que...",
"a causa raiz era...", "o que o mercado chama de...".

**Passo 2 — Apresentação ao mantenedor**

```
📚 Aprendizado consolidado identificado:
"[síntese do aprendizado em 1-2 frases]"

Critérios ativados: [números]
Benchmarks relacionados: [se identificados]
Contexto: [em que momento da sessão surgiu]

Gostaria de registrar e redigir este aprendizado para o hub-aprendizagem?
```

**Passo 3 — Redação imediata**
Após aprovação, redigir o aprendizado completo **ali mesmo**, com contexto
fresco. Formato: narrativa com contexto, diagnóstico, benchmark relacionado
e lição permanente. Não deixar para depois — o contexto da sessão
é o recurso mais valioso e se perde com o tempo.

**Passo 4 — Depósito na tabela abaixo**
Status inicial: `pendente`. Quando inserido no hub-aprendizagem: `registrado`.

---

### Tabela de conhecimentos consolidados

| Data | Sessão de origem | Aprendizado | Critérios ativados | Rascunho disponível | Status | Aguardando desde |
|---|---|---|---|---|---|---|
| 2026-06-21 | Sessão operacional 2026-06-21 — S05 v1.1 + D01 v1.1 | **Importação de artefatos externos exige reconciliação, não cópia** — sessões de IA externas que conhecem a estrutura do ecossistema tendem a reproduzir seus padrões internamente (neste caso, a sessão de produção embutiu uma seção `## Histórico de Versões` dentro do SKILL.md, espelhando a função do `backlog-versoes.md`). Ao importar artefatos produzidos fora do rito canônico, é preciso varrer e remover estruturas espelhadas — fontes de drift da mesma classe do Erro #013. A importação não é cópia: é reconciliação contra a fonte de verdade. Benchmark: Single Source of Truth (SSOT). | #1, #3, #5 | Rascunho a redigir | pendente | 2026-06-21 |
| 2026-06-15 | W04 sessão 2 — C4 versionamento e C7 ATLAS | **Teste de valor contra o estado final** — ideias que têm a sensação intuitiva de fazer sentido podem demonstrar o contrário quando confrontadas com duas perguntas: "o que garantimos ao fazer?" e "o que perdemos ao não fazer?", ambas aplicadas ao estado final esperado. Caso fundador: inter-referenciamento de versões (cadeia sumario→CONTEXTO→arquivo) parecia tecnicamente saudável; o confronto com essas perguntas revelou custo alto sem retorno real. Parentesco com YAGNI e crítica à otimização prematura da engenharia de software. | #2, #4, #5 | Rascunho a redigir | pendente | 2026-06-15 |
| 2026-06-15 | W04 sessão 2 — C15 consulta de previsão / C7 modelo 🧪 | **Mecanismos orientam, o humano decide, sobreposição é explícita** — postura de design em que mecanismos automatizados aconselham ou ordenam por padrão, mas nunca bloqueiam; a autoridade de decisão permanece humana e qualquer sobreposição é declarada e legítima. Observado em três mecanismos na mesma sessão: modelo de priorização 🧪 (orienta, não determina), loop de abertura C15 (segue fila por padrão, urgência sobrepõe), fallback de urgência. *Nota de maturidade: três instâncias na mesma sessão — amadurecer antes de promover a capítulo.* | #2, #5 | Rascunho a redigir | pendente | 2026-06-15 |
| 2026-06-14 | Sessão — propagação dois tokens ao W05/W06 | **O auditor não escreve o próprio log** — corolário concreto da separação executor/auditor: como o auditor opera só com token de leitura, qualquer artefato que exija escrita (o log do W05) é depositado pela sessão executora. Decisão de design (Opção A) que redesenhou a Etapa 8 do W05 v1.3. **Texto redigido nesta sessão — aguarda depósito no cap-02 do hub-aprendizagem (nova Seção 8 + Lição 6).** | #2, #3, #5 | Rascunho redigido em W04 sessão 2 | pendente | 2026-06-14 |
| 2026-06-08 | W04 — primeira sessão de roadmapping (curadoria T1) | API GitHub vs raw.githubusercontent.com: por que a regra existe, o que observamos que acontece com CDN cache em operações de leitura operacional, e como chegamos à instrução "nunca raw — sempre API" | #1, #2, #5 | cap-04-api-vs-raw.md (hub-aprendizagem, 2026-06-16) | registrado | 2026-06-08 |
| 2026-06-05 | Sessão de engenharia reversa e W05 | Separação executor/auditor como princípio arquitetural — viés de confirmação estrutural, Defense in Depth, W05 como camada independente | #1, #2, #4, #5 | cap-02 — **depósito da Seção 8 + Lição 6 pendente** | registrado | 2026-06-05 |
| 2026-06-07 | Sessão de design do wiki-ecossistema | Conhecimento como query — distinção entre informação materializada e derivada sob demanda; fronteira viva/congelada | #3, #5 | Rascunho completo (cap-03) | registrado | 2026-06-07 |
| 2026-06-12 | Sessão de operação — formalização do ciclo de sessão | Princípio da fonte primária sobre o estado derivado — reconstruir da fonte primária é preferível a remendar o derivado. NOTA DE MATURIDADE: aguardar mais instâncias antes de promover a capítulo. | #1, #2 | Rascunho a redigir — aguardar mais instâncias | pendente | 2026-06-12 |

---

### Legenda de status (Seção E)

| Status | Significado |
|---|---|
| `pendente` | Identificado e aprovado — aguarda inserção no hub-aprendizagem |
| `registrado` | Inserido formalmente no hub-aprendizagem |
| `arquivado` | Avaliado e não avança — ver Seção D |

---

## Legenda de status (Seções B e C)

| Status | Significado |
|---|---|
| `pendente` | Aguarda próxima sessão do W04 |
| `maturando` | Foi avaliada, tem potencial, precisa de mais reflexão |
| `aprovada` | Migrou para o ROADMAP confirmado |
| `arquivada` | Avaliada e não avança no momento — ver Seção D |
| `rejeitada` | Avaliada e descartada — ver Seção D |

## Política de limpeza

Após cada sessão do W04, toda a Seção A é processada e esvaziada.
Seções B, C e E: itens com decisão migram para a Seção D.
Itens com status `maturando` permanecem nas seções originais.
**Nenhum item é deletado — apenas movido.**

## Política de rascunhos (hub-entrada/rascunhos-staging/)

Rascunhos MD depositados em `rascunhos-staging/` seguem o ciclo de vida:
- **pendente:** arquivo vivo — pode receber seções de atualização datadas
- **aprovado:** recebe cabeçalho de status; permanece como histórico; ideia
  migra para hub-memoria como documento vivo após aprovação em W04
- **rejeitado:** recebe cabeçalho de status; permanece como histórico

Nomenclatura: `AAAA-MM-DD-[slug].md`
Nenhum rascunho é deletado.
