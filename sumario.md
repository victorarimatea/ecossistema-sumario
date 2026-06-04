# Sumário do Ecossistema DTD/SETIS

**Versão:** v1.9 — 2026-06-03
**Repositório âncora:** ecossistema-sumario
**Mantenedor:** victorarimatea

---

## Repositórios Ativos

### Portfólio público (repositório-mãe)

| ID | Nome | Versão | Descrição |
|---|---|---|---|
| — | hub-entrada | v0.9 | Porta de entrada pública: MANIFESTO, ROADMAP, CHANGELOG, DECISOES, monitoramento de projetos |

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
| S04 | skl-github-orquestracao | v2.1 | Garante consistência do ecossistema a cada operação — plano, aprovação, execução, verificação |
| S05 | skl-transcricao-documental | v1.0 | Converte documentos PDF em Markdown estruturado seguindo o padrão DTD/SETIS/SES-DF (7 etapas, auto-verificação) |
| S06 | skl-registro-reuniao | v1.0 | Transforma resumos de reunião (PLAUD NOTE ou texto) em registros institucionais padronizados para o SEI | Converte documentos PDF em Markdown estruturado seguindo o padrão DTD/SETIS/SES-DF (7 etapas, auto-verificação) |

### Documentos (D)

| ID | Nome | Versão | Descrição |
|---|---|---|---|
| D01 | doc-governanca-ses-df | v1.0 | Transcrições estruturadas em Markdown de legislações, portarias, resoluções e referências internacionais de saúde digital — 28 documentos (Fase 1 + Fase 2 Tier 1) |
| D02 | mat-cadastro-ses-setis-dtd | v1.0 | Matriz de Cadastros de referência validada para uso interno da DTD/SETIS/SES-DF |

### Workflows (W)

| ID | Nome | Versão | Status | Descrição |
|---|---|---|---|---|
| W01 | wkf-transcricao-documental | v1.0 | ativo | Processo completo de transcrição de PDFs regulatórios em Markdown — memória organizacional do pipeline DTD/SETIS/SES-DF |
| W02 | wkf-registro-reuniao | v1.0 | ativo | Processo de registro institucional de reunião — PLAUD NOTE Pro → Markdown → SEI |
| W03 | wkf-registro-sessao | v1.0 | ativo | Registro estruturado de sessões de trabalho intensivo — preserva história da construção do ecossistema | Processo completo de transcrição de PDFs regulatórios em Markdown estruturado — memória organizacional do pipeline DTD/SETIS/SES-DF |

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
| D | doc-governanca-ses-df | Matrizes normativas: Portaria 193/2024, PTD-SES, base normativa de saúde digital |
| D | pdtic-historico | Histórico de versões do PDTIC com IACs gerados |
| S | skill-iac-generico | IAC para qualquer par de documentos (versão sem especialização temática) |

---

## Links rápidos

| Repositório | Tipo | Visibilidade | URL |
|---|---|---|---|
| hub-entrada | Portfólio | Público | https://github.com/victorarimatea/hub-entrada |
| hub-fonte | M01 | Público | https://github.com/victorarimatea/hub-fonte |
| mat-saude-digital-taxonomia | M02 | Público | https://github.com/victorarimatea/mat-saude-digital-taxonomia |
| skl-criador-de-skills | S01 | Público | https://github.com/victorarimatea/skl-criador-de-skills |
| skl-iac-pdtic | S02 | Privado | https://github.com/victorarimatea/skl-iac-pdtic |
| wkf-transcricao-documental | W01 | Público | https://github.com/victorarimatea/wkf-transcricao-documental |
| skl-poc-saude-digital | S03 | Público | https://github.com/victorarimatea/skl-poc-saude-digital |
| prj-telessaude-poc-prisional | P01 | Privado | https://github.com/victorarimatea/prj-telessaude-poc-prisional |
| doc-governanca-ses-df | D01 | Público | https://github.com/victorarimatea/doc-governanca-ses-df |
| mat-cadastro-ses-setis-dtd | D02 | Público | https://github.com/victorarimatea/mat-cadastro-ses-setis-dtd |
| skl-transcricao-documental | S05 | Público | https://github.com/victorarimatea/skl-transcricao-documental |
| skl-iac-pdtic | S02 | Privado | https://github.com/victorarimatea/skl-iac-pdtic |
| wkf-transcricao-documental | W01 | Público | https://github.com/victorarimatea/wkf-transcricao-documental |
| skl-github-orquestracao | S04 | Público | https://github.com/victorarimatea/skl-github-orquestracao |
