# DECISÕES — Ecossistema DTD/SETIS

Registro das grandes decisões arquiteturais e de design do projeto.
Cada decisão documenta: contexto, alternativas consideradas e motivo da escolha.

Formato inspirado em ADR (Architecture Decision Records), adaptado para
o contexto de gestão pública.

---

## D001 — GitHub como plataforma de memória institucional

**Data:** 2026-05-22
**Status:** Vigente

**Contexto:**
Necessidade de criar memória institucional para a DTD que sobrevivesse
a mudanças de servidor, de gestão e de ferramentas. O conhecimento
precisava ser acessível tanto por humanos quanto por agentes de IA.

**Alternativas consideradas:**
- SharePoint / OneDrive institucional — dependente de infraestrutura SES-DF
- Notion — plataforma proprietária, risco de descontinuação
- Google Drive — boa para humanos, difícil de consumir por agentes de IA
- GitHub — padrão da indústria para documentação técnica versionada

**Decisão:** GitHub com repositórios em Markdown.

**Motivo:** versionamento nativo, diff de alterações, acessível por API,
legível por agentes de IA, custo zero, padrão universal reconhecido.

---

## D002 — Separação entre tipo de repositório e nome

**Data:** 2026-05-26
**Status:** Vigente

**Contexto:**
Ao definir a nomenclatura dos repositórios, havia a opção de incluir
o tipo (M, S, D) no nome (ex: `matriz-taxonomia`) ou apenas no sumário.

**Alternativas consideradas:**
- Prefixo no nome: `matriz-saude-digital-taxonomia` — nomes longos, redundância
- Sufixo no nome: `saude-digital-taxonomia-m` — confuso, não é convencional
- Tipo apenas no sumário: `saude-digital-taxonomia` — nomes curtos e legíveis

**Decisão:** Tipo apenas no sumário, nome sem prefixo de tipo.

**Motivo:** nomes mais curtos são mais fáceis de lembrar, digitar e referenciar.
O sumário é a fonte de verdade para o tipo — não é preciso duplicar essa
informação no nome.

---

## D003 — Matrizes públicas, skills privadas (por padrão)

**Data:** 2026-05-26
**Status:** Vigente

**Contexto:**
Skills contêm lógica de negócio e protocolos de execução que podem
revelar vulnerabilidades se públicos. Matrizes são fontes de verdade
sem informação sensível.

**Decisão:** Matrizes públicas, skills privadas por padrão.

**Motivo:** matrizes públicas permitem leitura sem autenticação (essencial
para que o Claude acesse sem token). Skills privadas protegem a lógica
de automação. Exceção: `skill-criador-de-skills` é pública por ser
documentação de processo, não de lógica sensível.

---

## D004 — Padrão B de backlog (mínimo com extensões por tipo)

**Data:** 2026-05-26
**Status:** Vigente

**Contexto:**
O backlog da `saude-digital-taxonomia` tinha campos mais ricos que o
padrão mínimo definido na `nomenclatura.md`. Havia conflito entre
consistência e riqueza de informação.

**Alternativas consideradas:**
- Opção A: padrão único simplificado para todos — consistência total,
  perda de riqueza nos backlogs especializados
- Opção B: mínimo obrigatório + extensões por tipo — consistência base
  com riqueza onde necessário

**Decisão:** Opção B.

**Motivo:** backlogs de matrizes de conhecimento precisam de campos como
"Fonte" e "Proposto por" para rastreabilidade científica. Backlogs de
skills precisam de "Skills afetadas" para rastrear impacto em cascata.
O mínimo garante que qualquer repositório seja auditável; as extensões
garantem que cada tipo seja auditável da forma mais adequada à sua natureza.

---

## D005 — IAC como instrumento de dois modos (V e H)

**Data:** 2026-05-27
**Status:** Vigente

**Contexto:**
O IAC foi criado inicialmente como instrumento de análise vertical
(comparação entre versões do mesmo documento — IAC-V). Durante a
preparação para o SGTD, surgiu a necessidade de analisar a conformidade
entre o PDTIC e o PTD-SES — uma análise de natureza diferente.

**Alternativas consideradas:**
- Criar um instrumento totalmente novo para análise horizontal
- Expandir o IAC para cobrir os dois modos dentro do mesmo modelo

**Decisão:** Expandir o IAC para dois modos (V e H) dentro do mesmo modelo.

**Motivo:** os dois modos compartilham a mesma estrutura de capa, ficha
técnica, sumário e lógica de encaminhamentos. Criar um instrumento
separado duplicaria a infraestrutura sem necessidade. O nome IAC-V e
IAC-H é suficientemente claro para distinguir os casos de uso.

---

## D006 — Repositório mãe público como portfólio institucional

**Data:** 2026-05-27
**Status:** Vigente

**Contexto:**
O ecossistema estava distribuído em repositórios funcionais sem uma
entrada pública que explicasse o projeto como um todo. Havia necessidade
de um ponto de entrada para visitantes externos e para inicialização
de novas sessões de trabalho.

**Alternativas consideradas:**
- Usar o `ecossistema-sumario` como repositório mãe — confunde função
  técnica (sumário para skills) com função pública (portfólio)
- Criar repositório `dtd-setis` dedicado — separação clara de propósitos

**Decisão:** Criar `dtd-setis` como repositório mãe público.

**Motivo:** o `ecossistema-sumario` é infraestrutura técnica consultada
por agentes de IA. O `dtd-setis` é comunicação pública e portfólio.
Misturar os dois comprometeria ambas as funções. A separação também
permite que o repositório mãe seja transferido para uma organização
GitHub da SES-DF no futuro sem afetar o funcionamento do ecossistema.
