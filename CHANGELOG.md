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

# CHANGELOG — Ecossistema DTD/SETIS

Histórico cronológico de tudo que foi construído.
Entrada mais recente no topo.

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
