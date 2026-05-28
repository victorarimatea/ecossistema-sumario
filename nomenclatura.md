# Matriz de Nomenclatura do Ecossistema DTD/SETIS

**Versão:** v0.4 — 2026-05-27
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
---

## 8. Modelo IAC — Instrumento de Análise Comparativa

O IAC é o instrumento padrão de governança documental do ecossistema DTD/SETIS.
Deve ser utilizado sempre que houver necessidade de análise formal entre documentos.

### 8.1 Versão do modelo

O modelo IAC é versionado independentemente dos documentos que analisa.
Formato: `IAC vMAJOR.MINOR — AAAA-MM-DD`
Versão atual: `IAC v0.2 — 2026-05-27`

### 8.2 Modos de análise

| Modo | Sigla | Quando usar |
|---|---|---|
| Análise Comparativa Vertical | IAC-V | Comparar versões diferentes do mesmo documento |
| Análise Comparativa Horizontal | IAC-H | Verificar conformidade entre documentos distintos |

### 8.3 Estrutura obrigatória de todo IAC

Todo IAC deve conter obrigatoriamente, nesta ordem:

1. Capa institucional com ficha técnica completa (tipo, modo, autor, destinatários, processo SEI)
2. Sumário
3. Apresentação e objetivo do documento
4. Contexto normativo
5. Panorama quantitativo comparativo
6. Análise detalhada (modificações para IAC-V / convergências e lacunas para IAC-H)
7. Encaminhamentos ou recomendações
8. Modelo IAC — padrão para uso futuro

### 8.4 Nomenclatura de arquivos IAC

Formato: `[SIGLA-DOCUMENTO]_IAC-[MODO]_v[VERSAO]_[AAAA-MM-DD].[ext]`

Exemplos:
- `PDTIC_IAC-V_v02_2026-05-27.pdf` — IAC Vertical do PDTIC, versão 0.2
- `PDTIC_PTD_IAC-H_v01_2026-05-27.pdf` — IAC Horizontal PDTIC × PTD, versão 0.1



---

## 9. Padrão de acentuação em documentos gerados

Todo documento DOCX/PDF produzido por qualquer skill do ecossistema deve
seguir o protocolo de correção de acentuação em português antes da entrega.

### Protocolo obrigatório (3 etapas)

**Etapa A — Substituição global no script**
Aplicar substituição global de palavras sem acentuação no código antes
de executar o script de geração. Ver lista completa de palavras no
SKILL.md de cada skill geradora.

**Etapa B — Correção individual de títulos**
Verificar e corrigir cada título de seção individualmente após a
substituição global, pois títulos usam funções separadas no código.

**Etapa C — Verificação automática do DOCX**
Executar script Python de verificação no DOCX gerado antes de converter
para PDF. Se encontrar palavras sem acento, voltar à Etapa A.

### Regra de entrega

Nenhum documento é entregue sem passar pelas 3 etapas com sucesso.
A conversão para PDF só ocorre após a Etapa C confirmar zero ocorrências
de palavras sem acentuação.

### Skills que implementam este padrão
- `skill-criador-de-skills` (S01) — garante que novas skills nasçam com a regra
- `skill-iac-pdtic` (S02) — aplica nas gerações IAC-V e IAC-H
