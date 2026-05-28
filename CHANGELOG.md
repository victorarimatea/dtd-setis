# CHANGELOG — Ecossistema DTD/SETIS

Histórico cronológico de tudo que foi construído.
Entrada mais recente no topo.

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
  8 convergências identificadas, 5 lacunas, 0 conflitos

### Corrigido
- IAC-V v0.1 → v0.2: Seção 6 reescrita com linguagem regimental correta
  (termo "deliberação" substituído — competência do Fórum, não do SGTD)
- Acentuação completa em português aplicada a todos os documentos gerados
  (método de duas rodadas de substituição + verificação automática)

### Decisão
- Estabelecido padrão de dois modos IAC (V e H) como instrumento permanente
  de governança documental da DTD/SETIS

---

## [0.4] — 2026-05-27

### Adicionado
- Primeiro teste bem-sucedido do fluxo automatizado: S01 criou S02 via API
- `skill-iac-pdtic` (S02) v1.0 criada automaticamente pela `skill-criador-de-skills`
- Repositórios públicos: `ecossistema-sumario` e `skill-criador-de-skills`
- API do GitHub integrada ao fluxo de criação de skills
- Personal Access Token como mecanismo de autenticação para escrita

---

## [0.3] — 2026-05-26

### Adicionado
- `skill-criador-de-skills` (S01) v1.0 — skill fundacional do ecossistema
  Protocolo de 7 etapas para criação automatizada de repositórios de skill
- `ecossistema-sumario` como repositório âncora público
- `sumario.md` — índice vivo de todos os repositórios
- `nomenclatura.md` v0.1 — convenções de nomes, versões e estrutura

### Decisão
- Matrizes M01 e M02 tornadas públicas para permitir leitura sem autenticação

---

## [0.2] — 2026-05-26

### Adicionado
- Arquitetura do ecossistema definida: tipos M (Matriz), S (Skill), D (Documento)
- Conceito do SUMÁRIO como meta-repositório roteador
- Conceito de Matrizes como fontes de verdade consultadas por todas as skills
- Padrão de backlog com campos: tipo de alteração, autorizado por, exposição de motivos
- `saude-digital-taxonomia` (M02) integrada ao ecossistema

### Decisão
- Adotado padrão B (mínimo universal com extensões por tipo) para backlogs

---

## [0.1] — 2026-05-22

### Adicionado
- `saude-digital-taxonomia` v1.0 — primeiro repositório do ecossistema
  8 partes temáticas, 24 capítulos, 107 subtópicos de saúde digital
- `backlog-versoes.md` com padrão de rastreabilidade de alterações

### Contexto
- Semana 1 da DTD/SETIS como unidade formal
- Primeiro repositório GitHub criado pelo mantenedor
