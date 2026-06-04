# CONTEXTO.md — Ecossistema DTD/SETIS

**Versão:** v2.1 — 2026-06-04
**Mantenedor:** victorarimatea
**Propósito:** Briefing estrutural para inicialização de sessões de trabalho.
Leia este arquivo antes de qualquer ação. Para onboarding externo, leia ONBOARDING.md.

---

## Mensagem do mantenedor — para novos colaboradores e agentes externos

*Se você não é Victor Arimatea, bem-vindo ao Ecossistema DTD/SETIS.*

Este ecossistema foi construído com um propósito simples: demonstrar que é
possível fazer gestão pública de qualidade mesmo quando os recursos são
escassos, desde que haja método, padronização e tecnologia a serviço do
propósito institucional.

O que você encontra aqui é uma infraestrutura viva de automação e governança
documental — repositórios que se conectam entre si, skills especializadas que
se acionam umas às outras, workflows desenhados com cuidado para entregar
documentos institucionais com qualidade técnica, rastreabilidade completa e
conformidade normativa.

A maior parte do ecossistema é pública e está disponível para uso.
Quanto mais for utilizado, mais maduro e capaz ele se torna.

Sinta-se bem-vindo. O ONBOARDING.md vai orientá-lo pelo caminho certo
a partir do seu propósito.

— Victor Leonardo Arimatea Queiroz
Diretor de Transformação Digital — DTD/SETIS/SES-DF

---

## Quem é o mantenedor

**Victor Leonardo Arimatea Queiroz**
Diretor de Transformação Digital — Diretoria de Transformação Digital (DTD)
Secretaria Executiva de Tecnologia da Informação em Saúde (SETIS)
Secretaria de Estado de Saúde do Distrito Federal (SES-DF)

A DTD foi criada em outubro de 2025. Victor é o único servidor da unidade —
toda a construção deste ecossistema é trabalho individual, desenvolvido
em paralelo com projetos institucionais de alta complexidade.

---

## O que é este ecossistema

Um sistema de automação e governança documental construído do zero,
combinando:

- **Repositórios GitHub** como memória institucional permanente e auditável
- **Skills do Claude** como agentes de automação especializados
- **Matrizes de conhecimento** como fontes de verdade compartilhadas
- **Instrumentos padronizados** (IAC, PoC) como produtos de governança

O objetivo de longo prazo é que uma única instrução possa acionar múltiplas
skills, consultar repositórios especializados, produzir documentos
institucionais completos e registrar tudo em backlogs auditáveis —
com mínima intervenção manual do mantenedor.

---

## Estrutura do ecossistema

### Portfólio público

| Nome | Descrição |
|---|---|
| hub-entrada | Porta de entrada pública: MANIFESTO, ROADMAP, CHANGELOG, monitoramento de projetos |

### Matrizes (M) — fontes de verdade estruturais

| ID | Nome | Descrição |
|---|---|---|
| M01 | hub-fonte | Âncora do ecossistema: sumário, nomenclatura, glossário, contexto |
| M02 | mat-saude-digital-taxonomia | Taxonomia estruturada de saúde digital |

### Skills (S) — agentes de automação especializados

| ID | Nome | Descrição |
|---|---|---|
| S01 | skl-criador-de-skills | Cria novos repositórios de skill via API GitHub |
| S02 | skl-iac-pdtic | Gera IAC-V e IAC-H do PDTIC da SES-DF (privado) |
| S03 | skl-poc-saude-digital | Gera documentos de PoC em saúde digital no padrão SES-DF |
| S04 | skl-github-orquestracao | Garante consistência do ecossistema a cada operação |
| S05 | skl-transcricao-documental | Converte PDFs regulatórios em Markdown estruturado |
| S06 | skl-registro-reuniao | Transforma resumos de reunião em registros institucionais para o SEI |
| S07 | skl-briefing-saude-digital | Briefing periódico de saúde digital com classificação taxonômica |

### Documentos (D) — conteúdo institucional estruturado

