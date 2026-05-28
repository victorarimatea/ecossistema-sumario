# protocolo-atualizacoes.md — Ecossistema DTD/SETIS

**Versão:** v1.0 — 2026-05-28
**Repositório:** ecossistema-sumario (M01)
**Mantenedor:** victorarimatea
**Status:** Documento de referência — candidato a skill autônoma

> Este documento define o protocolo obrigatório de encerramento para qualquer
> operação realizada no ecossistema DTD/SETIS. Toda skill que escreve em
> repositórios GitHub deve consultar este arquivo ao final da execução e
> verificar sistematicamente o que precisa ser atualizado.
>
> **Regra geral:** nenhuma operação está concluída enquanto todos os arquivos
> afetados não estiverem atualizados e registrados.

---

## Como usar este protocolo

1. Identifique o tipo de operação realizada na seção 1
2. Siga a checklist correspondente na seção 2
3. Registre o encerramento conforme a seção 3
4. Só informe "concluído" ao mantenedor após percorrer todos os itens

---

## Seção 1 — Tipos de operação

| Código | Tipo | Descrição |
|---|---|---|
| OP-A | Criação de repositório | Novo repositório de qualquer tipo (M, S, D) |
| OP-B | Atualização de skill | Alteração no SKILL.md ou arquivos de referência de skill existente |
| OP-C | Atualização de matriz | Alteração em arquivo de uma matriz (M01, M02 etc.) |
| OP-D | Geração de documento | Produção de IAC, PoC ou outro instrumento institucional |
| OP-E | Correção pontual | Correção de erro, typo ou inconsistência sem alteração de conteúdo |
| OP-F | Atualização de planejamento | Alteração em ROADMAP, CONTEXTO.md ou documentação de visão |

Uma operação pode combinar mais de um tipo. Nesse caso, execute as checklists
de todos os tipos aplicáveis, eliminando duplicatas.

---

## Seção 2 — Checklists por tipo de operação

---

### OP-A — Criação de repositório

**Repositório criado:** qualquer tipo (M, S ou D)

#### No repositório criado
- [ ] `README.md` criado com estrutura padronizada (tipo, versão, mantenedor, status)
- [ ] `backlog-versoes.md` criado com entrada v1.0 — inclui exposição de motivos
- [ ] `SKILL.md` criado (apenas tipo S) — com cabeçalho de versão, seção IDENTIDADE
      DO ECOSSISTEMA, Etapa 0 de leitura do âncora e REGRA DE ACENTUAÇÃO (se gera DOCX/PDF)
- [ ] Arquivos de referência criados em `references/` (se aplicável)

#### No ecossistema-sumario (M01)
- [ ] `sumario.md` — nova entrada na seção correta (M, S ou D) com ID, nome, versão e descrição
- [ ] `CONTEXTO.md` — tabela "Repositórios ativos" atualizada com o novo repositório
- [ ] `backlog-versoes.md` — nova entrada registrando a criação (tipo: Adição)

#### No dtd-setis (portfólio público)
- [ ] `README.md` — novo repositório adicionado na tabela e no diagrama ASCII
- [ ] `CHANGELOG.md` — nova entrada na versão atual registrando a criação
- [ ] `ROADMAP.md` — item correspondente marcado como ✅ (se estava planejado)
      ou novo item adicionado como ✅ na fase correta (se não estava no roadmap)

#### No repositório da skill que executou a criação (se aplicável)
- [ ] `backlog-versoes.md` — sem necessidade de registro (a operação já está no M01)

---

### OP-B — Atualização de skill existente

**Skill atualizada:** qualquer repositório tipo S

#### No repositório da skill
- [ ] `SKILL.md` — versão incrementada no cabeçalho (MINOR para melhorias, MAJOR para
      mudanças incompatíveis com versão anterior)
- [ ] `backlog-versoes.md` — nova entrada com tipo, motivo e alterações realizadas;
      incluir campo `**Impacto**` (breaking / non-breaking) e `**Skills afetadas**`

#### No ecossistema-sumario (M01)
- [ ] `sumario.md` — versão da skill atualizada na tabela
- [ ] `CONTEXTO.md` — tabela "Skills incorporadas" atualizada com novo evento e data
- [ ] `backlog-versoes.md` — nova entrada registrando a atualização (tipo: Atualização)

#### No dtd-setis (portfólio público)
- [ ] `CHANGELOG.md` — nova entrada registrando a atualização

> **Atenção:** se a atualização da skill introduz um padrão que deve ser propagado
> a outras skills (ex: REGRA DE ACENTUAÇÃO), verificar cada skill afetada e abrir
> item no backlog do M01 como lembrete de propagação pendente.

---

### OP-C — Atualização de matriz

**Matriz atualizada:** qualquer repositório tipo M (M01, M02 etc.)

#### No repositório da matriz
- [ ] Arquivo alterado com versão incrementada no cabeçalho
- [ ] `backlog-versoes.md` — nova entrada com tipo, motivo e alterações;
      para matrizes de conhecimento: incluir campos `**Tópico afetado**`,
      `**Fonte**` e `**Proposto por**`

