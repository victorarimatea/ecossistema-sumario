# CONTEXTO.md — Ecossistema DTD/SETIS

**Versão:** v3.4 — 2026-06-06
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
| hub-aprendizagem | Repositório documental reflexivo — boas práticas, benchmarks e lições aprendidas da jornada de construção |

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
| S04 | skl-github-orquestracao | v2.7 — Garante consistência; verificações CONFIRMAR; escala SEV1–SEV4; 6-A expandida (ideias + conhecimento consolidado) |
| S05 | skl-transcricao-documental | Converte PDFs regulatórios em Markdown estruturado |
| S06 | skl-registro-reuniao | Transforma resumos de reunião em registros institucionais para o SEI |
| S07 | skl-briefing-saude-digital | Briefing periódico de saúde digital com classificação taxonômica |

### Documentos (D) — conteúdo institucional estruturado

| ID | Nome | Descrição |
|---|---|---|
| D01 | doc-governanca-ses-df | 28 documentos transcritos: legislação, portarias, resoluções e referências internacionais |
| D02 | mat-cadastro-ses-setis-dtd | Matriz de cadastros de referência da DTD/SETIS/SES-DF |
| D03 | hub-aprendizagem | Repositório documental reflexivo — boas práticas, benchmarks e lições aprendidas da construção do ecossistema DTD/SETIS |

### Workflows (W) — memória organizacional de processos

| ID | Nome | Descrição |
|---|---|---|
| W01 | wkf-transcricao-documental | Processo completo de transcrição de PDFs regulatórios |
| W02 | wkf-registro-reuniao | Processo de registro institucional de reunião (privado) |
| W03 | wkf-registro-sessao | v1.2 — Registro estruturado de sessões; inclui reconciliação com ROADMAP (Etapa 2-A) |
| W04 | wkf-roadmap-geral | v1.0 — Gestão de roadmap: ciclo semanal, staging area, diálogo estratégico, três camadas de curadoria |
| W05 | wkf-auditoria-consistencia | v1.2 — Auditoria de consistência em 5 camadas; independente da S04; sem token; apenas detecta e reporta
| W06 | wkf-sessao-agente | v1.0 — Protocolo de Sessão Assistida por Agente; processo pai do W03 e W05; governa abertura, trabalho e fechamento |

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


---

## Taxonomia e Glossário — distinção essencial

O ecossistema mantém dois instrumentos de conhecimento estrutural que coexistem
com propósitos distintos e complementares. Confundi-los é um erro comum — esta
seção existe para eliminá-lo.

### Taxonomia (M02 — `mat-saude-digital-taxonomia`)

A taxonomia é um **mapa de navegação temática**. Ela organiza o território
do conhecimento em Partes, capítulos e subtópicos — como o índice de um livro
técnico. Não define termos: **classifica assuntos**.

**Para que serve:**
- Classificar itens do briefing, documentos, projetos e entregas por tema
- Orientar buscas ("este assunto mora em qual parte do mapa?")
- Indexar conteúdo para recuperação futura
- Dar consistência à curadoria temática ao longo do tempo

**Quem usa:** A skill S07 (`skl-briefing-saude-digital`) usa a taxonomia para
atribuir tags `🏷️` a cada item do briefing. Exemplo: uma notícia sobre FDA
aprovando algoritmo de IA para leitura de ECG recebe `🏷️ 3.1 · 3.5 · 18.2`
— indicando que o assunto pertence aos capítulos de IA em diagnóstico por
imagem, regulação de IA médica e dispositivos SaMD. A taxonomia não diz
*o que é* IA em diagnóstico: diz *onde esse assunto está* no mapa.

**Exemplos de entradas na taxonomia:**
- `3.1 IA em diagnóstico por imagem e patologia digital`
- `7.1 Consultas remotas — modelos síncronos e assíncronos`
- `11.1 Legislações globais: LGPD, GDPR, HIPAA e equivalentes`
- `18.1 Dispositivos de software como produto médico (SaMD)`

Cada entrada é um **endereço temático**, não uma definição.

---

### Glossário (M01 — `hub-fonte/GLOSSARIO.md`)

O glossário é um **dicionário de definições**. Cada entrada responde à
pergunta: *"O que é isso?"*. Não organiza territórios: **define conceitos**.

**Para que serve:**
- Garantir que todos os agentes e colaboradores usem os mesmos termos
  com o mesmo significado
- Eliminar ambiguidade semântica em documentos, skills e workflows
- Ser consultado antes de redigir qualquer documento institucional
- Ser a fonte de verdade quando há dúvida sobre o significado de um termo

**Quem usa:** A S04 (`skl-github-orquestracao`) realiza auditoria de glossário
ao final de toda operação — varredura dos arquivos criados ou alterados em
busca de termos novos não definidos. A S03 (`skl-poc-saude-digital`) e a S06
(`skl-registro-reuniao`) consultam o glossário para garantir uso correto de
termos institucionais em documentos formais.

**Exemplos de entradas no glossário:**
- `Interoperabilidade` → *"Capacidade de dois ou mais dispositivos ou sistemas
  para trocar informações e utilizá-las para a correta execução de uma função
  especificada sem alterar o conteúdo dos dados."*
- `SaMD` → *"Software destinado a finalidades médicas que realiza essas funções
  sem fazer parte do hardware de um dispositivo médico."*
- `Drift documental` → *"Condição em que dois ou mais arquivos do ecossistema
  que deveriam estar sincronizados passam a apresentar informações divergentes
  por falta de propagação de uma atualização."*
- `Radar Institucional` → definição proprietária do ecossistema DTD/SETIS,
  não encontrada em outras fontes.

---

### A aparente redundância — por que não é um problema

Alguns termos aparecem tanto na taxonomia quanto no glossário. Isso é correto
e intencional — são usos diferentes do mesmo conceito:

| Termo | Na taxonomia | No glossário |
|---|---|---|
| Interoperabilidade | `4.2` — endereço temático de notícias e documentos sobre interoperabilidade | Definição formal do conceito para uso em documentos institucionais |
| Telemedicina | `7.x` — capítulo de cuidado virtual | Definição normativa extraída da regulação brasileira |
| SaMD | `18.1` — subtópico de regulação de software médico | Definição técnica para uso em PoCs e documentos formais |
| IA Generativa | `3.3` — subtópico de LLMs na medicina | Definição formal para uso em documentos do ecossistema |

**Regra de uso para agentes de IA:**
- Precisa *classificar* um assunto? → Use a taxonomia (M02). Atribua o código
  do subtópico mais específico disponível.
- Precisa *definir* ou *verificar o significado* de um termo? → Use o glossário
  (M01/GLOSSARIO.md). Nunca invente uma definição se o termo já está aqui.
- Precisa fazer as duas coisas? → Use os dois instrumentos de forma independente.
  A classificação taxonômica e a definição glossarial de um mesmo termo coexistem
  sem conflito.

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
