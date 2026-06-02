# CONTEXTO.md — Ecossistema DTD/SETIS

**Versão:** v1.7 — 2026-06-02
**Mantenedor:** victorarimatea
**Propósito:** Briefing completo para inicialização de novas sessões de trabalho.
Leia este arquivo antes de qualquer outra ação.

> **Escopo deste arquivo:** descreve a *estrutura durável* do ecossistema — quem
> o mantém, do que é feito, suas convenções, o modelo IAC e a governança da
> SES-DF relevante. **Não registra estado operacional transitório** (datas de
> reunião, versões em tramitação, status "aguarda"). Esse conteúdo vive em
> `backlog-acoes-dtd.md` (histórico retrospectivo) e na agenda do mantenedor
> (calendário prospectivo). Critério de inclusão: *se uma sessão ler isto daqui
> a seis meses, continua verdadeiro e útil?*

---

## Quem é o mantenedor

**Victor Leonardo Arimatea Queiroz**
Diretor de Transformação Digital — Diretoria de Transformação Digital (DTD)
Secretaria Executiva de Tecnologia da Informação em Saúde (SETIS)
Secretaria de Estado de Saúde do Distrito Federal (SES-DF)
Matrícula: 1657757-4

A DTD foi criada em outubro de 2025. Victor é o único servidor da unidade no momento —
toda a construção deste ecossistema é trabalho individual, desenvolvido em
paralelo com projetos institucionais de moderada a alta complexidade.

---

## O que é este ecossistema

Um sistema de automação e governança documental construído do zero, combinando:
- Repositórios GitHub como memória institucional permanente
- Skills do Claude como agentes de automação especializados
- Matrizes de conhecimento como fontes de verdade compartilhadas
- Instrumentos padronizados (IAC) como produtos de governança

O objetivo de longo prazo é que uma única instrução possa acionar múltiplas
skills, consultar vários repositórios, produzir documentos institucionais
completos e registrar tudo em backlogs auditáveis — com mínima intervenção
manual do mantenedor.

---

## Estrutura atual do ecossistema

> Snapshot de estrutura — atualizado conforme repositórios são criados ou versionados.

### Repositórios ativos

| ID | Tipo | Nome | Versão | Descrição |
|---|---|---|---|---|
| — | Portfólio | dtd-setis | v0.9 | Repositório-mãe público: porta de entrada, MANIFESTO, ROADMAP, CHANGELOG, DECISOES |
| M01 | Matriz | ecossistema-sumario | v0.22 | Âncora: sumário, nomenclatura, contexto, protocolo de atualizações, histórico de ações |
| M02 | Matriz | saude-digital-taxonomia | v1.0 | Taxonomia estruturada de saúde digital |
| S01 | Skill | skill-criador-de-skills | v1.0 | Cria novos repositórios de skill via API GitHub |
| S02 | Skill | skill-iac-pdtic | v2.0 | Gera IAC-V e IAC-H do PDTIC da SES-DF |
| S03 | Skill | skill-poc-saude-digital | v1.0 | Gera documentos de PoC em saúde digital no padrão SES-DF/DTD |
| S04 | Skill | skill-github-orquestracao | v1.6 | Garante consistência do ecossistema a cada operação |
| S05 | Skill | skill-transcricao-documental | v1.0 | Converte PDFs regulatórios em Markdown estruturado |
| S06 | Skill | skill-registro-reuniao | v1.0 | Transforma resumos de reunião em registros institucionais padronizados para o SEI |
| D01 | Documento | governanca-ses-df | v1.0 | 28 documentos transcritos — legislação e referências de saúde digital |
| D02 | Documento | doc-cadastro-ses-setis-dtd | v1.0 | Matriz de Cadastros de referência DTD/SETIS/SES-DF |
| W01 | Workflow | workflow-transcricao-documental | v1.0 | Processo de transcrição documental — memória organizacional do pipeline |
| W02 | Workflow | workflow-registro-reuniao | v1.0 | Processo de registro institucional de reunião — PLAUD NOTE → Markdown → SEI (privado) |
| P01 | Projeto | telessaude-poc-prisional | v0.1 | PoC Totem de Telemedicina no Sistema Prisional do DF (privado) |
| A01 | Agenda | agenda-dtd | v1.0 | Acervo cronológico de registros de reunião da DTD (privado) |

### Repositórios planejados (não criados ainda)

