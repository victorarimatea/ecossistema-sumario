# Matriz de Nomenclatura do Ecossistema DTD/SETIS

**Versão:** v1.0 — 2026-06-02
**Mantenedor:** victorarimatea

> Define as convenções obrigatórias de nomenclatura para todos os
> repositórios, arquivos e versões do ecossistema. Toda skill e todo
> repositório criado deve estar em conformidade com este documento.
>
> **Nota:** Para definições dos termos utilizados neste documento
> (matriz, skill, projeto, IAC, PoC, drift, OP-X etc.), consulte o
> [`GLOSSARIO.md`](./GLOSSARIO.md) do repositório âncora.

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
- `telessaude-poc-prisional`

**Regras:**
- Apenas letras minúsculas, números e hífens
- Sem espaços, underscores ou caracteres especiais
- Sem prefixos de tipo (não use `matriz-`, `skill-doc-`, `proj-`, etc.)
- Nome deve ser autoexplicativo sem precisar abrir o repositório

---

## 2. Nomenclatura de arquivos obrigatórios

Todo repositório do ecossistema deve conter estes arquivos na raiz:

| Arquivo | Obrigatório em | Função |
|---|---|---|
| `README.md` | Todos | Apresentação pública do repositório |
| `backlog-versoes.md` | Todos | Histórico auditável de alterações |
| `SKILL.md` | Skills (tipo S) | Documentação técnica da skill para o Claude |
| `WORKFLOW.md` | Workflows (tipo W) | Documento principal do processo — 8 seções obrigatórias |
| `EXECUCOES.md` | Projetos (tipo P) | Índice de workflows acionados no projeto, com links para logs no repositório W |
| `sumario.md` | Apenas M01 | Índice central do ecossistema |
| `nomenclatura.md` | Apenas M01 | Este arquivo |
| `CONTEXTO.md` | Apenas M01 | Briefing de inicialização de sessões |
| `protocolo-atualizacoes.md` | Apenas M01 | Protocolo obrigatório de encerramento de operações |
| `backlog-acoes-dtd.md` | Apenas M01 | Histórico retrospectivo de ações e produtos da DTD |

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

## 4-A. Estrutura interna de projetos (tipo P)

Todo repositório de projeto deve ser **privado** e conter esta estrutura:

```
nome-do-projeto/
├── README.md
├── backlog-versoes.md
├── stakeholders.md
├── reunioes/
│   └── AAAA-MM-DD-[assunto-resumido].md
└── documentos/
    └── [artefatos aprovados: PoCs, memorandos, pareceres, relatórios]
```

### Arquivos obrigatórios de projetos

| Arquivo / Pasta | Função |
|---|---|
| `README.md` | Ficha técnica: nome, status, período, responsáveis, processo SEI de referência |
| `backlog-versoes.md` | Registro histórico de todas as decisões tomadas ao longo do projeto |
| `stakeholders.md` | Todos os profissionais envolvidos: papel, instituição, período e nível de envolvimento |
| `reunioes/` | Atas estruturadas — uma por reunião, nomeadas `AAAA-MM-DD-[assunto].md` |
| `documentos/` | Artefatos produzidos e aprovados pelo projeto |

### Ciclo de vida dos projetos

O campo `status` no `sumario.md` segue vocabulário controlado:

```
ideia → planejado → em_execucao → entregue
                              ↘ cancelado
                              ↘ suspenso
```

### Visibilidade e monitoramento público

Repositórios de projeto são **sempre privados**. A visibilidade pública
de um projeto é gerenciada exclusivamente pelo repositório `dtd-setis`,
na pasta `projetos/monitoramento.md`, mediante autorização explícita do
Diretor de Transformação Digital. A documentação interna do projeto
(linguagem técnica, siglas, deliberações em curso) não é exposta
diretamente ao público — apenas uma visão panorâmica curada.

---

## 4-B. Estrutura interna de workflows (tipo W)

Todo repositório de workflow deve ser **público** (por padrão) e conter esta estrutura:

```
workflow-[descritor]/
├── README.md
├── WORKFLOW.md
├── INDICE.md
├── backlog-versoes.md
└── execucoes/
    └── AAAA-MM-DD-[contexto].md
```

### Arquivos obrigatórios de workflows

| Arquivo / Pasta | Função |
|---|---|
| `README.md` | Apresentação pública: tipo W, ID, versão, links para skill associada e repositório de saída |
| `WORKFLOW.md` | Documento principal com 8 seções obrigatórias (ver estrutura abaixo) |
| `INDICE.md` | Mapa completo de arquivos incluindo pasta execucoes/ |
| `backlog-versoes.md` | Histórico de evoluções do processo com exposição de motivos |
| `execucoes/` | Pasta para logs de execução — um arquivo por execução registrada |

### Estrutura obrigatória do WORKFLOW.md (8 seções)

