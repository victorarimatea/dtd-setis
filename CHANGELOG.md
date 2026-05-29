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
