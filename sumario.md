# Sumário do Ecossistema DTD/SETIS

**Versão:** v2.2 — 2026-06-04
**Repositório âncora:** hub-fonte
**Mantenedor:** victorarimatea

---

## Repositórios Ativos

### Portfólio público (repositório-mãe)

| ID | Nome | Versão | Descrição |
|---|---|---|---|
| — | hub-entrada | v0.9 | Porta de entrada pública: MANIFESTO, ROADMAP, CHANGELOG, DECISOES, monitoramento de projetos |

### Infraestrutura de conhecimento

| ID | Nome | Versão | Descrição |
|---|---|---|---|
| — | hub-aprendizagem | v1.0 | Memória intelectual do ecossistema — boas práticas, benchmarks e lições aprendidas |

### Matrizes (M)

| ID | Nome | Versão | Descrição |
|---|---|---|---|
| M01 | hub-fonte | v0.24 | Âncora: sumário, nomenclatura, glossário, contexto, protocolo de atualizações, histórico de ações |
| M02 | mat-saude-digital-taxonomia | v1.0 | Taxonomia estruturada de saúde digital |

### Skills (S)

| ID | Nome | Versão | Descrição |
|---|---|---|---|
| S01 | skl-criador-de-skills | v1.0 | Cria novos repositórios de skill via API GitHub |
| S02 | skl-iac-pdtic | v2.0 | Gera IAC-V e IAC-H do PDTIC da SES-DF |
| S03 | skl-poc-saude-digital | v1.0 | Gera documentos de PoC em saúde digital no padrão SES-DF/DTD |
| S04 | skl-github-orquestracao | v2.7 | Garante consistência do ecossistema a cada operação — plano, aprovação, execução, verificação |
| S05 | skl-transcricao-documental | v1.0 | Converte documentos PDF em Markdown estruturado seguindo o padrão DTD/SETIS/SES-DF (7 etapas, auto-verificação) |
| S06 | skl-registro-reuniao | v1.0 | Transforma resumos de reunião (PLAUD NOTE ou texto) em registros institucionais padronizados para o SEI |
| S07 | skl-briefing-saude-digital | v1.0 | Briefing periódico de saúde digital — monitoramento de notícias, regulações, mercado e tecnologia com classificação taxonômica |

### Documentos (D)

| ID | Nome | Versão | Descrição |
|---|---|---|---|
| D01 | doc-governanca-ses-df | v1.0 | Transcrições estruturadas em Markdown de legislações, portarias, resoluções e referências internacionais de saúde digital — 28 documentos |
| D02 | mat-cadastro-ses-setis-dtd | v1.0 | Matriz de Cadastros de referência validada para uso interno da DTD/SETIS/SES-DF |

### Workflows (W)

| ID | Nome | Versão | Status | Descrição |
|---|---|---|---|---|
| W01 | wkf-transcricao-documental | v1.0 | ativo | Processo completo de transcrição de PDFs regulatórios em Markdown — memória organizacional do pipeline DTD/SETIS/SES-DF |
| W02 | wkf-registro-reuniao | v1.0 | ativo | Processo de registro institucional de reunião — PLAUD NOTE Pro → Markdown → SEI |
| W03 | wkf-registro-sessao | v1.2 |
| W04 | wkf-roadmap-geral | v1.0 | ativo | Registro estruturado de sessões de trabalho intensivo — preserva história da construção do ecossistema |
| W05 | wkf-auditoria-consistencia | v1.0 | ativo | Auditoria de consistência do ecossistema — verifica estado declarado vs real em 5 camadas; independente da S04 |

### Agendas (A)

| ID | Nome | Versão | Descrição |
|---|---|---|---|
| A01 | agd-dtd | v1.0 | Agenda institucional DTD/SETIS/SES-DF — registros de reunião ordenados cronologicamente por data de ocorrência (privado) |

### Projetos (P)

| ID | Nome | Versão | Status | Descrição |
|---|---|---|---|---|
| P01 | prj-telessaude-poc-prisional | v0.1 | em_execucao | PoC de totem de telemedicina multiparâmetros no Sistema Prisional do DF — DTD/SETIS/SES-DF |
| P02 | hub-memoria | v0.2 | em_execucao | Projeto do Ecossistema — preserva história da construção, decisões de design e relatórios de sessão (privado) |

---

## Repositórios Planejados

| Tipo | Nome sugerido | Propósito |
|---|---|---|
| D | pdtic-historico | Histórico de versões do PDTIC com IACs gerados |
| S | skl-iac-generico | IAC para qualquer par de documentos (versão sem especialização temática) |

---

## Links rápidos

| ID | Repositório | Tipo | Visibilidade | URL |
|---|---|---|---|---|
| — | hub-entrada | Portfólio | Público | https://github.com/victorarimatea/hub-entrada |
| M01 | hub-fonte | Matriz | Público | https://github.com/victorarimatea/hub-fonte |
| M02 | mat-saude-digital-taxonomia | Matriz | Público | https://github.com/victorarimatea/mat-saude-digital-taxonomia |
| S01 | skl-criador-de-skills | Skill | Público | https://github.com/victorarimatea/skl-criador-de-skills |
| S02 | skl-iac-pdtic | Skill | Privado | https://github.com/victorarimatea/skl-iac-pdtic |
| S03 | skl-poc-saude-digital | Skill | Público | https://github.com/victorarimatea/skl-poc-saude-digital |
| S04 | skl-github-orquestracao | Skill | Público | https://github.com/victorarimatea/skl-github-orquestracao |
| S05 | skl-transcricao-documental | Skill | Público | https://github.com/victorarimatea/skl-transcricao-documental |
| S06 | skl-registro-reuniao | Skill | Público | https://github.com/victorarimatea/skl-registro-reuniao |
| S07 | skl-briefing-saude-digital | Skill | Público | https://github.com/victorarimatea/skl-briefing-saude-digital |
| D01 | doc-governanca-ses-df | Documento | Público | https://github.com/victorarimatea/doc-governanca-ses-df |
| D02 | mat-cadastro-ses-setis-dtd | Documento | Público | https://github.com/victorarimatea/mat-cadastro-ses-setis-dtd |
| W01 | wkf-transcricao-documental | Workflow | Público | https://github.com/victorarimatea/wkf-transcricao-documental |
| W02 | wkf-registro-reuniao | Workflow | Privado | https://github.com/victorarimatea/wkf-registro-reuniao |
| W03 | wkf-registro-sessao | Workflow | Público | https://github.com/victorarimatea/wkf-registro-sessao |
| A01 | agd-dtd | Agenda | Privado | https://github.com/victorarimatea/agd-dtd |
| P01 | prj-telessaude-poc-prisional | Projeto | Privado | https://github.com/victorarimatea/prj-telessaude-poc-prisional |
| P02 | hub-memoria | Projeto | Privado | https://github.com/victorarimatea/hub-memoria |