| Seção | Conteúdo |
|---|---|
| 1 — Identificação | Nome, ID, versão, status, responsável, skill associada, repositório de saída |
| 2 — Missão e contexto | Por que existe, problema resolvido, objetivos estratégicos, quem pode acionar |
| 3 — Estado final esperado | Critérios de qualidade verificáveis — benchmark de execução bem-sucedida |
| 4 — Etapas do processo | Sequência completa: executor, tipo (manual/auto), entrada, saída, critério de conclusão |
| 5 — Skills e subprocessos | Lista de skills e workflows consumidos, com links — nunca replicar conteúdo |
| 6 — Histórico de problemas | Memória institucional: P01, P02... com sintoma, causa raiz, solução, status |
| 7 — Roadmap de automação | Estado atual de cada etapa e condições para progressão |
| 8 — Referências e dependências | Documentos normativos, repositórios D e M referenciados |

### Nomenclatura do repositório W

**Formato:** `workflow-[descritor-do-processo]` em kebab-case minúsculo.

O prefixo `workflow-` é fixo e obrigatório. O descritor nomeia o processo,
não a tecnologia. Exemplos: `workflow-transcricao-documental`,
`workflow-iac-conformidade`, `workflow-poc-saude-digital`.

### Ciclo de vida dos workflows

```
rascunho → ativo → suspenso → descontinuado
```

- `rascunho`: em documentação, ainda não executado formalmente
- `ativo`: documentado e em uso
- `suspenso`: pausado temporariamente (motivo registrado no backlog)
- `descontinuado`: encerrado — arquivo preservado para histórico

### Logs de execução

**Localização:** `workflow-[descritor]/execucoes/AAAA-MM-DD-[contexto].md`

**Conteúdo obrigatório de cada log:**
- Data, hora e contexto de acionamento
- Quem/o que acionou (humano, projeto, outro workflow)
- Projeto associado, se houver (com link para repositório P)
- Resumo do que foi executado etapa a etapa
- Decisões tomadas e desvios do padrão
- Skills e subworkflows consumidos
- Artefatos gerados (com links)
- Status: `Completo` / `Parcial` / `Interrompido`
- Lições aprendidas (candidatas a P0N na Seção 6 do WORKFLOW.md)

**Obrigatoriedade:** logs são obrigatórios em sessões autenticadas com token
onde o Coordenador estiver presente. Sessões sem token são isentas.

### EXECUCOES.md no projeto associado (tipo P)

Quando um workflow é acionado no contexto de um projeto (tipo P), o repositório
do projeto deve manter um `EXECUCOES.md` na raiz com uma linha por workflow acionado.
Este arquivo **não duplica** o log — apenas referencia o log completo no repositório W.

```markdown
| Data       | Workflow                         | Contexto              | Log completo |
|------------|----------------------------------|-----------------------|--------------|
| 2026-06-02 | workflow-transcricao-documental  | Geração PoC v0.1      | → link       |
```


## 4-C. Estrutura interna de agendas (tipo A)

Todo repositório de agenda deve ser **privado** (por padrão) e conter esta estrutura:

```
agenda-[unidade]/
├── README.md
├── INDICE.md              ← índice cronológico por data de reunião
├── backlog-versoes.md
└── reunioes/
    └── AAAA/
        └── MM/
            └── AAAA-MM-DD-[CLASSIFICACAO]-[descricao].md
```

### Diferencial do tipo A: indexação por tempo de ocorrência

O tipo A é o único tipo do ecossistema indexado por **tempo de ocorrência**
dos eventos — não pela ordem de criação no ecossistema.

- A estrutura de pastas `reunioes/AAAA/MM/` garante ordenação cronológica natural
- O nome do arquivo começa com `AAAA-MM-DD` — qualquer listagem já é uma linha do tempo
- O INDICE.md lista reuniões em ordem de ocorrência, não de inserção no repositório
- O ID sequencial (A01, A02...) é usado apenas no sumário do ecossistema

### Dois campos de data obrigatórios no Front Matter YAML

```yaml
data_reuniao:    AAAA-MM-DD    # quando a reunião aconteceu
data_registro:   AAAA-MM-DD    # quando o arquivo foi inserido no repositório
```

A `data_reuniao` determina a posição no índice e na estrutura de pastas.
A `data_registro` é informação de rastreabilidade — registrada também
automaticamente no histórico de commits do git.

### Nomenclatura do repositório A

**Formato:** `agenda-[unidade]` em kebab-case minúsculo.

O prefixo `agenda-` é fixo e obrigatório. A unidade identifica a área
responsável. Exemplos: `agenda-dtd`, `agenda-gessp`, `agenda-diraps`.

### Nomenclatura dos arquivos de reunião

**Formato:** `AAAA-MM-DD-[CLASSIFICACAO]-[descricao-curta].md`

