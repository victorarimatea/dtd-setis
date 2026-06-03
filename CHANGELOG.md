# CHANGELOG — Ecossistema DTD/SETIS

Histórico cronológico de tudo que foi construído.
Entrada mais recente no topo.

---

## [2.6] — 2026-06-03

### Corrigido
- `dtd-setis/README.md`: atualizado com estado completo do ecossistema derivado
  do `sumario.md` v1.6 — diagrama ASCII com 4 camadas e todos os tipos (M, S, D, W, A, P);
  tabela de repositórios expandida de 4 para 15 entradas, organizadas por tipo;
  seção de navegação com orientação de leitura ("Leia primeiro"). Correção de drift
  acumulado desde as Fases 2, 3 e 4 do ecossistema (2026-06-01 a 2026-06-02).
- `dtd-setis/CHANGELOG.md`: cabeçalho duplicado (

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
  ação / médio prazo / longo prazo); governanca-ses-df e todos os entregáveis
  de 2026-06-02 marcados como ✅
- `INDICE.md`: data, contagem de arquivos e referência a arquitetura.md v2.0
  atualizados
- `backlog-versoes.md`: entradas retroativas v1.1–v2.0 adicionadas — histórico
  completo do portfólio desde a fundação

### Atualizado (blindagem estrutural)
- `skill-github-orquestracao` → v1.8: Verificação 5 (consistência cruzada
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
- `agenda-dtd` (A01, privado): acervo institucional de reuniões da DTD.
- `workflow-registro-reuniao` (W02, privado): memória organizacional do processo
  de transformação de gravações em registros formais — inclui histórico de
  problemas P01-P03 e roadmap de automação com integração SEI.
- `skill-registro-reuniao` (S06, público): skill que formaliza o prompt
  institucional desenvolvido com o PLAUD NOTE Pro — 5 etapas, 8 seções
  obrigatórias, depósito automático via S04.
- `skill-github-orquestracao` → v1.7: OP-AG adicionado com lógica específica
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
- `workflow-transcricao-documental` (W01, público): primeiro repositório do
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
- `skill-github-orquestracao` → v1.6: OP-W adicionado; EXECUCOES.md na OP-P
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
- `governanca-ses-df` (D01, público): primeiro repositório do tipo Documento
  no ecossistema. Contém 28 documentos transcritos em Markdown sobre saúde
  digital — 18 regulamentações nacionais (legislação federal, distrital,
  portarias ministeriais, resoluções CFM e ANVISA) + 10 referências
  internacionais bilíngues EN+PT. Estrutura com 6 subpastas + WORKFLOW-
  ESPECIFICACAO.md v1.1 (8 problemas documentados, protocolo de exceção,
  roadmap de automação).
- `skill-transcricao-documental` (S05, público): pipeline de transcrição
  documental formalizado como skill do ecossistema — 7 etapas, auto-
  verificação programática, protocolo de exceção §3.1.

### Regularizado
- `doc-cadastro-ses-setis-dtd` (D02): repositório existente sem estrutura
  padrão — adicionados INDICE.md, backlog-versoes.md e ficha técnica.
  Registrado formalmente como D02 no sumário.
- `skill-iac-pdtic` (S02): estava ativo mas não registrado no sumário.
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
- `skill-github-orquestracao` → v1.5: Verificação 4 adicionada à Etapa 6
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
- `skill-github-orquestracao` → v1.4: INDICE.md adicionado às checklists
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
- `skill-github-orquestracao` → v1.3: OP-E com critério objetivo, INDICE.md
  nas checklists OP-A e OP-P, Erro #005 incorporado

---

## [1.5] — 2026-06-01

### Atualizado
- `skill-github-orquestracao` → v1.2: segundo ciclo de aprendizado
  contínuo na mesma sessão de criação — Erro #004 incorporado.
  Verificação de backlog agora aceita '## v' e '### v' como padrões
  válidos, eliminando falsos positivos em repositórios com subseções.
- `ecossistema-sumario/sumario.md` → v0.8: S04 atualizado para v1.2

---

## [1.4] — 2026-06-01

### Corrigido
- `README.md`: instrução obrigatória de inicialização adicionada ao topo —
  Claude deve ler o CONTEXTO.md do ecossistema-sumario antes de qualquer ação;
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
- `skill-github-orquestracao` → v1.1: primeiro ciclo completo de aprendizado
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
- Repositório público `skill-github-orquestracao` (S04): skill de orquestração
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
- Repositório privado `telessaude-poc-prisional` (P01): primeiro projeto formal
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
- `ecossistema-sumario/sumario.md` -> v0.3: dtd-setis registrado; versão do M01 reconciliada para v0.10

### Adicionado
- `ecossistema-sumario/backlog-acoes-dtd.md`: histórico retrospectivo de ações e produtos da DTD — fonte única para relatórios de atividade consolidados

### Corrigido
- Drift de índices: S03 e dtd-setis ausentes do sumário/contexto; versão do M01 desalinhada (índices em v0.5, backlog em v0.9) -> reconciliada para v0.10

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
- Repositório público `skill-poc-saude-digital` (S03) incorporado ao ecossistema
- Padrão de PoC em Saúde Digital formalizado como skill: 11 seções obrigatórias,
  protocolo de governança, análise normativa e instrumentos jurídicos
- Baseado na PoC MedNear, caso zero do Marco Regulatório Interno de PoCs da SES-DF
- `sumario.md` do ecossistema-sumario estruturado pela primeira vez (v0.2)

---

## [0.6] — 2026-05-27

### Adicionado
- Repositório público `dtd-setis` como repositório mãe do ecossistema
- `README.md` com apresentação pública e portfólio da DTD
- `MANIFESTO.md` com propósito, visão, objetivos e princípios
- `ROADMAP.md` com planejamento das próximas entregas
- `CHANGELOG.md` (este arquivo)
- `DECISOES.md` com registro das grandes decisões do projeto
- `docs/arquitetura.md` com descrição técnica do ecossistema
- `CONTEXTO.md` no `ecossistema-sumario` para inicialização rápida de sessões

### Atualizado
- `skill-iac-pdtic` → v2.0: adição do modo IAC-H, governança SES-DF,
  regras de linguagem institucional, protocolo de 7 etapas
- `ecossistema-sumario/sumario.md` → v0.5: modelo IAC documentado,
  skill-iac-pdtic registrada como v2.0
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
