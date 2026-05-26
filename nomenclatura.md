# Matriz de Nomenclatura do Ecossistema DTD/SETIS

**Versão:** v0.1 — 2026-05-26
**Mantenedor:** victorarimatea

> Define as convenções obrigatórias de nomenclatura para todos os
> repositórios, arquivos e versões do ecossistema. Toda skill e todo
> repositório criado deve estar em conformidade com este documento.

---

## 1. Nomenclatura de repositórios

**Formato:** `[dominio]-[especificidade]` em kebab-case minúsculo.

O tipo do repositório **não entra no nome** — ele é registrado no
`sumario.md`. Isso mantém os nomes curtos e legíveis.

**Exemplos corretos:**
- `ecossistema-sumario`
- `saude-digital-taxonomia`
- `skill-iac-pdtic`
- `pdtic-historico`

**Regras:**
- Apenas letras minúsculas, números e hífens
- Sem espaços, underscores ou caracteres especiais
- Sem prefixos de tipo (não use `matriz-`, `skill-doc-`, etc.)
- Nome deve ser autoexplicativo sem precisar abrir o repositório

---

## 2. Nomenclatura de arquivos obrigatórios

Todo repositório do ecossistema deve conter estes arquivos na raiz:

| Arquivo | Obrigatório em | Função |
|---|---|---|
| `README.md` | Todos | Apresentação pública do repositório |
| `backlog-versoes.md` | Todos | Histórico auditável de alterações |
| `SKILL.md` | Skills (tipo S) | Documentação técnica da skill para o Claude |
| `sumario.md` | Apenas M01 | Índice central do ecossistema |
| `nomenclatura.md` | Apenas M01 | Este arquivo |

---

## 3. Versionamento de documentos e skills

**Formato:** `vMAJOR.MINOR — AAAA-MM-DD`

| Componente | Quando incrementar |
|---|---|
| MAJOR | Mudança que torna versões anteriores incompatíveis ou inválidas |
| MINOR | Melhorias, adições e correções compatíveis com versão anterior |
| Data | Data de finalização da versão, não de início do trabalho |

**Exemplos:**
- `v1.0 — 2026-05-22` ← primeira versão estável
- `v1.1 — 2026-05-26` ← melhoria menor
- `v2.0 — 2026-06-10` ← mudança estrutural

**Quando incluir hora:** apenas se houver mais de uma versão no mesmo
dia, acrescente ` HH:MM` ao final. Ex: `v1.2 — 2026-05-26 14:30`

---

## 4. Estrutura interna de skills (tipo S)

Todo repositório de skill deve ter esta estrutura:
