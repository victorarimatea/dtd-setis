# Roadmap — DTD/SETIS/SES-DF

**Última atualização:** 2026-06-02
**Versão do ecossistema:** CHANGELOG [2.3] | S04 v1.8

---

## ✅ Concluído

### Fase 1 — Fundação do ecossistema
- ✅ Repositório âncora `hub-fonte` (M01) com sumário, nomenclatura,
  glossário, CONTEXTO.md e protocolo de operações
- ✅ Portfólio público `hub-entrada` com MANIFESTO, ROADMAP, CHANGELOG, DECISOES
- ✅ Taxonomia de saúde digital `mat-saude-digital-taxonomia` (M02)
- ✅ Skill criador de skills `skl-criador-de-skills` (S01)

### Fase 2 — Instrumentos institucionais
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
- ✅ Tipo A (Agendas) formalizado — indexação cronológica, data_reuniao vs
  data_registro, estrutura reunioes/AAAA/MM/
- ✅ `agd-dtd` (A01) — acervo cronológico de reuniões da DTD
- ✅ `skl-registro-reuniao` (S06) — transformação de resumos em registros
  institucionais padronizados para o SEI
- ✅ GLOSSARIO.md com 8 categorias e 34+ termos formais
- ✅ Saneamento de drifts e auditoria cruzada de consistência (Erro #007)

---

## 🔄 Em andamento

- 🔄 P01 `prj-telessaude-poc-prisional` — PoC aguardando definição de unidade
  piloto (12 deliberações pendentes, ver README.md do P01)
- 🔄 Upload e transcrição dos documentos pendentes no D01 (itens 10–17 do §9
  do WORKFLOW-ESPECIFICACAO.md)

---

## 🎯 Próxima ação imediata

**Criar `pdtic-historico` (D — tipo Documento):**
Repositório para versionamento histórico do PDTIC da SES-DF com IACs gerados.
Habilitará o uso pleno da `skl-iac-pdtic` (S02) no ecossistema.

---

## 📅 Médio prazo

- Criar `workflow-iac-conformidade` (W03) — análise de conformidade documental
  automatizada, consumindo D01 e S02 como subprocessos
- Criar `governanca-ses-df-fase3` — transcrição dos documentos 10–17 pendentes
- Evoluir S05 para fase sequencial autônoma (condição: PASSOU ≥ 95% em ≥ 10 docs)
- Integração SEI via API quando disponível (roadmap longo prazo)
- Calendário visual sobre A01 (`agd-dtd`) — visualização de reuniões

---

## 🔭 Longo prazo

- GitHub MCP para operações autenticadas sem PAT manual
- Migração de PAT clássico para fine-grained com escopos mínimos e expiração curta
- Replicação do modelo de ecossistema para outras unidades da SES-DF
- Case institucional documentado para publicação
