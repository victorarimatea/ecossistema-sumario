# Sumário do Ecossistema DTD/SETIS

**Versão:** v0.4 — 2026-05-26
**Mantenedor:** victorarimatea

> Fonte de verdade sobre todos os repositórios do ecossistema.
> Toda skill consulta este arquivo antes de executar qualquer tarefa.
> Alterações requerem autorização do mantenedor e registro no backlog.

---

## Como ler este sumário

Cada repositório tem um **Tipo**, que define seu papel no ecossistema:

| Tipo | Sigla | Função |
|---|---|---|
| Matriz | M | Fonte de verdade consultada por todas as skills |
| Skill | S | Documentação e lógica de uma skill específica |
| Documento Institucional | D | Documentos vivos analisados e versionados pelas skills |

---

## Repositórios ativos

### [M] Matrizes

| ID | Nome | URL | Descrição | Versão atual |
|---|---|---|---|---|
| M01 | ecossistema-sumario | https://github.com/victorarimatea/ecossistema-sumario | Índice central e convenções do ecossistema | v0.4 — 2026-05-26 |
| M02 | saude-digital-taxonomia | https://github.com/victorarimatea/saude-digital-taxonomia | Taxonomia estruturada de saúde digital | v1.0 — 2026-05-22 |

### [S] Skills

| ID | Nome | URL | Descrição | Versão atual |
|---|---|---|---|---|
| S01 | skill-criador-de-skills | https://github.com/victorarimatea/skill-criador-de-skills | Cria novas skills no ecossistema garantindo conformidade com nomenclatura.md e atualização automática do sumario.md | v1.0 — 2026-05-26 |
| S02 | skill-iac-pdtic | https://github.com/victorarimatea/skill-iac-pdtic | Gera o Instrumento de Análise Comparativa (IAC) do PDTIC 2024–2027 da SES-DF, comparando versões e produzindo documento padronizado para o SGTD | v1.0 — 2026-05-26 |

### [D] Documentos Institucionais

*Nenhum documento institucional registrado ainda.*

---

## Regra de atualização

Sempre que um novo repositório for criado no ecossistema, este arquivo
deve ser atualizado antes de o repositório ser considerado ativo.
A skill `skill-criador-de-skills` é responsável por propor essa
atualização e solicitar autorização ao mantenedor.