| ID | Nome | Descrição |
|---|---|---|
| D01 | doc-governanca-ses-df | 28 documentos transcritos: legislação, portarias, resoluções e referências internacionais |
| D02 | mat-cadastro-ses-setis-dtd | Matriz de cadastros de referência da DTD/SETIS/SES-DF |

### Workflows (W) — memória organizacional de processos

| ID | Nome | Descrição |
|---|---|---|
| W01 | wkf-transcricao-documental | Processo completo de transcrição de PDFs regulatórios |
| W02 | wkf-registro-reuniao | Processo de registro institucional de reunião (privado) |
| W03 | wkf-registro-sessao | Registro estruturado de sessões de trabalho intensivo |

### Agendas (A) — acervos cronológicos

| ID | Nome | Descrição |
|---|---|---|
| A01 | agd-dtd | Acervo institucional de reuniões da DTD, ordenado por data de ocorrência (privado) |

### Projetos (P) — iniciativas formais da DTD

| ID | Nome | Status | Descrição |
|---|---|---|---|
| P01 | prj-telessaude-poc-prisional | em_execucao | PoC de totem de telemedicina no Sistema Prisional do DF (privado) |
| P02 | hub-memoria | em_execucao | Memória viva da construção do próprio ecossistema (privado) |

---

## Convenções obrigatórias

### Nomenclatura de repositórios
Formato: `[dominio]-[especificidade]` em kebab-case minúsculo.
O tipo (M/S/D/W/A/P) não entra no nome — fica registrado no `sumario.md`.
Referência completa: `nomenclatura.md`

### Versionamento
Formato: `vMAJOR.MINOR — AAAA-MM-DD`
MAJOR sobe em mudanças incompatíveis com versões anteriores.
MINOR sobe em melhorias e correções.

### Arquivos obrigatórios em todo repositório
`README.md`, `INDICE.md`, `backlog-versoes.md`
Skills (S) adicionam: `SKILL.md`
Workflows (W) adicionam: `WORKFLOW.md`, pasta `execucoes/`
Projetos (P) adicionam: `stakeholders.md`, `EXECUCOES.md`, pastas `reunioes/` e `documentos/`
M01 adiciona: `sumario.md`, `nomenclatura.md`, `CONTEXTO.md`, `GLOSSARIO.md`, `ONBOARDING.md`

### Toda operação no ecossistema passa pela S04
A skill de orquestração (`skl-github-orquestracao`) é acionada
automaticamente para qualquer alteração nos repositórios. Ela garante
que nenhum arquivo fique desatualizado por esquecimento.

---

## Governança da SES-DF relevante para o ecossistema

### Portaria nº 193/2024 — CIG/SES
- **CIG/SES:** colegiado consultivo do Secretário de Estado
- **Fórum de Subsecretários:** instância que delibera sobre planos e programas (Art. 7º, I)
- **SGTD** (Subcomitê VI): revisa PDTIC e PTD, encaminha ao Fórum (Art. 34, VIII)
  — Victor preside o SGTD como Diretor de Transformação Digital

### Instrumentos de planejamento
- **PDTIC 2024-2027:** Plano Diretor de TIC da SES-DF
  — aprovação: Fórum de Subsecretários (via SGTD)
- **PTD-SES 2024-2027:** Plano de Transformação Digital com impacto assistencial
  — aprovação: CGTD/SEEC (nível GDF — Portaria 718/2024)

### Regras críticas de linguagem institucional
- O **SGTD** revisa, manifesta, recomenda e encaminha. **Nunca delibera.**
- **Deliberação** sobre planos compete ao **Fórum de Subsecretários.**
- Documentos institucionais registram **constatações técnicas**, nunca a origem de manifestações.

---

## Como iniciar uma nova sessão de trabalho

Cole no início da conversa:

```
Leia https://raw.githubusercontent.com/victorarimatea/hub-fonte/main/CONTEXTO.md
e me diga o que entendeu sobre o ecossistema antes de começarmos.
```

Para onboarding de novos colaboradores ou agentes externos:

```
Leia https://raw.githubusercontent.com/victorarimatea/hub-fonte/main/ONBOARDING.md
e me diga qual é o seu propósito antes de começarmos.
```