#### No ecossistema-sumario (M01) — se a matriz atualizada NÃO for o próprio M01
- [ ] `sumario.md` — versão da matriz atualizada na tabela
- [ ] `backlog-versoes.md` — nova entrada registrando a atualização

#### No dtd-setis (portfólio público)
- [ ] `CHANGELOG.md` — nova entrada se a mudança for relevante para o portfólio

> **Nota:** atualizações no próprio M01 (ecossistema-sumario) já são registradas
> diretamente no seu backlog — não há repositório externo que precise ser notificado.

---

### OP-D — Geração de documento institucional (IAC, PoC, outros)

**Documento gerado:** IAC-V, IAC-H, PoC ou outro instrumento

#### No CONTEXTO.md do M01
- [ ] Tabela "Documentos IAC gerados" atualizada (para IACs) ou seção equivalente
      atualizada (para outros tipos de documento)
- [ ] Status do documento registrado: Produzido / Distribuído / Aguarda distribuição

#### No ecossistema-sumario (M01)
- [ ] `backlog-versoes.md` — nova entrada registrando a geração (tipo: Adição)

#### No dtd-setis (portfólio público)
- [ ] `CHANGELOG.md` — nova entrada se o documento for uma entrega relevante
      (ex: primeiro documento de um tipo, documento distribuído formalmente)

> **Nota:** documentos gerados não criam repositório próprio até que exista o
> repositório `pdtic-historico` ou equivalente. Até lá, o registro vive no CONTEXTO.md.

---

### OP-E — Correção pontual

**Correção realizada:** typo, inconsistência, erro sem alteração de conteúdo

#### No arquivo corrigido
- [ ] Correção aplicada
- [ ] Versão incrementada apenas se o erro comprometia a integridade do documento
      (ex: SHA errado, ID duplicado); caso contrário, sem incremento de versão

#### No repositório onde a correção ocorreu
- [ ] `backlog-versoes.md` — entrada apenas se a versão foi incrementada
      (tipo: Correção); correções sem incremento de versão não precisam de registro

> **Critério:** se alguém que lesse a versão anterior tomaria uma decisão errada
> por causa do erro, registre. Se é apenas estética, não registre.

---

### OP-F — Atualização de planejamento ou visão

**Arquivos afetados:** ROADMAP.md, CONTEXTO.md, MANIFESTO.md, DECISOES.md

#### No arquivo atualizado
- [ ] Conteúdo atualizado
- [ ] Data de atualização ajustada no cabeçalho ou rodapé do arquivo

#### No ecossistema-sumario (M01) — se o arquivo for CONTEXTO.md
- [ ] `backlog-versoes.md` — nova entrada (tipo: Atualização)
- [ ] Versão do CONTEXTO.md incrementada no cabeçalho

#### No dtd-setis (portfólio público) — se o arquivo for ROADMAP, MANIFESTO ou DECISOES
- [ ] `CHANGELOG.md` — nova entrada se a mudança for substantiva
      (nova fase concluída, nova decisão arquitetural, mudança de visão)

---

## Seção 3 — Registro de encerramento

Ao final de qualquer operação, antes de informar "concluído" ao mantenedor,
o Claude deve apresentar o seguinte resumo:

```
ENCERRAMENTO DA OPERAÇÃO
Tipo(s): [OP-X, OP-Y]
Repositório principal: [nome]
Arquivos atualizados: [lista]
Itens pendentes (se houver): [lista ou "nenhum"]
Próxima ação sugerida: [o que o mantenedor deve fazer agora, se algo]
```

Se houver itens pendentes — por falta de informação, token expirado, ou decisão
que depende do mantenedor — listá-los explicitamente com o motivo.

---

## Seção 4 — Quando este documento deve ser consultado

Este protocolo é consultado obrigatoriamente por:

- `skill-criador-de-skills` (S01) — na Etapa 7 (relatório final)
- `skill-iac-pdtic` (S02) — após geração e entrega de qualquer documento
- `skill-poc-saude-digital` (S03) — após geração e entrega de qualquer PoC
- Qualquer skill futura que realize escrita em repositórios do ecossistema
- O Claude em sessões avulsas (sem skill carregada) ao realizar operações no ecossistema

---

## Seção 5 — Evolução para skill autônoma

Este documento será promovido a skill autônoma (`skill-protocolo-encerramento`)
quando as seguintes condições forem atendidas:

- [ ] O protocolo tiver sido aplicado em pelo menos 3 operações completas
      e sua cobertura tiver sido validada na prática
- [ ] Houver necessidade de lógica condicional mais complexa do que uma checklist
      (ex: verificação automática de SHA, validação de consistência entre arquivos)
- [ ] O ecossistema tiver pelo menos 2 membros ativos — tornando a autonomia
      de execução mais valiosa do que a supervisão manual

Até lá, este documento de referência é suficiente e mais fácil de manter.
