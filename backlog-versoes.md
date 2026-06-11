## 2026-06-11 — Roteamento do design do ciclo de sessão (ROADMAP + staging)

**Tipo de alteração:** Atualização estrutural (registro de design)
**Autorizado por:** Victor Leonardo Arimatea Queiroz
**Timestamp:** 2026-06-11T20:42:00-03:00
**Exposição de motivos:** Sessão de design conceitual conduziu, por etapas e como
discussão de princípios, ao desenho do relatório de encerramento de sessão, do
Bloco de Handoff e dos ritos de condução. Quatro decisões de arquitetura foram
amadurecidas; três ideias emergentes foram deliberadamente retidas para não
sequestrar o fio em andamento (princípio "a velocidade pode ser nossa inimiga").
Esta operação roteia cada peça ao seu lar canônico: decisões fechadas ao ROADMAP,
ideias ainda embrionárias à staging. Nenhuma alteração na fonte de verdade
(sumario.md) nem em workflows — puro registro.

### Alterações realizadas
- `ROADMAP.md` — bloco "Formalização do ciclo de sessão" criado no Médio prazo
  com 3 metas fechadas (estrutura do relatório no W03; localização do handoff no
  W06; convergência como estado+resíduo SEV)
- `ROADMAP.md` — meta autônoma "Reclassificação W03 e fronteira skill↔workflow"
  registrada separadamente, por conter decisão de design pendente (não só execução)
- `ROADMAP.md` — cabeçalho: última atualização 2026-06-08 → 2026-06-11
- `staging.md` — 3 ideias adicionadas à Seção C (status pendente): memória de
  domínio do briefing; contribuição externa via issues públicas; disciplina de
  Arquitetura do Conhecimento
- `CHANGELOG.md` — entrada de 2026-06-11 documentando o roteamento

### Vínculos registrados
- Meta autônoma (reclassificação W03) ↔ Ideia C (Arquitetura do Conhecimento):
  mesma família de questão; provável abordagem conjunta em sessão evolutiva
- Ideia A (memória do briefing) ↔ "Handoff qualificado" (já na Seção C): lógica
  de acervo consultável
- Ideia C ↔ "Modularização da S04" (já na Seção C): respostas ao mesmo inchaço

---

## 2026-06-05 — staging.md reformulada

**Tipo de alteração:** Atualização estrutural
**Autorizado por:** Victor Leonardo Arimatea Queiroz
**Exposição de motivos:** Reformulação completa da staging.md para incorporar
os aprendizados da sessão de 2026-06-05. Painel de situação com contagem
dinâmica (sem números fixos — calculado a cada leitura para evitar drift
estrutural). Alertas de acúmulo e hiato embutidos como instruções de leitura.
Seção E criada para conhecimentos consolidados destinados ao hub-aprendizagem,
com Intenção do Comandante e critérios de elegibilidade próprios. Coluna
Status adicionada na Seção C. Visão de longo prazo registrada.

### Alterações realizadas
- Painel de Situação dinâmico adicionado (Abordagem 1 — contagem calculada)
- Alertas de acúmulo (≥5 pendentes) e hiato (>7 dias) embutidos
- Seção E — Conhecimentos consolidados criada com instrução completa
- Coluna Status adicionada na tabela da Seção C
- Entradas da Seção A atualizadas com registros de 2026-06-05
- Ideia de visão de longo prazo registrada na Seção C

---

## v2.0 — 2026-06-02

**Tipo de alteração:** Atualização + Saneamento
**Autorizado por:** victorarimatea
**Exposição de motivos:** Saneamento de drifts identificados em auditoria
externa (diagnóstico por ferramenta LLM). Causa raiz: S04 não instruía
atualização de CONTEXTO.md, ROADMAP.md e arquitetura.md em todos os tipos
de operação. Resultado: arquivos centrais acumularam versões defasadas ao
longo de duas sessões intensas de implementação. Corrigido com reescrita
da arquitetura.md (v2.0), reorganização do ROADMAP.md e blindagem
estrutural da S04 com Erro #007 e Verificação 5.

### Alterações realizadas nesta versão
- `docs/arquitetura.md` → v2.0: reescrita completa com 6 tipos, 4 camadas,
  relações entre tipos e S04
- `ROADMAP.md`: reorganizado em concluído/em curso/próximo/médio/longo prazo
- `INDICE.md`: contagem e estrutura atualizadas
- `backlog-versoes.md`: entradas retroativas v1.1–v1.9 adicionadas

---

## v1.9 — 2026-06-02 (retroativo)

**Tipo de alteração:** Adição
**Exposição de motivos:** Tipo A (Agenda) implementado. S06 e W02 criados.
Implementação do workflow de registro de reunião com PLAUD NOTE Pro.
Ver CHANGELOG [2.3].

---

## v1.8 — 2026-06-02 (retroativo)

