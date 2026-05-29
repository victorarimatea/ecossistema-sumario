# backlog-acoes-dtd.md — Histórico de Ações e Produtos da DTD

**Repositório:** M01 — ecossistema-sumario
**Mantenedor:** victorarimatea
**Propósito:** Registro retrospectivo, datado e append-only das ações e produtos
institucionais da Diretoria de Transformação Digital (DTD/SETIS/SES-DF).
Fonte única para a consolidação de relatórios de atividade (mensais, anuais,
de prestação de contas).

---

## Como usar este backlog

- **Entrada mais recente sempre no topo.**
- Cada ação concluída ou iniciada gera uma entrada. Atualizações de status de uma
  ação já registrada editam a entrada existente (campo *Status*), não criam nova.
- Itens **prospectivos** (reuniões futuras, prazos) **não entram aqui** — eles
  vivem na agenda/calendário do mantenedor. Uma data agendada vira entrada de
  backlog *depois* de executada, registrando o resultado
  (ex.: "Fórum aprovou o PDTIC v1.8").
- Datas em formato `AAAA-MM-DD`. Quando o dia exato não for conhecido, usar
  `AAAA-MM` e marcar `[dia a confirmar]`.

### Esquema de entrada

Esquema próprio do backlog de ações, harmonizado com as convenções de backlog do
ecossistema (mantém *Autorizado por* e referência auditável):

- **Data** — `AAAA-MM-DD`
- **Ação** — verbo + objeto (o que foi feito)
- **Tipo** — `Produto documental` · `Articulação institucional` · `Configuração do ecossistema` · `Normativo` · `Outro`
- **Instrumento/Produto** — instrumento gerado e sua versão (quando aplicável)
- **Encaminhamento** — destino da ação (a quem/onde foi)
- **Status** — `Concluído` · `Em andamento` · `Aguardando`
- **Autorizado por** — instância ou responsável
- **Referência** — Processo SEI, repositório ou link auditável
- **Observações** — opcional

> Formato em blocos (não tabela) por ser mais limpo em diffs do Git e mais
> fácil de manter à mão. Os campos são uniformes, permitindo conversão
> programática para tabela na hora de montar um relatório.

### Modelo de entrada (copiar e preencher)

```
### AAAA-MM-DD — [título curto da ação]
- **Ação:**
- **Tipo:**
- **Instrumento/Produto:**
- **Encaminhamento:**
- **Status:**
- **Autorizado por:**
- **Referência:**
- **Observações:**
```

> **Nota de backfill:** ações de construção do ecossistema (criação dos
> repositórios, incorporação de skills, criação do protocolo de atualizações)
> estão registradas em `backlog-versoes.md` (M01) e no `CHANGELOG.md` do
> `dtd-setis`. Podem ser retroportadas para cá como entradas do tipo
> `Configuração do ecossistema` quando for útil para um relatório consolidado.

---

## Entradas

### 2026-05-27 — IAC-H de Conformidade PDTIC × PTD-SES
- **Ação:** Produzido IAC de Análise de Conformidade entre o PDTIC v1.8 e o PTD-SES 2024-2027
- **Tipo:** Produto documental
- **Instrumento/Produto:** IAC-H v0.1
- **Encaminhamento:** Aguarda distribuição
- **Status:** Aguardando
- **Autorizado por:** DTD/SETIS
- **Referência:** Processo SEI 00060-00227811/2026-80
- **Observações:** Análise horizontal de alinhamento. Índice global: 69% — parecer CONFORME COM RESSALVAS.

### 2026-05-27 — IAC-V de Revisão do PDTIC 2024-2027
- **Ação:** Produzido IAC de Análise de Revisão do PDTIC 2024-2027 (v1.5 → v1.8)
- **Tipo:** Produto documental
- **Instrumento/Produto:** IAC-V v0.2
- **Encaminhamento:** Distribuído aos membros do SGTD
- **Status:** Concluído
- **Autorizado por:** DTD/SETIS
- **Referência:** Processo SEI 00060-00227811/2026-80
- **Observações:** Análise vertical das modificações entre versões do PDTIC.