| Tipo | Nome sugerido | Propósito |
|---|---|---|
| D | governanca-ses-df | Matrizes normativas: Portaria 193/2024, PTD-SES, base normativa de saúde digital |
| D | pdtic-historico | Histórico de versões do PDTIC com IACs gerados |
| S | skill-iac-generico | IAC para qualquer par de documentos (versão sem especialização temática) |

---

## Convenções do ecossistema

### Nomenclatura de repositórios
`[dominio]-[especificidade]` em kebab-case minúsculo.
O tipo (M/S/D) não entra no nome — fica registrado no sumário.

### Versionamento
`vMAJOR.MINOR — AAAA-MM-DD`
MAJOR sobe em mudanças incompatíveis com versões anteriores.
MINOR sobe em melhorias e correções.

### Arquivos obrigatórios em todo repositório
`README.md`, `backlog-versoes.md`
Skills (tipo S) adicionam: `SKILL.md`
Matriz M01 adiciona: `sumario.md`, `nomenclatura.md`, `CONTEXTO.md`, `protocolo-atualizacoes.md`, `backlog-acoes-dtd.md`

### Backlogs
Há dois tipos de backlog no ecossistema, com propósitos distintos:
- **`backlog-versoes.md`** — registra alterações *no próprio repositório/documento*.
  Campos obrigatórios: Tipo de alteração, Autorizado por, Exposição de motivos.
  Matrizes de conhecimento usam campos adicionais: Tópico afetado, Fonte, Proposto por.
- **`backlog-acoes-dtd.md`** (M01) — registra *ações e produtos institucionais da DTD*
  ao longo do tempo. Base para relatórios de atividade consolidados. Esquema próprio
  descrito no cabeçalho do arquivo.

Em ambos: entrada mais recente sempre no topo.

### Protocolo de encerramento
Toda operação de escrita em repositórios segue o `protocolo-atualizacoes.md` (M01),
que define checklists por tipo de operação (OP-A a OP-F) e um relatório de
encerramento obrigatório antes de declarar qualquer trabalho concluído.

---

## O modelo IAC — Instrumento de Análise Comparativa

Padrão de governança documental criado pela DTD/SETIS. Versão atual: **v0.2**.

### Dois modos

**IAC-V (Vertical):** compara versões do mesmo documento.
Pergunta central: *O que mudou?*
Exemplo: PDTIC v1.5 → v1.8

**IAC-H (Horizontal):** verifica conformidade entre documentos distintos.
Pergunta central: *Estão alinhados?*
Exemplo: PDTIC × PTD-SES 2024-2027

### Estrutura obrigatória (ambos os modos)
Capa com ficha técnica → Sumário → Apresentação → Contexto normativo →
Análise (modificações ou convergências/lacunas) → Encaminhamentos/Recomendações →
Modelo IAC para uso futuro

### Regras críticas de linguagem institucional
- O **SGTD** revisa, manifesta, recomenda e encaminha. NUNCA delibera.
- **Deliberação** sobre planos compete ao **Fórum de Subsecretários** (Art. 7º, I — Portaria 193/2024).
- Documentos institucionais registram **constatações técnicas**, nunca a origem de manifestações.

---

## Estrutura de governança da SES-DF relevante para o ecossistema

### Portaria nº 193/2024 — CIG/SES
- **CIG/SES:** colegiado consultivo do Secretário de Estado
- **Fórum de Subsecretários:** delibera sobre planos e programas (Art. 7º, I)
  — instância que **aprova formalmente** o PDTIC
- **SGTD** (Subcomitê VI): revisa PDTIC e PTD, encaminha ao Fórum (Art. 34, VIII)
  — Victor é presidente do SGTD como Diretor de Transformação Digital

### Instrumentos de planejamento
- **PDTIC 2024-2027:** plano de TIC da SES-DF.
  - Aprovação: Fórum de Subsecretários (via SGTD) → portal da SES-DF
  - Versões e tramitação são rastreadas em `pdtic-historico` (planejado) e no `backlog-acoes-dtd.md`
- **PTD-SES 2024-2027:** plano de transformação digital com impacto assistencial
  - Aprovação: CGTD/SEEC (nível GDF — Portaria 718/2024)
- Processo SEI de referência: 00060-00227811/2026-80

---

## Lições técnicas incorporadas às skills

Conhecimento de engenharia durável, válido para qualquer sessão que toque o pipeline de geração de DOCX:
- Acentuação completa em português requer duas rodadas de substituição no pipeline Node.js/DOCX
- Títulos de seções precisam de correção individual além da substituição global
- Verificação automática do DOCX gerado é obrigatória antes de entregar

---

## Histórico de ações e produtos