**Tipo de alteração:** Adição
**Exposição de motivos:** Tipo W (Workflows) implementado. W01 criado como
caso zero. P01 recebeu EXECUCOES.md. S04 atualizada para v1.6 com OP-W.
Ver CHANGELOG [2.2].

---

## v1.7 — 2026-06-02 (retroativo)

**Tipo de alteração:** Adição
**Exposição de motivos:** Migração do Cowork concluída. D01, D02, S05
registrados. 28 documentos transcritos no D01. Ver CHANGELOG [2.0].

---

## v1.6 — 2026-06-02 (retroativo)

**Tipo de alteração:** Adição
**Exposição de motivos:** GLOSSARIO.md criado com 8 categorias. S04 v1.4
com Verificação 4 (auditoria de glossário). Ver CHANGELOG [1.7] e [1.9].

---

## v1.5 — 2026-06-01 (retroativo)

**Tipo de alteração:** Correção
**Exposição de motivos:** Saneamento de drifts durante diagnóstico de
maturidade. INDICE.md criado em todos os repositórios públicos. Protocolo
descontinuado em favor da S04. Ver CHANGELOG [1.4] a [1.6].

---

## v1.4 — 2026-06-01 (retroativo)

**Tipo de alteração:** Adição
**Exposição de motivos:** S04 criada (v1.0). Primeiro repositório de
orquestração do ecossistema. CONTEXTO.md com regras de autodescoberta
e aprendizado contínuo. Ver CHANGELOG [1.0] a [1.3].

---

## v1.3 — 2026-06-01 (retroativo)

**Tipo de alteração:** Adição
**Exposição de motivos:** P01 telessaude-poc-prisional criado. Tipo P
formalizado no ecossistema. Pasta projetos/ criada no dtd-setis.
Ver CHANGELOG anterior.

---

## v1.2 — 2026-05-29 (retroativo)

**Tipo de alteração:** Adição
**Exposição de motivos:** IAC-V e IAC-H do PDTIC produzidos via S02.
ROADMAP e DECISOES evoluídos. Ver CHANGELOG v0.9.

---

## v1.1 — 2026-05-27 (retroativo)

**Tipo de alteração:** Adição
**Exposição de motivos:** S01, S02 adicionadas ao ecossistema. M02
saude-digital-taxonomia criado. Ver CHANGELOG v0.6–v0.8.

---

# Backlog de Versões — dtd-setis

**Versão:** v1.0 — 2026-06-01
**Repositório:** https://github.com/victorarimatea/dtd-setis
**Mantenedor:** victorarimatea

> Registro histórico de decisões e motivações por trás de cada alteração
> neste repositório. Complementa o CHANGELOG.md, que registra as entregas.
> Entradas anteriores a 2026-06-01 foram retroalimentadas com base no
> CHANGELOG existente na data de criação deste arquivo.

---

## v1.0 — 2026-06-01

**Tipo de alteração:** Criação
**Autorizado por:** victorarimatea
**Exposição de motivos:** Criação deste arquivo para suprir lacuna de
rastreabilidade identificada no diagnóstico de maturidade do ecossistema
(2026-06-01). O dtd-setis é o único repositório ativo que não possuía
backlog-versoes.md, em violação da nomenclatura.md que o define como
obrigatório em todos os repositórios. As entradas abaixo foram
retroalimentadas com base no CHANGELOG existente.

### Alterações realizadas
- Criação do arquivo `backlog-versoes.md` com histórico retroalimentado

---

## v0.9 — 2026-05-29 (retroalimentado)

**Tipo de alteração:** Atualização
**Autorizado por:** victorarimatea
**Exposição de motivos:** Evolução do portfólio público com adição de
documentação de suporte ao PDTIC e atualização do ROADMAP e DECISOES.

---

## v0.8 — 2026-05-28 (retroalimentado)

**Tipo de alteração:** Atualização
**Autorizado por:** victorarimatea
**Exposição de motivos:** Adição de documentação sobre o IAC e registro
das primeiras entregas formais do ecossistema.

---

## v0.7 — 2026-05-28 (retroalimentado)

**Tipo de alteração:** Atualização
**Autorizado por:** victorarimatea
**Exposição de motivos:** Atualização do ROADMAP com novas fases e
refinamento do MANIFESTO com os princípios do ecossistema.

---

## v0.6 — 2026-05-27 (retroalimentado)

**Tipo de alteração:** Atualização
**Autorizado por:** victorarimatea
**Exposição de motivos:** Registro das primeiras skills (S01, S02) e
atualização do diagrama de arquitetura do ecossistema.

---

## v0.5 — 2026-05-27 (retroalimentado)

**Tipo de alteração:** Criação inicial do portfólio
**Autorizado por:** victorarimatea
**Exposição de motivos:** Criação do repositório dtd-setis como porta
de entrada pública do ecossistema DTD/SETIS. Estrutura inicial com
MANIFESTO, ROADMAP, CHANGELOG e DECISOES.

---
