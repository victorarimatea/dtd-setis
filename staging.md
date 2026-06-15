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
| 2026-06-13 | CONTEXTO.md (hub-fonte) | PTD / PTD-SES | Instrumento de planejamento citado junto ao PDTIC (que está definido); assimetria notável — pode merecer entrada breve de contextualização | SEV4 W05 2026-06-13 | ⏳ pendente |
| 2026-06-13 | CONTEXTO.md (hub-fonte) | SGTD | Subcomitê de Governança de TI e Dados que o mantenedor preside; usado na seção de governança do ecossistema | SEV4 W05 2026-06-13 | ⏳ pendente |
| 2026-06-13 | CONTEXTO.md (hub-fonte) | CIG/SES | Comitê Institucional de Governança referenciado na Portaria 193/2024; colegiado externo ao ecossistema | SEV4 W05 2026-06-13 | ⏳ pendente |
| 2026-06-13 | CONTEXTO.md (hub-fonte) | Fórum de Subsecretários | Instância deliberativa referenciada nas regras de linguagem institucional do CONTEXTO.md | SEV4 W05 2026-06-13 | ⏳ pendente |
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

---

### Tabela de ideias mineradas

| Data | Conversa de origem | Ideia candidata | Pergunta orientadora ativada | Validada pelo mantenedor | Status | Aguardando desde |
|---|---|---|---|---|---|---|
| 2026-06-14 | Sessão de design ATLAS — amadurecimento do roadmap e governança da evolução | ATLAS — nome do núcleo genérico e iniciativa-guarda-chuva da Fase 2 do roadmap (governança da evolução). Distinção estrutural: a maquinaria de governança/automação (S04, taxonomia de tipos, controle de drift, separação executor/auditor, staging, W04/W05/W06) é genérica e independente do domínio saúde; ATLAS nomeia esse NÚCLEO. DTD/SETIS permanece como a primeira INSTÂNCIA — sem rebatismo, sem DOU-3, sem cascade em cabeçalhos. Generalização = hipótese ML-1, não execução (segunda instância ainda não existe). Três itens já na base convergem sob esse guarda-chuva: (a) Disciplina de Arquitetura do Conhecimento (Seção C, 2026-06-11) — saúde estrutural; IS/RD por outro nome; (b) Consulta de previsão na abertura (Seção C, 2026-06-12) — execução reativa→previsível; (c) Reclassificação W03/fronteira skill↔workflow (ROADMAP, médio prazo). Modelo de classificação: IS-1..5 (impacto sistêmico), RD-1..5 (risco de drift), ES-1..5 (economia sistêmica), DOU-0..3 (impacto doutrinário), ML-0..5 (maturidade). Mercado (RICE, WSJF, AHP, Lean Portfolio) como referência de método, não de modelo. Princípios fixados: escore é QUERY calculada na leitura, nunca artefato gravado; camada auto-computável (IS/RD/ES) separada da irredutivelmente humana (DOU, 'agora?'); orienta, não determina; começar mínimo. Laboratório: opcional, acionado por alto IS/RD (forma provável: branches API), não é portão obrigatório no fluxo principal. Destino final: DECISOES.md + sessão evolutiva dedicada. NÃO promover sem decisão de nome e moldura. Ref.: documento 'Evolução do Roadmap e Governança da Evolução' + consolidação sessão 2026-06-14. | #2, #5, #6, #7 | ✅ confirmado | ⏳ pendente | 2026-06-14 |
| 2026-06-14 | Pendência carregada — abertura da sessão 2026-06-14 | Ergonomia de fechamento — o encerramento da sessão deve entregar AMBOS os pacotes em code fence copiável em sequência: Pacote 2 (bloco de reauditoria W05, para o chat avulso de auditoria) e Pacote 1 (bloco de abertura da próxima sessão, já contextualizado pelo handoff). Coerente com o princípio 'entrega de artefatos em bloco copiável' (Seção C, 2026-06-12) e com a ergonomia de transporte do PROTOCOLO-SESSAO.md. Avaliar como item do roteiro formal de encerramento do W06/WORKFLOW.md. | #1, #5, #6 | ✅ confirmado | ⏳ pendente | 2026-06-14 |
| 2026-06-14 | Sessão — propagação dois tokens W05/W06 + correção pós-auditoria | Todo bloco copiável com campo de token (Pacotes 1/2 do W06, PROTOCOLO-SESSAO) deve declarar explicitamente QUAL token (leitura vs edição) — convenção e/ou checagem automatizável. Motivação: o campo genérico "acesso repo" travou a largada da sessão de 2026-06-14, pedindo o token errado para a fase de leitura | 1, 6 | ✅ confirmado | ⏳ pendente | 2026-06-14 |
| 2026-06-13 | Sessão quitação dívida legada | CONFIRMAR com delay mínimo (3s) como sub-passo obrigatório da S04 Etapa 5 — incorporar na instrução de execução pós-PUT: aguardar 3s e fazer GET separado antes de declarar confirmação. Motivação: falso-negativo por propagação da API GitHub reocorreu em 2 itens desta sessão e estava no handoff como resíduo SEV4 não formalizado; delay de 3s foi suficiente empiricamente | 1, 5 | ⏳ pendente | — | — |
| 2026-06-13 | Sessão quitação dívida legada | Design: Simplificação do modelo de propagação de versões — avaliar sumario-only ou source-only (omitir versão do CONTEXTO.md; adaptar Camada 1 da W05 e checklists da S04). Motivação: cadeia de 3 nós é fonte recorrente de drift; princípio knowledge-as-query já adotado no ecossistema | 7 | ⏳ pendente | — | — |
| 2026-06-08 | W04 — encerramento + exercício teórico pós-auditoria | Handoff qualificado com diagnóstico causal: quando o W05 retorna SEV2, o W03 inclui etapa explícita de diagnóstico causal ("por que esse SEV2 existiu") aproveitando o contexto vivo da sessão executora — a correção vai para o Handoff, o diagnóstico fica registrado; a sessão de auditoria absorve o Handoff qualificado e pode executar as correções com causa raiz documentada, fechando o ciclo entre executor e auditor | #4 (pergunta estratégica sem resposta imediata) e #7 (implicação estratégica identificada pelo agente) | ✅ confirmado | pendente | 2026-06-08 |
| 2026-06-08 | W04 — primeira sessão de roadmapping | Princípio da staging area: "idéias em excesso são preferíveis a idéias perdidas" — a curadoria é o momento da consolidação, não o registro; formalizar na Seção 2 do W04/WORKFLOW.md como princípio de design da staging | #6 — nomeação de princípio que não estava formalizado | ✅ confirmado | pendente | 2026-06-08 |
| 2026-06-08 | W04 — primeira sessão de roadmapping | Critério de curadoria da Etapa 5 do W04: árbitro é prioridade × factibilidade × tempo disponível na sessão — quando há pouco tempo, encaixar tarefa mais rápida sem perder visão do que é mais importante; formalizar na Etapa 5 do W04/WORKFLOW.md | #6 — princípio articulado em voz alta, não escrito no workflow | ✅ confirmado | pendente | 2026-06-08 |
| 2026-06-04 | Sessão de criação do W04 | Estrutura formal de perfis de acesso do ecossistema — define quem pode visualizar, editar e criar em cada repositório; base para governança multiusuário | #1 — lacuna identificada | ✅ confirmado | maturando | 2026-06-04 |
| 2026-06-04 | Sessão de criação do W04 | Família de workflows derivados do W04 para projetos específicos — `wkf-roadmap-telessaude`, `wkf-roadmap-pdtic` e outros, sem alterar o W04 base | #6 — nomeação de algo que não existe | ✅ confirmado | maturando | 2026-06-04 |
| 2026-06-05 | Sessão de correção de drifts e Intenção do Comandante | Intenção do Comandante como princípio universal do ecossistema — declarar no `nomenclatura.md` e exigir que cada skill tenha sua própria declaração calibrada para seu domínio | #7 — implicação estratégica não explorada | ✅ confirmado | aprovada | 2026-06-05 |
| 2026-06-05 | Sessão de engenharia reversa e hub-aprendizagem | Visão de longo prazo — ecossistema empoderado por APIs externas, automações sem piloto humano, integração com ferramentas além do GitHub | #5 — desejo e intenção de longo prazo não convertida em ação imediata | ✅ confirmado | aprovada | 2026-06-05 |
| 2026-06-06 | Sessão de auditoria W05 e amadurecimento do ecossistema | Modularização da S04 por tipo de operação — cada OP-X como módulo independente, S04 funcionando como dispatcher | #4 e #7 | ✅ confirmado | aprovada | 2026-06-06 |
| 2026-06-06 | 4ª auditoria W05 de fechamento (Opus 4.8) | Reorganização completa do backlog-versoes.md do M01 — missão dedicada | Identificado por auditoria W05 SEV3 | ✅ confirmado | aprovada | 2026-06-06 |
| 2026-06-06 | Fechamento sessão 2026-06-06 — auditorias W05 | Correção das instruções raw.githubusercontent.com remanescentes no W05/WORKFLOW.md e no CONTEXTO.md | Item prioritário | ✅ confirmado | aprovada | 2026-06-06 |
| 2026-06-06 | Fechamento sessão 2026-06-06 | Resolver inconsistência terminológica "perguntas orientadoras" vs "perguntas ordenadoras" | Detectado por auditoria W05 | ✅ confirmado | aprovada | 2026-06-06 |
| 2026-06-06 | Fechamento sessão 2026-06-06 | Lote de termos para o GLOSSARIO.md: versionamento independente, conhecimento consolidado, Padrão CONFIRMAR, context mining/mineração de contexto, perguntas orientadoras | Candidatos SEV4 acumulados | ✅ confirmado | aprovada | 2026-06-06 |
| 2026-06-06 | Fechamento sessão 2026-06-06 | Atualizar campo Versão na Seção 1 do W06/WORKFLOW.md para v1.1 | Detectado por auditoria W05 SEV3 | ✅ confirmado | aprovada | 2026-06-06 |
| 2026-06-06 | Fechamento sessão 2026-06-06 | ID W04 reutilizado em item prospectivo do ROADMAP (wkf-iac-conformidade) — atribuir W07 | Detectado por auditoria W05 SEV4 | ✅ confirmado | aprovada | 2026-06-06 |
| 2026-06-06 | Fechamento sessão 2026-06-06 — reflexão de Victor | Adotar timestamp ISO 8601 completo nas entradas de backlog/changelog — aplicação prospectiva | Reflexão estratégica de Victor | ✅ confirmado | aprovada | 2026-06-06 |
| 2026-06-06 | Fechamento sessão 2026-06-06 — visão de Victor | Antecipar cenário multi-contribuidor: campos autor/revisor nas entradas de backlog | Visão de longo prazo de Victor | ✅ confirmado | maturando | 2026-06-06 |
| 2026-06-06 | Fechamento sessão 2026-06-06 — derivado | Ajustar critério de detecção de duplicata do W05 | Derivado da discussão sobre timestamp | ✅ confirmado | aprovada | 2026-06-06 |
| 2026-06-07 | Sessão de design do wiki-ecossistema | Criar o tipo `wiki` na nomenclatura + repositório `wiki-ecossistema` | #6 — nomeação de algo que não existe | ✅ confirmado | aprovada | 2026-06-07 |
| 2026-06-07 | Sessão de design do wiki-ecossistema | Definir a anatomia do cabeçalho de metadados de documento normativo (YAML frontmatter) | #1 e #2 | ✅ confirmado | maturando | 2026-06-07 |
| 2026-06-07 | Sessão de design do wiki-ecossistema | Workflow de ingestão assistida de norma (N1) — ao subir documento novo, gera relatório de impacto | #1 e #6 | ✅ confirmado | maturando | 2026-06-07 |
| 2026-06-07 | Sessão de design do wiki-ecossistema | Workflow de vigília de conformidade (N2) — cruza a base: lei federal nova → portarias/normas locais potencialmente desatualizadas | #1 e #4 | ✅ confirmado | maturando | 2026-06-07 |
| 2026-06-07 | Sessão de design do wiki-ecossistema | Template padronizado de página-tema do wiki | #6 e #1 | ✅ confirmado | maturando | 2026-06-07 |
| 2026-06-11 | Sessão de design do ciclo de sessão (relatório+handoff+ritos) | Memória de domínio do briefing de saúde digital — cada acionamento do briefing deposita registro datado do que viu (classificado pela `taxonomia-saude-digital`); o acervo vira consultável, aplicando "conhecimento como query" (cap-03) a conteúdo noticioso. Três usos: anti-repetição (distingue novidade de desdobramento), curva de destaque temporal (alta no mês vs. panorama do ano), staging de investigação (marcar notícias para mergulho posterior). PRIMEIRA categoria de registro de CONTEÚDO/domínio, distinta de todo registro de PROCESSO/infraestrutura existente. Relaciona-se com a ideia 'Handoff qualificado' (mesma seção) na lógica de acervo consultável | #2 (hipótese sobre algo que poderia existir) e #7 (implicação estratégica identificada pelo agente) | ✅ confirmado | pendente | 2026-06-11 |
| 2026-06-11 | Sessão de design do ciclo de sessão | Contribuição externa via issues públicas — repositório público porta-de-entrada dedicado a issues (o GitHub não oferece permissão só-issues no mesmo repo) recebe sugestões de qualquer usuário sem acesso de escrita; fluxo: issue externa → triagem do mantenedor → staging interna, preservando 'nada avança sem aprovação'. Controle de abuso via limites de interação (contribuidores anteriores / contas >24h; 24h a 6 meses). Fork+PR como canal complementar para propostas de código (terceiro testando o IAC). VIABILIDADE TÉCNICA CONFIRMADA por pesquisa em 2026-06-11 | #1 (lacuna no ecossistema — governança multiusuário) e #6 (nomeação de algo que não existe) | ✅ confirmado | pendente | 2026-06-11 |
| 2026-06-11 | Sessão de design do ciclo de sessão (anexo de amadurecimento) | Disciplina de Arquitetura do Conhecimento — terceira camada de governança, ORTOGONAL à auditoria: a auditoria (W05) verifica CONFORMIDADE ('o sistema está correto?'); esta verifica SAÚDE ESTRUTURAL ('o sistema continua evoluindo de forma sustentável?'). Conformidade e qualidade arquitetural são dimensões distintas — um artefato pode passar em todas as validações e acumular dívida arquitetural. Princípios qualificadores: complexidade, coesão, acoplamento, duplicação, fragmentação, convergência skill↔workflow, divergência workflow↔skill, ownership (fonte canônica única). VINCULADA à meta autônoma 'Reclassificação W03 e fronteira skill↔workflow' no ROADMAP — provável abordagem conjunta. Relaciona-se com 'Modularização da S04' (mesma seção) como resposta tática ao mesmo problema de inchaço. ESCOPO: material e maduro demais para subitem — merece sessão evolutiva própria | #1 (lacuna estrutural identificada) e #7 (implicação estratégica não explorada) | ✅ confirmado | pendente | 2026-06-11 |
| 2026-06-11 | Pérola final da sessão (pós-encerramento) | Protocolo de sessão canônico + regra de acesso contextual API/raw — criar `hub-entrada/PROTOCOLO-SESSAO.md` como fonte canônica dos ritos (abertura/fechamento/leitura), permitindo blocos de terminal enxutos (ponteiros estáveis; conteúdo evolui no GitHub). Inclui: (a) REGRA DE ACESSO CONTEXTUAL — API-only para operação (anti-drift pós-escrita), raw para leitura sem token (contorna teto de 60 req/h por IP; cache CDN inócuo sem escrita) — descoberta empírica de 2026-06-11, REGISTRAR no CONTEXTO.md antes que se perca (já se perdeu uma vez); (b) BLOCO DE LEITURA COMPARTILHÁVEL read-only para demonstração a terceiros (chefe/colega/qualquer LLM com web), hub-entrada como anfitrião; (c) bloco de leitura 3a promovível a operação se surgir insight. Vinculado à meta 'Formalização do ciclo de sessão' (W06) no ROADMAP — provável execução conjunta. Ref.: ANEXO-2026-06-11-blocos-terminal-e-protocolo-sessao | #1 (lacuna: acesso multiusuário sem token) e #7 (implicação estratégica: demonstrabilidade do ecossistema) | ✅ confirmado | pendente — consolidada em PROTOCOLO-SESSAO.md v1.0 (2026-06-13); baixa no W04 | 2026-06-11 |
| 2026-06-12 | Sessão de operação — formalização do ciclo de sessão | Consulta de previsão na abertura — verificação ROADMAP/staging ANTES de aceitar intervenção. A S04 hoje fecha o loop no fim (reconciliação 5-A retroativa) mas não o abre no começo: nenhuma etapa pergunta, antes de executar, se a intervenção proposta já está prevista no ROADMAP (e é o próximo tijolo da fila) ou se é intervenção nova que deveria passar pela staging primeiro. Proposta: loop de abertura simétrico ao de fechamento — na abertura, consultar a sequência prevista no ROADMAP e seguir a ordem por padrão; intervenções fora da fila exigem declaração explícita de urgência/emergência (legítima no estágio inicial do sistema). Move o ecossistema de execução reativa para execução previsível e priorizada. Toca S04 (rito de execução) e W06 (rito de sessão). Relaciona-se com 'Disciplina de Arquitetura do Conhecimento' e com o princípio da fonte primária (mesma seção) | #1 (lacuna estrutural no rito de execução) e #7 (implicação estratégica não explorada) | ✅ confirmado | pendente | 2026-06-12 |
| 2026-06-12 | Sessão de operação — regra de fallback do handoff | Princípio da fonte primária sobre o estado derivado — quando um artefato de estado derivado (handoff, índice, painel, cabeçalho de versão) falha ou diverge, reconstruir a partir da fonte de verdade primária (o ecossistema real) é preferível a remendar o derivado. Generalização da regra de fallback do W06 (handoff corrompido → auditoria W05 nova do zero) decidida nesta sessão. Aplicável a outros pontos: INDICE.md corrompido → regerar da árvore; painel de staging → recalcular das tabelas (já aplicado); divergência de versão → reconciliar da fonte canônica. Candidato a princípio formal no hub-aprendizagem se confirmado em mais instâncias. Surgiu também na investigação da divergência de versão do M01 nesta mesma sessão — terceira instância do mesmo padrão no dia | #7 (implicação estratégica identificada pelo agente a partir de decisão pontual do mantenedor) | ✅ confirmado | pendente | 2026-06-12 |
| 2026-06-12 | Sessão de operação — formalização do ciclo de sessão | Entrega de artefatos de sessão em bloco copiável (low-friction handoff no lado humano) — todo texto que o mantenedor precisa transportar entre chats (Pacote 2 de auditoria, blocos-ponteiro, instruções de reauditoria) deve ser entregue pelo agente em code fence pronto para cópia de um toque, eliminando a seleção manual de texto no bloco de notas do celular. É a contrapartida, no lado humano, do que a leitura automática do handoff (W06 v1.2) fez no lado do agente: ambos removem uma etapa manual frágil de um rito recorrente. Princípio de design de interface dos ritos; insumo direto de como o futuro PROTOCOLO-SESSAO.md deve apresentar seus blocos (sempre em code fence copiável) | #1 (atrito recorrente no lado humano de todo fechamento) e #5 (muda como conduzimos os ritos daqui em diante) | ✅ confirmado | pendente — consolidada em PROTOCOLO-SESSAO.md v1.0 (2026-06-13); baixa no W04 | 2026-06-12 |
| 2026-06-12 | Sessão de operação — encerramento | Bloco de abertura da próxima sessão entregue no fechamento da atual — ao encerrar, o agente apresenta em code fence copiável o Bloco 1 (abertura de operação) da PRÓXIMA sessão, já contextualizado pelo estado que termina (missão provável, dívida prioritária do handoff), faltando apenas o token. Fecha o arco de baixo atrito: handoff lido automaticamente (lado agente) + Pacote 2 copiável (fechamento) + Bloco 1 copiável (abertura seguinte). O mantenedor copia o bloco da sessão anterior, leva à seguinte, insere o token e já abre uma sessão de construção — corrente contínua entre sessões. O bloco de leitura (3a/3b) NÃO é entregue (mora no bloco de notas, uso pontual); só o de operação. Insumo para o PROTOCOLO-SESSAO.md | #1 (atrito recorrente de abertura) e #5 (continuidade de fato entre sessões) | ✅ confirmado | pendente — consolidada em PROTOCOLO-SESSAO.md v1.0 (2026-06-13); baixa no W04 | 2026-06-12 |