Classificações possíveis (sem acentos, em maiúsculas):
- `ALINHAMENTO-ESTRATEGICO`
- `ALINHAMENTO-TATICO`
- `ALINHAMENTO-OPERACIONAL`
- `ALINHAMENTO-TECNICO`
- `ALINHAMENTO-TECNICO-OPERACIONAL`
- `ALINHAMENTO-TECNICO-ESTRATEGICO`

Exemplos:
- `2026-06-02-ALINHAMENTO-ESTRATEGICO-telessaude-poc-prisional.md`
- `2026-05-05-ALINHAMENTO-TECNICO-OPERACIONAL-totem-health360-seape.md`

### Relação com projetos (tipo P)

Quando uma reunião é associada a um projeto formal, o arquivo fica no
repositório A e uma referência é criada no `EXECUCOES.md` do projeto P.
Nunca duplicar o conteúdo — apenas referenciar. Mesma lógica do tipo W.

### Ciclo de vida dos registros de reunião

Registros de reunião não têm ciclo de vida — são imutáveis após criação.
Correções são feitas via nova versão do arquivo com nota de revisão no
Front Matter (`versao_registro: 1.1` + nota explicativa).


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

### 5.1 Backlog de ações da DTD (backlog-acoes-dtd.md)

Arquivo obrigatório apenas em M01. Distinto do `backlog-versoes.md`: enquanto o
backlog de versões registra alterações *no repositório*, o backlog de ações
registra *ações e produtos institucionais da DTD* (documentos IAC, PoCs,
articulações, configurações do ecossistema) ao longo do tempo. É a fonte única
para relatórios de atividade consolidados.

- Entrada mais recente sempre no topo.
- Itens prospectivos (reuniões, prazos) não entram — viram entrada após executados.
- O esquema de campos é definido no cabeçalho do próprio arquivo.

---

## 10. Índices locais de repositório

Todo repositório do ecossistema deve conter um **INDICE.md** na raiz,
independentemente do número de arquivos ou presença de subpastas.

### 10.1 Propósito

O INDICE.md permite que qualquer ferramenta automatizada ou humano
entenda rapidamente o que existe no repositório e chegue ao recurso
certo sem precisar ler todos os arquivos. É especialmente importante
em repositórios com conteúdo rico, subpastas ou muitos artefatos
acumulados ao longo do tempo — evitando consumo desnecessário de
créditos e tempo de navegação.

### 10.2 Estrutura obrigatória

```markdown
# Índice — [nome-do-repositório]

**Última atualização:** AAAA-MM-DD
**Total de arquivos:** N

## Arquivos na raiz

| Arquivo | Descrição | Função no ecossistema |
|---|---|---|
| `README.md` | Apresentação e navegação | Porta de entrada do repositório |
| `INDICE.md` | Este arquivo | Mapa completo de conteúdo |
| `backlog-versoes.md` | Histórico de versões | Rastreabilidade e auditoria |
| ... | ... | ... |

## Subpastas (se existirem)

| Pasta | Conteúdo | Quando consultar |
|---|---|---|
| `references/` | Documentos de referência | Ao buscar exemplos e modelos |
| ... | ... | ... |
```

### 10.3 Regras de manutenção

- O INDICE.md deve ser **atualizado a cada novo arquivo ou pasta criada**
- A atualização do INDICE.md é item obrigatório nas checklists OP-A e OP-P da S04
- A data de "Última atualização" deve refletir a data real da última modificação
- Arquivos descontinuados permanecem no índice com marcação `~~arquivo~~` e nota

### 10.4 Criação retroativa

Repositórios existentes que ainda não possuem INDICE.md devem recebê-lo
na primeira operação que os tocar, mesmo que essa não seja a operação principal.
A criação do INDICE.md em repositório existente é classificada como OP-E.


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

### 7.4 Projetos (tipo P)

Campos adicionais obrigatórios para este tipo:

| Campo | Valores possíveis |
|---|---|
| `**Status**` | `ideia` / `planejado` / `em_execucao` / `entregue` / `cancelado` / `suspenso` |
| `**Processo SEI**` | Número do processo administrativo de referência |
| `**Parceiros institucionais**` | Instituições envolvidas na entrega |

### 7.5 Workflows (tipo W)

Campos adicionais obrigatórios para este tipo:

| Campo | Valores possíveis |
|---|---|
| `**Status do workflow**` | `rascunho` / `ativo` / `suspenso` / `descontinuado` |
| `**Execuções afetadas**` | IDs ou datas das execuções impactadas pela mudança, se aplicável |
| `**Skills afetadas**` | Skills que consomem este workflow e podem precisar de ajuste |


### 7.6 Agendas (tipo A)

Campos adicionais obrigatórios para este tipo:

| Campo | Valores possíveis |
|---|---|
| `**Reuniões afetadas**` | Datas das reuniões impactadas pela mudança, se aplicável |
| `**Motivo de revisão**` | Apenas quando um registro de reunião existente for corrigido |


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