O registro retrospectivo do que a DTD produziu (documentos IAC, PoCs, articulações,
configurações do ecossistema) é mantido em **`backlog-acoes-dtd.md`** (M01),
fonte única para relatórios de atividade consolidados. Este arquivo não duplica
esse conteúdo.

---

## Próximos passos planejados

1. **Criar repositório `governanca-ses-df`** com Portaria 193/2024, PTD-SES,
   base normativa de saúde digital e matriz de competências institucionais
2. **Atualizar `skill-iac-pdtic`** para consultar `governanca-ses-df` na Etapa 1
3. **Criar repositório `pdtic-historico`** para registrar versões aprovadas do PDTIC
   com os IACs correspondentes
4. **Criar `skill-iac-generico`** — versão sem especialização temática do IAC
5. **Configurar o ecossistema como Projeto no Claude** carregando os SKILL.md
   para ativação permanente das skills
6. **Migrar a escrita em repositórios para GitHub MCP** quando disponível
   nativamente no Claude — elimina a necessidade de Personal Access Token

---

## Como iniciar uma nova sessão de trabalho

Cole no início da conversa:

```
Leia https://raw.githubusercontent.com/victorarimatea/ecossistema-sumario/main/CONTEXTO.md
e me diga o que entendeu sobre o ecossistema antes de começarmos.
```

O Claude vai absorver todo o contexto e você continua de onde parou.

---

## Protocolo obrigatório para operações no GitHub

### Regra 1 — Autodescoberta da skill de orquestração

Toda sessão que resulte em criação ou alteração de arquivos nos repositórios
do ecossistema deve obrigatoriamente seguir a **skill-github-orquestracao (S04)**
antes de qualquer execução.

**Repositório:** https://github.com/victorarimatea/skill-github-orquestracao

Esta regra se aplica **independentemente de o usuário mencioná-la**. Se o Claude
identificar que a sessão vai resultar em operações no GitHub e a S04 não foi
referenciada, deve pausar, informar o usuário e acionar a skill antes de prosseguir.

O fluxo de autodescoberta funciona assim:
1. Usuário apresenta qualquer link do ecossistema no início da sessão
2. Claude lê este CONTEXTO.md durante a inicialização
3. Claude registra internamente que S04 é obrigatória para operações no GitHub
4. Quando a sessão encaminhar para alterações em repositórios, Claude aciona
   a S04 automaticamente — sem depender da memória do usuário

### Regra 2 — Aprendizado contínuo e atualização automática da S04

Todo erro, aprendizado ou melhoria identificado durante a execução de uma
operação no GitHub deve atualizar a skill-github-orquestracao (S04) **na
mesma sessão**, antes do encerramento.

**O que dispara a atualização:**

| Tipo | Critério |
|---|---|
| **Erro** | Qualquer inconsistência encontrada durante a execução que não estava prevista nas verificações existentes da S04 |
| **Aprendizado** | Qualquer padrão, sequência ou verificação que funcionou bem e merece ser preservado como regra permanente |
| **Melhoria** | Qualquer ajuste de fluxo que reduziu passos, evitou retrabalho ou aumentou confiabilidade da execução |

**Regra de encerramento:** antes de emitir o relatório final (Etapa 7 da S04),
o Claude deve verificar se houve qualquer um dos três tipos acima. Se sim,
propõe atualização da S04 como parte obrigatória do encerramento — não como
item opcional. A versão da S04 é incrementada (MINOR), o `backlog-versoes.md`
da skill é atualizado, e o `sumario.md` do M01 reflete a nova versão.

**Objetivo:** garantir que o erro nunca se repita e que o aprendizado nunca
fique preso em uma única sessão. O ecossistema melhora a cada operação.

---

## Tecnologias e acessos relevantes

- **GitHub:** github.com/victorarimatea (públicos: dtd-setis, ecossistema-sumario, saude-digital-taxonomia, skill-criador-de-skills, skill-poc-saude-digital; privado: skill-iac-pdtic)
- **API GitHub:** Personal Access Token com permissão `repo` — gerado sob demanda, revogar após uso. Migração para fine-grained PAT (Contents read/write, escopo mínimo, expiração curta) e depois GitHub MCP é o caminho-alvo
- **Claude:** claude.ai — projeto "Ecossistema DTD/SETIS" com arquivos do PDTIC carregados
- **Documentos no projeto Claude:** PDTIC v1.5, PDTIC v1.8, Decreto 48.503/2026, Processo SEI 00060-00227811/2026-80, Portaria 193/2024, Portaria 718/2024, PTD-SES 2024-2027
