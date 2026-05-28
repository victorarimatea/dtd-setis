# Arquitetura do Ecossistema DTD/SETIS

**Versão:** v1.0 — 2026-05-27

---

## Visão geral

O ecossistema é composto por três camadas que trabalham juntas:

```
┌─────────────────────────────────────────────────┐
│  CAMADA DE INTERFACE                             │
│  Claude.ai — conversas no Projeto DTD/SETIS      │
│  Skills carregadas via Project Knowledge         │
└─────────────────────┬───────────────────────────┘
                      │ lê / escreve
┌─────────────────────▼───────────────────────────┐
│  CAMADA DE CONHECIMENTO (GitHub)                 │
│                                                  │
│  Matrizes (M)    Skills (S)    Documentos (D)    │
│  ────────────    ──────────    ─────────────      │
│  M01 sumário     S01 criador   D01 governança    │
│  M02 taxonomia   S02 iac-pdtic (planejado)       │
└─────────────────────┬───────────────────────────┘
                      │ produz
┌─────────────────────▼───────────────────────────┐
│  CAMADA DE PRODUTO                               │
│  Documentos IAC (DOCX + PDF)                     │
│  Backlogs auditáveis                             │
│  Repositórios atualizados automaticamente        │
└─────────────────────────────────────────────────┘
```

---

## Tipos de repositório

### Matrizes (M) — fontes de verdade

Repositórios públicos consultados por todas as skills antes de qualquer ação.
Nunca são alterados sem autorização explícita do mantenedor.

| ID | Repositório | Conteúdo principal |
|---|---|---|
| M01 | ecossistema-sumario | Sumário de todos os repositórios, convenções de nomenclatura, contexto do ecossistema |
| M02 | saude-digital-taxonomia | Taxonomia estruturada de saúde digital em 107 subtópicos |

### Skills (S) — agentes especializados

Cada repositório de skill contém um `SKILL.md` que o Claude lê como
instrução de execução. Quando carregado em um Projeto do Claude,
a skill é ativada automaticamente em qualquer conversa daquele projeto.

| ID | Repositório | Função | Modo |
|---|---|---|---|
| S01 | skill-criador-de-skills | Cria repositórios de skill via API GitHub | Automático |
| S02 | skill-iac-pdtic | Gera IAC do PDTIC | IAC-V e IAC-H |

### Documentos (D) — memória institucional

Repositórios que armazenam documentos institucionais vivos, versionados
e consultáveis por skills.

*(Nenhum criado ainda — ver ROADMAP.md)*

---

## Fluxo de criação de uma nova skill

```
1. Usuário solicita: "Cria skill X com função Y"
         │
2. S01 lê M01/sumario.md e M01/nomenclatura.md
         │
3. S01 valida nome, verifica duplicatas
         │
4. S01 apresenta plano e solicita confirmação
         │
5. Usuário confirma + fornece token GitHub
         │
6. S01 cria repositório via API
   S01 cria README.md, SKILL.md, backlog-versoes.md
   S01 atualiza M01/sumario.md
   S01 atualiza M01/backlog-versoes.md
         │
7. S01 entrega relatório final
```

---

## Fluxo de geração de um IAC

```
1. Usuário solicita: "Gera IAC-V do PDTIC v1.5 → v1.8"
         │
2. S02 lê M01/sumario.md e M01/nomenclatura.md
   S02 verifica própria entrada no sumário
         │
3. S02 identifica modo (V ou H) e solicita documentos
         │
4. S02 lê os documentos integralmente
         │
5. S02 executa análise comparativa sistemática
         │
6. S02 gera documento IAC (DOCX + PDF)
   com acentuação correta, estrutura padronizada,
   linguagem regimental precisa
         │
7. S02 entrega os arquivos
   Pergunta se registra no pdtic-historico (D)
```

---

## Protocolo de acesso à API GitHub

As skills que escrevem no GitHub usam Personal Access Token (PAT):
- Permissão mínima necessária: `repo` (leitura e escrita em repositórios)
- O token é fornecido pelo usuário no momento da execução
- Nunca é armazenado — usado apenas na sessão corrente
- Deve ser revogado após cada sessão de uso

Leitura de repositórios públicos não requer token.

---

## Convenções técnicas

### Versionamento semântico adaptado
`vMAJOR.MINOR — AAAA-MM-DD`
- MAJOR: mudança incompatível com versões anteriores
- MINOR: melhoria ou correção compatível

### Encoding de documentos para API GitHub
Todos os arquivos são enviados em Base64 (`base64 -w 0`).
O SHA do arquivo atual deve ser obtido antes de qualquer atualização
para evitar conflitos (erro 409 da API).

### Geração de documentos DOCX/PDF
Pipeline: JavaScript (Node.js + docx library) → DOCX → LibreOffice (soffice) → PDF
Acentuação: duas rodadas de substituição + verificação automática do DOCX gerado.
