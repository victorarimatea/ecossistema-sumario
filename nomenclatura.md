# Matriz de Nomenclatura do Ecossistema DTD/SETIS

**Versão:** v0.2 — 2026-05-26
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

nome-da-skill/
├── README.md
├── SKILL.md
├── backlog-versoes.md
└── exemplos/
└── exemplo-01.md

---

## 5. Estrutura do backlog-versoes.md

Padrão obrigatório para todos os repositórios:

    # Backlog de Versões — [nome-do-repositorio]

    ## vX.Y — AAAA-MM-DD

    **Tipo de alteração:** [Criação | Adição | Correção | Atualização | Remoção]
    **Autorizado por:** victorarimatea
    **Exposição de motivos:** [descrição objetiva do porquê da mudança]

    ### Alterações realizadas
    - item 1
    - item 2

---

## 6. Regras de atualização do ecossistema

1. Nenhum repositório é criado sem entrada correspondente em `sumario.md`
2. Nenhum arquivo obrigatório pode ser renomeado sem atualização do `sumario.md`
3. Toda alteração em Matrizes (tipo M) requer registro em `backlog-versoes.md`
4. Skills devem verificar sua própria entrada no `sumario.md` a cada execução
   e solicitar autorização ao mantenedor caso encontrem divergência

---

## 7. Extensões de backlog por tipo de repositório

O formato definido na Seção 5 é o mínimo obrigatório para todos os
repositórios. Cada tipo pode estender esse formato com campos adicionais
conforme sua natureza.

### 7.1 Matrizes de conhecimento (ex: taxonomias, glossários)

Campos adicionais obrigatórios para este tipo:

| Campo | Valores possíveis |
|---|---|
| `**Tópico afetado**` | Código e nome do tópico alterado |
| `**Fonte**` | Evidência que motivou a mudança |
| `**Proposto por**` | `sistema` ou `manual` |

Inclui também duas seções fixas ao final do arquivo:

- `## Alterações Pendentes (Backlog)` — propostas geradas por skills
  aguardando autorização do mantenedor
- `## Notas de Revisão Futura` — observações para próximas versões

**Repositório de referência:** `saude-digital-taxonomia`

### 7.2 Skills (tipo S)

Campos adicionais obrigatórios para este tipo:

| Campo | Valores possíveis |
|---|---|
| `**Impacto**` | `breaking` (incompatível) ou `non-breaking` (compatível) |
| `**Skills afetadas**` | Lista de skills do ecossistema impactadas pela mudança |

**Repositório de referência:** a ser definido na criação da primeira skill.

### 7.3 Documentos institucionais (tipo D)

Campos adicionais obrigatórios para este tipo:

| Campo | Valores possíveis |
|---|---|
| `**Instrumento de aprovação**` | ATA, Despacho, Portaria, etc. |
| `**Processo SEI**` | Número do processo relacionado |
| `**IAC gerado**` | Referência ao IAC que documentou a revisão |

**Repositório de referência:** a ser definido na criação do `pdtic-historico`.