---

## Seção D — Arquivo histórico

*Ideias e registros já processados em sessões do W04.*
*Nunca deletados — o histórico de decisões tem valor institucional.*

| Data entrada | Data decisão | Item | Decisão | Motivo | Sessão |
|---|---|---|---|---|---|
| 2026-06-04 | 2026-06-08 | S04 v2.2 — Verificação 5-A: reconciliação obrigatória com ROADMAP | aprovado 🔒 | Maturidade interna — rastreabilidade | W04 sessão 1 |
| 2026-06-04 | 2026-06-08 | W03 v1.1 — Etapa 2-A: reconciliação com ROADMAP | aprovado 🔒 | Maturidade interna — rastreabilidade | W04 sessão 1 |
| 2026-06-04 | 2026-06-08 | W04 wkf-roadmap-geral v1.0 — criação do workflow de gestão de roadmap | aprovado 📊 | Narrativa estratégica para SETIS | W04 sessão 1 |
| 2026-06-04 | 2026-06-08 | staging.md — criação da staging area do ecossistema | aprovado 🔒 | Implementação técnica interna | W04 sessão 1 |
| 2026-06-05 | 2026-06-08 | S04 v2.5 — escala de severidade SEV1–SEV4 | aprovado 🔒 | Maturidade interna | W04 sessão 1 |
| 2026-06-05 | 2026-06-08 | S04 v2.6 — verificações embutidas CONFIRMAR | aprovado 🔒 | Maturidade interna | W04 sessão 1 |
| 2026-06-05 | 2026-06-08 | hub-aprendizagem v1.0 — repositório de memória intelectual criado | aprovado 📊 | Narrativa de valor para SETIS | W04 sessão 1 |
| 2026-06-05 | 2026-06-08 | S04 v2.7 — Etapa 6-A expandida com mineração de conhecimento consolidado | aprovado 🔒 | Maturidade interna | W04 sessão 1 |
| 2026-06-05 | 2026-06-08 | W03 v1.2 — Etapa 2-B: identificação de aprendizados consolidados | aprovado 🔒 | Maturidade interna | W04 sessão 1 |
| 2026-06-07 | 2026-06-08 | cap-03 hub-aprendizagem v1.1 — "Conhecimento como Query" + 5 ideias na staging | aprovado 📊 | Visão de longo prazo da camada de conhecimento | W04 sessão 1 |
| 2026-06-04 | 2026-06-08 | `wkf-resumo-executivo` (1ª entrada) | aprovado 📊 — consolidado com 2ª entrada | Ativo estratégico permanente; médio prazo | W04 sessão 1 |
| 2026-06-04 | 2026-06-08 | `wkf-resumo-executivo` (2ª entrada) | aprovado 📊 — consolidado com 1ª entrada | Mesmo item, duas capturas; unificado | W04 sessão 1 |

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
| 2026-06-14 | Sessão — propagação dois tokens ao W05/W06 | O auditor não escreve o próprio log — corolário concreto da separação executor/auditor: como o auditor opera só com token de leitura e nunca recebe token de edição, qualquer artefato que exija escrita (o log de execução do W05) é depositado pela sessão executora. Decisão de design (Opção A) que redesenhou a Etapa 8 do W05 v1.3 | #2, #3, #5 | Rascunho a redigir | pendente | 2026-06-14 |
| 2026-06-08 | W04 — primeira sessão de roadmapping (curadoria T1) | API GitHub vs raw.githubusercontent.com: por que a regra existe, o que observamos que acontece com CDN cache em operações de leitura operacional, e como chegamos à instrução "nunca raw — sempre API" | #1 (problema recorrente), #2 (causa raiz não óbvia antes da prática), #5 (muda como operamos daqui para frente) | cap-04-api-vs-raw.md (hub-aprendizagem, 2026-06-16) | registrado | 2026-06-08 |
| 2026-06-05 | Sessão de engenharia reversa e W05 | Separação executor/auditor como princípio arquitetural — viés de confirmação estrutural, Defense in Depth, W05 como camada independente | #1, #2, #4, #5 | Rascunho completo disponível (cap-02) | registrado | 2026-06-05 |
| 2026-06-07 | Sessão de design do wiki-ecossistema | Conhecimento como query — distinção entre informação materializada e derivada sob demanda; fronteira viva/congelada | #3, #5 | Rascunho completo (cap-03) | registrado | 2026-06-07 |
| 2026-06-12 | Sessão de operação — formalização do ciclo de sessão | Princípio da fonte primária sobre o estado derivado — quando um artefato de estado derivado (handoff, índice, painel, cabeçalho de versão) falha ou diverge, reconstruir a partir da fonte de verdade primária (o ecossistema real) custa menos e é mais confiável que remendar o derivado. Observado em 3 instâncias no mesmo dia: (1) regra de fallback do handoff (W06 v1.2) — handoff corrompido aciona auditoria W05 nova; (2) painel de staging recalculado das tabelas por design; (3) investigação da divergência de versão do M01 — reconciliar da fonte canônica, não corrigir o número à mão. NOTA DE MATURIDADE: as 3 instâncias são do mesmo dia; #1 e #2 firmemente ativados, #5 ainda a confirmar por uso prolongado — amadurecer na Seção C antes de promover a capítulo do hub-aprendizagem | #1 (padrão recorrente), #2 (causa raiz não óbvia — o reflexo natural é remendar o derivado) | Rascunho a redigir — aguardar mais instâncias | pendente | 2026-06-12 |

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
