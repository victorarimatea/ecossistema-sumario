## v0.34 — 2026-06-13

**Tipo:** Atualização (OP-F + propagação de OP-B)
**Arquivos alterados:** CONTEXTO.md (v3.8 → v3.9), sumario.md (v3.5 → v3.6)
**Operação S04:** registro da doutrina de dois tokens no CONTEXTO; propagação
ao sumario (hub-entrada v2.0 → v2.1 pelo novo PROTOCOLO-SESSAO.md; S04 v2.7 →
v2.8; versão do M01 reconciliada v0.31 → v0.34)
**Sessão:** Operação — criação do PROTOCOLO-SESSAO.md canônico (2026-06-13)

**O que mudou:**
- `CONTEXTO.md`: seção "Como iniciar uma nova sessão de trabalho" reescrita
  para o modelo de dois tokens (leitura ampla na abertura; edição na conversão
  para escrita); raw aposentado como canal de sessão. Cabeçalho v3.8 → v3.9
- `sumario.md`: hub-entrada v2.0 → v2.1 (novo artefato PROTOCOLO-SESSAO.md);
  S04 v2.7 → v2.8 (ETAPA 0 dois tokens); linha do M01 reconciliada de v0.31
  para v0.34 (propagação atrasada desde v0.32 — fechada agora usando este
  backlog como fonte primária). Cabeçalho v3.5 → v3.6

**Por que foi feito:**
A sessão criou o PROTOCOLO-SESSAO.md como lar canônico dos ritos de sessão e,
com ele, adotou a doutrina de dois tokens, alinhando o S04 (ETAPA 0) e o
CONTEXTO. A reconciliação da versão do M01 no sumario (v0.31 → v0.34) corrige
uma defasagem de propagação herdada, usando este backlog como fonte primária.

---

## v0.33 — 2026-06-12

**Tipo:** Atualização (OP-F / propagação de OP-W)
**Arquivos alterados:** sumario.md (v3.4 → v3.5), CONTEXTO.md (v3.7 → v3.8)
**Operação S04:** propagação de duas atualizações de workflow (OP-W) para os
arquivos de referência central do M01
**Sessão:** W06 — Formalização do ciclo de sessão (metas 1, 2 e 3 do ROADMAP)

**O que mudou:**
- `sumario.md`: versão do W03 atualizada v1.2 → v1.3 e do W06 v1.1 → v1.2,
  com descrições revisadas; cabeçalho do sumario v3.4 → v3.5
- `CONTEXTO.md`: tabela de workflows — mesmas versões propagadas;
  cabeçalho v3.7 → v3.8

**Por que foi feito:**
Sessão de formalização do ciclo de sessão executou as três metas fechadas na
sessão de design de 2026-06-11:
- **Meta 1+3 (W03 v1.3):** estrutura do relatório reorganizada em três blocos
  (narrativa, ciclo de qualidade, handoff) e frontmatter expandido com os
  campos `convergencia` e `residuo_tolerado`
- **Meta 2 (W06 v1.2):** handoff passa a ser lido automaticamente pelo agente
  a partir do último relatório de sessão no hub-memoria, eliminando a cola
  manual; adicionada regra de fallback (falha na extração → auditoria W05 nova
  do zero, nunca reverter ao processo manual)

As versões no sumario.md e no CONTEXTO.md são mantidas sincronizadas — o
sumario.md é a fonte de verdade e o CONTEXTO.md deriva dele.

---

## v0.32 — 2026-06-10

**Tipo:** Correção (OP-E)
**Arquivos alterados:** README.md, CONTEXTO.md
**Operação S04:** OP-E (correção pontual)
**Sessão:** W06 — correção de divergências SEV2

**O que mudou:**
- `README.md`: versão atualizada de v0.30 para v0.31 (SEV2-01) e instrução
  de sessão substituída — raw.githubusercontent.com → GitHub Contents API
- `CONTEXTO.md`: seção "Como iniciar uma nova sessão de trabalho" corrigida
  — URLs raw.githubusercontent.com substituídas por instruções via
  GitHub Contents API (SEV2-03)

**Por que foi feito:**
Divergências SEV2 identificadas pelo W05 em auditoria de 2026-06-09.
README.md declarava v0.30 enquanto sumario.md e backlog já registravam v0.31.
CONTEXTO.md e README.md instruíam leitura via raw.githubusercontent.com,
contradizendo o protocolo API-only estabelecido em 2026-06-06 (alerta de
cache CDN). Correção aplicada na abertura da sessão de 2026-06-10.

---

## v0.31 — 2026-06-08

**Tipo:** Atualização
**Arquivo alterado:** GLOSSARIO.md (v2.1 → v2.2)
**Operação S04:** OP-C (atualização de matriz)
**Sessão:** W04 — primeira sessão de roadmapping

**O que mudou:**
- 5 novos termos adicionados à Categoria 17 (Conceitos Proprietários do Ecossistema):
  `versionamento independente`, `conhecimento consolidado`, `Padrão CONFIRMAR`,
  `context mining / mineração de contexto`, `perguntas orientadoras`
- Índice alfabético unificado atualizado com os 5 novos termos

**Por que foi feito:**
Termos candidatos acumulados em múltiplas sessões (SEV4 no W05). Aprovados
em curadoria na primeira sessão W04 de 2026-06-08. O termo "Padrão CONFIRMAR"
recebeu tratamento especial: o qualificador "Padrão" foi adicionado para
distingui-lo de instrução genérica e sinalizar que carrega protocolo específico.

---

# Backlog de Versões — hub-fonte (M01)

**Repositório:** https://github.com/victorarimatea/hub-fonte
**Mantenedor:** victorarimatea

> Este documento registra o histórico de versões do repositório hub-fonte
> como unidade. Cada entrada inclui versão, data, tipo de alteração,
> exposição de motivos e alterações realizadas.

---

## ⚠️ Nota de Reconciliação — 2026-06-06

Este backlog acumulou, ao longo de sua história, inconsistências estruturais
que são aqui **documentadas** (não corrigidas) em respeito ao princípio de
imutabilidade histórica do ecossistema. Uma reorganização completa e cuidadosa
do arquivo está registrada como missão futura na staging area.

**Inconsistências conhecidas neste arquivo:**

1. **Duplicação de numeração v0.25–v0.30:** existem dois blocos de entradas
   com os mesmos números de versão — um datado 2026-06-06 (inserido na sessão
   de correções de auditoria W05) e outro datado 2026-06-05. **O bloco 2026-06-06
   é o canônico** para as versões v0.25–v0.30. O bloco 2026-06-05 representa
   entradas anteriores cuja numeração colidiu por erro de propagação.

2. **Séries de versão entrelaçadas:** o arquivo contém entradas de séries de
   versão de documentos internos (ex.: v2.5, v2.4, v1.6, datadas 06-04/06-05)
   misturadas com a série do repositório como unidade (v0.X). Essas entradas
   referem-se a versionamentos de documentos específicos (sumario.md, GLOSSARIO.md)
   registrados historicamente neste backlog antes da separação clara de
   versionamento por documento.

3. **Título legado embutido:** há um segundo título H1 com o nome legado
   `ecossistema-sumario` em ponto intermediário do arquivo (resquício de
   concatenação de dois backlogs durante a renomeação do repositório).
   Preservado por imutabilidade histórica.

**Versão canônica atual do repositório hub-fonte (M01):** v0.30 (2026-06-06),
conforme registrado no sumario.md.

---

## v0.34 — 2026-06-06

**Tipo de alteração:** Correção
**Autorizado por:** victorarimatea
**Exposição de motivos:** Oitava rodada de correções da sessão 2026-06-06,
identificadas pela sexta rodada de auditoria W05 (Opus 4.8). Divergências
remanescentes de representação visual e formatação.

**Causa raiz:** Erro #009 — drift entre representações paralelas do mesmo dado
(diagrama ASCII vs tabela autoritativa no README do hub-entrada). W06 e D03
foram adicionados às tabelas em operações anteriores mas não ao diagrama.
Cabeçalho do ROADMAP defasado por valores escritos antes das operações seguintes.
Glitch de formatação Markdown no CONTEXTO (linhas W05/W06 sem | de fechamento).

### Alterações realizadas
- `README.md` hub-entrada: diagrama ASCII com W06 e D03 (SEV2 + SEV4)
- `ROADMAP.md` hub-entrada: cabeçalho atualizado — sumario v3.1, W06 v1.1 (SEV3)
- `CONTEXTO.md` v3.5 → v3.6: | de fechamento nas linhas W05/W06 (SEV4)

### Diferido para Handoff (SEV4 não-bloqueantes)
- ID W04 reutilizado em item prospectivo do ROADMAP (wkf-iac-conformidade)
- Inconsistência terminológica: "perguntas orientadoras" (S04) vs "ordenadoras" (ROADMAP)
- Candidatos ao glossário: versionamento independente, conhecimento consolidado

---

## v0.33 — 2026-06-06

**Tipo de alteração:** Correção + Adição
**Autorizado por:** victorarimatea
**Exposição de motivos:** Sétima rodada de correções da sessão 2026-06-06,
identificadas pela quinta rodada de auditoria W05 (Opus 4.8). Validação final
contra o novo critério de convergência do W06 v1.1 (zero SEV1/SEV2).

**Causa raiz dos SEV2:** Erro #013 recorrente — os incrementos de M01 (v0.30)
e W06 (v1.1) foram registrados no sumario.md e WORKFLOW.md na operação anterior
sem propagação para os respectivos READMEs. A reincidência do mesmo erro durante
sua própria correção reforça empiricamente a necessidade estrutural da separação
executor/auditor e do protocolo de Handoff.

### Alterações realizadas
- `README.md` hub-fonte: v0.25 → v0.30 (SEV2)
- `README.md` wkf-sessao-agente: v1.0 → v1.1 (SEV2)
- `sumario.md` v3.0 → v3.1: Links rápidos completados com D03, W04, W05, W06 (SEV3)
- `GLOSSARIO.md` v2.0 → v2.1: backlog-acoes-dtd, protocolo-atualizacoes, ONBOARDING (SEV4)

### Divergências SEV4 descartadas (não proprietárias)
- SHA e base64: termos técnicos genéricos, não específicos do ecossistema

---

## v0.32 — 2026-06-06

**Tipo de alteração:** Adição
**Autorizado por:** victorarimatea
**Exposição de motivos:** Propagação da atualização do W06 para v1.1 (novo
critério de convergência de auditoria por integridade operacional).

### Alterações realizadas
- `sumario.md` v2.9 → v3.0: W06 v1.0 → v1.1
- `CONTEXTO.md` v3.4 → v3.5: W06 v1.0 → v1.1

---

## v0.31 — 2026-06-06

**Tipo de alteração:** Correção + Melhoria
**Autorizado por:** victorarimatea
**Exposição de motivos:** Sexta rodada de correções da sessão 2026-06-06,
identificadas pela quarta rodada de auditoria W05 independente (executada com
modelo Opus 4.8, que produziu auditoria mais detalhada — 13 divergências).

**Causa raiz central:** padrão recorrente de incrementos registrados em backlogs
sem propagação para README/SKILL/sumario (Erro #013). Duplicação no próprio
backlog do M01 causada por inserções sem verificação de entradas pré-existentes.

### Alterações realizadas
- `README.md` skl-github-orquestracao: v1.0 → v2.7
- `README.md` wkf-registro-sessao: v1.0 → v1.2
- `README.md` wkf-auditoria-consistencia: v1.0 → v1.2
- `README.md` + `SKILL.md` skl-criador-de-skills: v1.0 → v1.1
- `README.md` hub-memoria: v0.2 → v0.3
- `taxonomia.md` M02: nome legado corrigido
- `backlog-versoes.md` M02: entrada v1.1 reposicionada; URL legada corrigida
- `README.md` S01/S02/S03: rótulo "Versão atual:" → "Versão:"
- `backlog-versoes.md` M01: título H1 + nota de reconciliação (inconsistências
  históricas documentadas, não corrigidas — reorganização completa adiada para
  missão futura)
- `nomenclatura.md`: exceção pasta sessoes/ do P02 formalizada
- `sumario.md` v2.8 → v2.9: M01 v0.30, S01 v1.1, P02 v0.3

### Itens registrados para missão futura (staging)
- Reorganização completa do backlog do M01 (séries de versão entrelaçadas)

---

## v0.30 — 2026-06-06

**Tipo de alteração:** Correção + Melhoria
**Autorizado por:** victorarimatea
**Exposição de motivos:** Quinta e última rodada de correções da sessão
2026-06-06, identificadas pela terceira rodada de auditoria W05 independente.

**Causas raiz:**
- Campo Versão do hub-entrada inserido na linha 148 em vez das primeiras linhas
  (erro de posicionamento na operação anterior)
- Skills com Front Matter YAML sem declaração de versão legível por varredura
  automatizada — convenção não existia; criada agora
- Índice Alfabético do GLOSSARIO.md não atualizado desde v1.6 (11 termos ausentes)
- Tipo W ausente da Categoria 1 do GLOSSARIO.md desde a formalização do tipo W

### Alterações realizadas
- `README.md` hub-entrada: campo Versão movido para linha 2 (após título)
- `SKILL.md` skl-poc-saude-digital: `version: "v1.0"` adicionado ao Front Matter
- `SKILL.md` skl-briefing-saude-digital: `version: "v1.0"` adicionado ao Front Matter
- `GLOSSARIO.md` v1.9 → v2.0: Tipo W na Cat.1; 11 termos no Índice Alfabético
- `nomenclatura.md`: convenção de versão em Skills com Front Matter YAML registrada
- `sumario.md` v2.7 → v2.8

---

## v0.29 — 2026-06-06

**Tipo de alteração:** Correção
**Autorizado por:** victorarimatea
**Exposição de motivos:** Quarta rodada de correções da sessão 2026-06-06,
identificadas pela segunda rodada de auditoria W05 independente de fechamento.

**Causas raiz:**
- W05 atualizado para v1.2 nesta sessão sem propagação imediata para sumario.md
  e CONTEXTO.md
- hub-entrada com versão ambígua (v0.9 retroalimentada vs v2.0 operacional) —
  decisão do mantenedor: v2.0 é a versão canônica desde a refatoração de 2026-06-02
- P01 README sem campo Versão desde a criação
- OP-W e OP-AG e W05 ausentes do GLOSSARIO.md

### Alterações realizadas
- `sumario.md` v2.6 → v2.7: W05 v1.2; hub-entrada v2.0
- `CONTEXTO.md` v3.3 → v3.4: W05 v1.2
- `README.md` hub-entrada: v0.9 → v2.0
- `README.md` P01: campo Versão v0.1 adicionado
- `GLOSSARIO.md` v1.8 → v1.9: W05 entrada dedicada; OP-W e OP-AG adicionados

---

## v0.28 — 2026-06-06

**Tipo de alteração:** Correção + Adição
**Autorizado por:** victorarimatea
**Exposição de motivos:** Terceira rodada de correções da sessão 2026-06-06,
identificadas por auditoria W05 de fechamento executada em chat separado.

**Causa raiz:** README.md do hub-fonte nunca foi sincronizado com a versão
do repositório como unidade (ficou em v0.11 desde criação). GLOSSARIO.md
não tinha entradas para 8 termos em uso ativo nos documentos operacionais.

### Alterações realizadas
- `README.md` hub-fonte: v0.11 → v0.25 (alinhado ao sumario.md)
- `README.md` hub-entrada: campo Versão v0.9 adicionado
- `GLOSSARIO.md` v1.7 → v1.8: 8 novos termos adicionados — Commander's Intent,
  staging area, W06/wkf-sessao-agente, hub-aprendizagem (D03),
  mat-cadastro-ses-setis-dtd (D02), engenharia reversa,
  separação executor/auditor, Handoff

---

## v0.27 — 2026-06-06

**Tipo de alteração:** Adição
**Autorizado por:** victorarimatea
**Exposição de motivos:** Registro do W06 (wkf-sessao-agente) no ecossistema
após criação do repositório e aprovação do WORKFLOW.md v1.0.

### Alterações realizadas
- `sumario.md` v2.4 → v2.5: W06 adicionado à tabela de Workflows
- `CONTEXTO.md` v3.2 → v3.3: W06 adicionado à tabela de Workflows
- `README.md` hub-entrada: W06 adicionado à tabela de Workflows

---

## v0.26 — 2026-06-06

**Tipo de alteração:** Correção
**Autorizado por:** victorarimatea
**Exposição de motivos:** Segunda rodada de correções identificadas pela auditoria
W05 independente executada em sessão separada em 2026-06-06. A auditoria independente
encontrou 11 divergências, incluindo 3 introduzidas pela própria operação anterior
desta sessão — confirmando o princípio de separação executor/auditor.

**Causa raiz geral:** propagação incompleta na operação anterior (hub-entrada README
não verificado contra sumario.md); erro de substituição que copiou descrição do W03
para W04; linha W04 duplicada no CONTEXTO.md por replace parcial; nomes legados
no GLOSSARIO.md não corrigidos desde renomeação do repositório âncora.

### Alterações realizadas
- `sumario.md` v2.3 → v2.4: W04 com descrição correta; W05 v1.0 → v1.1
- `CONTEXTO.md` v3.1 → v3.2: linha W04 duplicada removida; W05 v1.1;
  hub-aprendizagem movido para seção Documentos com ID D03
- `GLOSSARIO.md` v1.6 → v1.7: cabeçalho e corpo com nomenclatura atual
  (hub-fonte, mat-saude-digital-taxonomia, hub-entrada)
- `README.md` hub-entrada: W04, W05 e D03 adicionados às tabelas
- `INDICE.md` prj-telessaude-poc-prisional: criado (arquivo obrigatório ausente)
- `execucoes/.gitkeep` wkf-roadmap-geral: pasta obrigatória criada

---

## v0.25 — 2026-06-06

**Tipo de alteração:** Correção
**Autorizado por:** victorarimatea
**Exposição de motivos:** Correção de divergências identificadas pela auditoria W05
na sessão de abertura de 2026-06-06. Três problemas corrigidos:
(1) linha W03 no sumario.md estava truncada — faltavam campos `status` e `descrição`;
(2) versão do M01 no sumario.md estava em v0.24 sem ter sido incrementada após
as sessões de 2026-06-05 que alteraram múltiplos arquivos do repositório;
(3) hub-aprendizagem não tinha ID formal — classificado como D03 após decisão
do mantenedor (repositório documental reflexivo; não cria nova categoria de tipo).

**Causa raiz:** falha de sequência lógica na execução — mapa de dependências
percorrido antes de atualizar o documento-núcleo; e ausência de decisão explícita
documentada sobre a taxonomia do hub-aprendizagem no momento de sua criação.

### Alterações realizadas
- `sumario.md` v2.2 → v2.3: linha W03 completada; M01 v0.24 → v0.25;
  hub-aprendizagem movido de "Infraestrutura de conhecimento" para Documentos (D)
  com ID D03
- `CONTEXTO.md` v3.0 → v3.1: hub-aprendizagem atualizado para D03

---

## v0.30 — 2026-06-05

**Tipo de alteração:** Adição
**Proposto por:** Victor Leonardo Arimatea Queiroz
**Tópico afetado:** Novo workflow W05
**Exposição de motivos:** Criação do W05 wkf-auditoria-consistencia —
resposta estrutural ao GAP 1 identificado no exercício de engenharia reversa
de 2026-06-05. Primeiro processo genuinamente independente da S04: audita
o estado real do ecossistema em 5 camadas sem executar operações.

### Alterações realizadas
- `sumario.md`: W05 adicionado na tabela de Workflows e na tabela de links
- `CONTEXTO.md` v2.9 → v3.0: W05 adicionado na tabela de Workflows

---

## v0.29 — 2026-06-05

**Tipo de alteração:** Atualização
**Proposto por:** Victor Leonardo Arimatea Queiroz
**Tópico afetado:** Versões da S04 e W03
**Exposição de motivos:** Sincronização após Ajustes 1, 2 e 3 da sessão de
2026-06-05. S04 v2.7 (Etapa 6-A expandida). W03 v1.2 (Etapa 2-B adicionada).
staging.md reformulada com painel dinâmico, alertas e Seção E.

### Alterações realizadas
- `sumario.md`: S04 v2.6→v2.7; W03 v1.1→v1.2
- `CONTEXTO.md` v2.8→v2.9: S04 v2.6→v2.7; W03 v1.1→v1.2

---

## v0.28 — 2026-06-05

**Tipo de alteração:** Adição
**Proposto por:** Victor Leonardo Arimatea Queiroz
**Tópico afetado:** Novo repositório de infraestrutura de conhecimento
**Exposição de motivos:** Criação do hub-aprendizagem na sessão de 2026-06-05.
Repositório de memória intelectual identificado como lacuna estrutural do
ecossistema: backlogs e changelogs registram o quê e o quando, mas não o
raciocínio por trás das escolhas nem o diálogo com benchmarks de mercado.

### Alterações realizadas
- `sumario.md`: nova seção "Infraestrutura de conhecimento" + hub-aprendizagem v1.0
- `CONTEXTO.md` v2.7 → v2.8: hub-aprendizagem adicionado na tabela de estrutura

---

## v0.27 — 2026-06-05

**Tipo de alteração:** Atualização
**Proposto por:** Victor Leonardo Arimatea Queiroz
**Tópico afetado:** Referências à versão da S04 (skl-github-orquestracao)
**Exposição de motivos:** Sincronização após Execução 2 da sessão de 2026-06-05.
S04 atualizada para v2.6 com verificações embutidas obrigatórias (Nível B Estrutural).

### Alterações realizadas
- `sumario.md`: S04 v2.5 → v2.6
- `CONTEXTO.md` v2.6 → v2.7: S04 v2.5 → v2.6, descrição atualizada

---

## v0.26 — 2026-06-05

**Tipo de alteração:** Atualização
**Proposto por:** Victor Leonardo Arimatea Queiroz
**Tópico afetado:** Referências à versão da S04 (skl-github-orquestracao)
**Exposição de motivos:** Sincronização após Execução 1 da sessão de 2026-06-05.
S04 atualizada para v2.5 com escala de severidade SEV1–SEV4 e classificação
retroativa dos Erros #001–#013. sumario.md e CONTEXTO.md atualizados
para refletir v2.5.

### Alterações realizadas
- `sumario.md`: S04 v2.4 → v2.5
- `CONTEXTO.md` v2.5 → v2.6: S04 v2.4 → v2.5, descrição atualizada

---

## v0.25 — 2026-06-05

**Tipo de alteração:** Atualização
**Proposto por:** Victor Leonardo Arimatea Queiroz
**Tópico afetado:** Referências à versão da S04 (skl-github-orquestracao)
**Exposição de motivos:** Sincronização de referências após diagnóstico de drift
identificado na abertura de sessão de 2026-06-05. sumario.md registrava S04 em v2.1
e CONTEXTO.md em v2.3; versão real do SKILL.md era v2.4. Ambos atualizados para v2.4.
Operação classificada como OP-E/OP-C com registro de Erro #013 na S04.

### Alterações realizadas
- `sumario.md` v2.0 → v2.1: S04 v2.3 → v2.4
- `CONTEXTO.md` v2.4 → v2.5: S04 v2.3 → v2.4

---

## v2.5 — 2026-06-05

**Tipo de alteração:** Correção
**Autorizado por:** Victor Leonardo Arimatea Queiroz — Diretor de Transformação Digital
**Exposição de motivos:** Correção de drifts de nomenclatura legada em três arquivos
operacionais do M01. Os arquivos ONBOARDING.md, INDICE.md e README.md ainda
referenciavam o nome `ecossistema-sumario` (nome anterior do repositório, renomeado
para `hub-fonte`) em campos de metadados e URLs. O conteúdo funcional dos três
arquivos estava correto. Causa raiz: o ONBOARDING.md foi criado durante ou
imediatamente após a refatoração de nomenclatura, e o README.md/INDICE.md nunca
receberam atualização de título após o renomeio. A S04 não cobria o ONBOARDING.md
em suas verificações — gap corrigido simultaneamente na v2.4 da S04.
Nota de princípio: registros históricos em backlog-versoes.md e CHANGELOG.md que
referenciam `ecossistema-sumario` ou `dtd-setis` pela nomenclatura da época são
preservados integralmente — representam o estado real do sistema no momento em que
foram escritos e não devem ser alterados.

### Alterações realizadas
- `ONBOARDING.md` v1.0 → v1.1: campo `**Repositório:**` corrigido de `ecossistema-sumario` para `hub-fonte`
- `INDICE.md`: título corrigido de `Índice — ecossistema-sumario` para `Índice — hub-fonte`; data atualizada para 2026-06-05; contagem corrigida de 8 para 10 arquivos
- `README.md` v0.10 → v0.11: título, versão, tabela de arquivos (ONBOARDING.md e GLOSSARIO.md adicionados) e URL de sessão corrigidos

---

## v2.4 — 2026-06-04

**Tipo de alteração:** Atualização
**Autorizado por:** victorarimatea
**Exposição de motivos:** W04 criado e S04 atualizada para v2.3 com Etapa 6-A.
Sumario e CONTEXTO sincronizados.

### Alterações realizadas
- `sumario.md` v2.1 → v2.2: W04 adicionado; S04 → v2.3
- `CONTEXTO.md` v2.3 → v2.4: W04 adicionado; S04 v2.3 atualizado com Etapa 6-A

---

## v2.3 — 2026-06-04

**Tipo de alteração:** Atualização
**Autorizado por:** victorarimatea
**Exposição de motivos:** S04 e W03 atualizados para corrigir drift estrutural
do ROADMAP — entregáveis não previstos eram implementados mas nunca registrados
no ROADMAP. Verificação 5-A adicionada à S04 e Etapa 2-A adicionada ao W03.
Erro #010 documentado. CONTEXTO.md atualizado com versões corretas.

### Alterações realizadas
- `sumario.md` v2.0 → v2.1: S04 atualizado para v2.2; W03 atualizado para v1.1
- `CONTEXTO.md` v2.2 → v2.3: notas de versão adicionadas nas tabelas S04 e W03

---

## v2.2 — 2026-06-04 (CONTEXTO.md)

**Tipo de alteração:** Adição
**Autorizado por:** Victor Leonardo Arimatea Queiroz — Diretor de Transformação Digital
**Exposição de motivos:** Adição da seção "Taxonomia e Glossário — distinção essencial"
ao CONTEXTO.md. A seção explica com exemplos concretos a diferença de propósito entre
M02 (taxonomia — mapa de navegação temática) e M01/GLOSSARIO.md (dicionário de
definições), inclui tabela de coexistência com 4 termos exemplo e regra explícita de
uso para agentes de IA. Motivação: risco identificado de confusão entre os dois
instrumentos por novos colaboradores e agentes, dado que nenhum documento do
ecossistema explicava a distinção. Operação conduzida via S04 (OP-C), sessão
de 2026-06-04.

---

## v1.6 — 2026-06-04 (GLOSSARIO.md)

**Tipo de alteração:** Adição
**Autorizado por:** Victor Leonardo Arimatea Queiroz — Diretor de Transformação Digital
**Exposição de motivos:** Adição de 32 termos distribuídos em 5 novas categorias:
Cat. 13 (Monitoramento e Inteligência Organizacional — 8 termos, incluindo os
definidos pelo mantenedor em sessão de 2026-06-04 com pergunta orientadora);
Cat. 14 (Análise de Dados e BI — 6 termos);
Cat. 15 (Gestão Orientada a Dados — 5 termos);
Cat. 16 (Arquitetura de Dados — 5 termos, com cross-reference de Integração → Cat. 11);
Cat. 17 (Conceitos Proprietários do Ecossistema — 8 termos de autoria DTD/SETIS).
Índice Alfabético Unificado atualizado de 62 para 91 entradas.
Análise de conflitos realizada: único ponto identificado foi Interoperabilidade —
resolvido mantendo definição normativa na Cat. 11 e adicionando cross-reference
na Cat. 16. Operação conduzida via S04 (OP-C), sessão de 2026-06-04.

---

## v1.5 — 2026-06-04 (GLOSSARIO.md)

**Tipo de alteração:** Adição + Reestruturação
**Autorizado por:** Victor Leonardo Arimatea Queiroz — Diretor de Transformação Digital
**Exposição de motivos:** Incorporação de 26 termos normativos produzidos em análise
prévia no NotebookLM sobre o corpus documental do D01. O glossário foi reestruturado
em Parte I (infraestrutura do ecossistema — 8 categorias preexistentes) e Parte II
(domínio da saúde digital — Cat. 9 a 12). Criada Cat. 13 (Monitoramento e Inteligência
Organizacional) como placeholder para termos identificados em sessão de 2026-06-04.
Adicionado Índice Alfabético Unificado com 62 entradas. Adaptação do termo
"Auditabilidade" para "Auditabilidade de IA" (Cat. 11) para evitar ambiguidade com
"Auditoria de glossário" (Cat. 5) — aprovada pelo mantenedor em sessão de 2026-06-04.
Cross-references cruzados entre as duas entradas. Análise de conflitos realizada
previamente: nenhum conflito de definição identificado entre os 26 termos novos e
os termos existentes. Operação conduzida via S04 (OP-C), sessão de 2026-06-04.

---

## v2.0 — 2026-06-04

**Tipo de alteração:** Adição + Correção
**Autorizado por:** Victor Leonardo Arimatea Queiroz — Diretor de Transformação Digital
**Exposição de motivos:** (1) Registro de S07 `skl-briefing-saude-digital` — skill formalizada
a partir da versão consolidada no projeto Claude; (2) Correção da tabela de Links rápidos:
duplicatas removidas, todos os 18 repositórios ativos incluídos com ID, tipo e visibilidade.
Operação conduzida via S04 (OP-A + OP-C + OP-E), sessão de 2026-06-04.

---

## v0.24 — 2026-06-03

**Tipo de alteração:** Atualização (MAJOR)
**Autorizado por:** victorarimatea
**Exposição de motivos:** Reescrita completa do CONTEXTO.md (v1.8 → v2.0).
Higienização estrutural: removidos todos os elementos transitórios acumulados
desde maio/2026 (datas de reunião, processos SEI, versões específicas do PDTIC,
próximos passos, documentos IAC produzidos, tokens e arquivos carregados no Claude).
Adicionada mensagem de boas-vindas do mantenedor para colaboradores e agentes externos.
Estrutura de repositórios atualizada para refletir o ecossistema completo atual
(15 repositórios em 6 tipos: M, S, D, W, A, P). ONBOARDING.md registrado nos
arquivos obrigatórios do M01. Versão MAJOR pois o documento anterior era
incompatível com o estado real do ecossistema.

---

## v0.23 — 2026-06-03

**Tipo de alteração:** Adição
**Autorizado por:** victorarimatea
**Exposição de motivos:** Criação do ONBOARDING.md — documento de entrada para
agentes de IA e colaboradores externos. Organiza o acesso ao ecossistema por
propósito (entender / agente IA / executar tarefa / contribuir), com links
diretos para os recursos corretos em cada caso. Permite compartilhar um único
link com qualquer pessoa ou sistema e garantir navegação produtiva imediata.
INDICE.md atualizado para refletir o novo arquivo.

---

## v0.26 — 2026-06-02

**Tipo de alteração:** Adição
**Autorizado por:** victorarimatea
**Exposição de motivos:** Criação do P02 (ecossistema-dtd-setis) para preservar
a história da construção do ecossistema, e do W03 (workflow-registro-sessao)
como processo de registro de sessões de trabalho intensivo. O P02 nasce com
Resumo Executivo técnico completo e relatório narrativo da sessão fundacional
de 2026-06-02.

### Alterações realizadas
- `sumario.md` → v1.6: P02 e W03 registrados
- `CONTEXTO.md` → v1.8: P02 e W03 adicionados
- `backlog-versoes.md` → esta entrada (v0.26)

---

## v0.24 — 2026-06-03

**Tipo de alteração:** Correção + Atualização
**Autorizado por:** victorarimatea
**Exposição de motivos:** Duas correções na mesma operação: (1) drift no sumario.md — P02 ainda registrado como v0.1 quando o CONTEXTO.md já havia sido atualizado para v0.2 na sessão anterior; (2) atualização da S04 para v2.0 após incorporação da checklist OP-P especial para o P02. A sessão de 2026-06-03 também produziu o mapeamento completo dos 8 arquivos externos que referenciam o P02, formalizado como OP-P especial na S04 v2.0.
**Tópico afetado:** sumario.md — versões de P02 e S04
**Fonte:** Operação OP-P + OP-C de 2026-06-03
**Proposto por:** sistema

### Alterações realizadas
- `sumario.md` v1.9 → v2.0: P02 corrigido de v0.1 para v0.2 (drift); S04 atualizado de v1.9 para v2.0
- `CONTEXTO.md` v1.9 → v2.0: S04 atualizado de v1.9 para v2.0

---



## v0.23 — 2026-06-03

**Tipo de alteração:** Atualização
**Autorizado por:** victorarimatea
**Exposição de motivos:** Atualização do CONTEXTO.md para refletir o estado atual do ecossistema após publicação do RESUMO-EXECUTIVO-v2.0 no P02. Duas correções pontuais: (1) versão do P02 atualizada de v0.1 para v0.2 na tabela de repositórios ativos; (2) item 5 dos próximos passos planejados marcado como concluído — o projeto Ecossistema DTD/SETIS já está configurado e ativo no Claude.ai.
**Tópico afetado:** Estrutura atual do ecossistema — tabela de repositórios ativos; próximos passos planejados
**Fonte:** Operação OP-P de atualização do P02 em 2026-06-03
**Proposto por:** sistema

### Alterações realizadas
- `CONTEXTO.md` v1.8 → v1.9: versão do P02 atualizada (v0.1 → v0.2), item 5 dos próximos passos marcado como concluído

---



## v0.25 — 2026-06-02

**Tipo de alteração:** Correção + Atualização
**Autorizado por:** victorarimatea
**Exposição de motivos:** Saneamento de drifts identificados em auditoria
externa por ferramenta LLM. Causa raiz confirmada: S04 não instruía
atualização dos arquivos de referência central (CONTEXTO.md, ROADMAP.md,
arquitetura.md) nos tipos de operação OP-C, OP-W e OP-AG. Corrigido com
blindagem estrutural da S04 v1.8 (Erro #007 + Verificação 5).

### Alterações realizadas
- `CONTEXTO.md` → v1.7: versões sincronizadas com sumario.md (fonte de verdade)
- `sumario.md` → v1.4: duplicações removidas; S04 atualizado para v1.7
- `dtd-setis/docs/arquitetura.md` → v2.0: reescrita com 6 tipos, 4 camadas,
  relações entre tipos, S04, repositório âncora e porta de entrada
- `dtd-setis/ROADMAP.md`: reorganizado em concluído/em curso/próximo/médio/longo
- `dtd-setis/INDICE.md`: contagem, data e docs/arquitetura.md v2.0 atualizados
- `dtd-setis/backlog-versoes.md`: entradas retroativas v1.1–v2.0 adicionadas
- `skill-github-orquestracao/SKILL.md` → v1.8: Verificação 5 + Erro #007
- `backlog-versoes.md` → esta entrada (v0.25)
- `dtd-setis/CHANGELOG.md` → entrada [2.4]

---

## v0.24 — 2026-06-02

**Tipo de alteração:** Adição
**Autorizado por:** victorarimatea
**Exposição de motivos:** Implementação do tipo A (Agenda) e dos componentes
do workflow de registro de reunião (S06 e W02). O tipo A nasce da necessidade
de um lar para registros de reunião avulsos e introduz o primeiro tipo do
ecossistema indexado por tempo de ocorrência — não por ordem de criação.
A skill S06 formaliza o prompt institucional desenvolvido e testado pelo
Diretor de Transformação Digital com o PLAUD NOTE Pro.

### Alterações realizadas
- `nomenclatura.md` → v1.0: Seção 4-C (tipo A), Seção 7.6, campos
  data_reuniao/data_registro, nomenclatura agenda-[unidade]
- `sumario.md` → v1.3: tipo A, A01, S06, W02 registrados
- `GLOSSARIO.md` → v1.4: Categoria 8 (6 termos)
- `CONTEXTO.md` → v1.6: S06, W02, A01 adicionados
- `backlog-versoes.md` → esta entrada (v0.24)

---

## v0.23 — 2026-06-02

**Tipo de alteração:** Adição
**Autorizado por:** victorarimatea
**Exposição de motivos:** Implementação do tipo W (Workflows) no ecossistema
DTD/SETIS/SES-DF. O tipo W nasce da visão de que workflows são capital
organizacional crítico — devem estar escritos, versionados, auditáveis e
consultáveis por humanos e ferramentas de IA. A estrutura resolve o problema
dual de memória: o repositório W acumula todas as execuções do processo em
qualquer contexto; o projeto P vê todos os workflows que foram acionados em
seu contexto via EXECUCOES.md. Solução: um único log no W, referenciado no P.

### Alterações realizadas
- `nomenclatura.md` → v0.9: Seção 4-B (estrutura tipo W), Seção 7.5 (backlog
  tipo W), WORKFLOW.md e EXECUCOES.md na tabela de arquivos obrigatórios
- `sumario.md` → v1.2: seção Workflows (W) criada; W01 registrado
- `GLOSSARIO.md` → v1.3: Categoria 7 — 5 novos termos (workflow, subprocesso,
  log de execução, estado final esperado, EXECUCOES.md)
- `CONTEXTO.md` → v1.5: W01 adicionado aos repositórios ativos
- `backlog-versoes.md` → esta entrada (v0.23)

---

## v0.22 — 2026-06-02

**Tipo de alteração:** Atualização
**Autorizado por:** victorarimatea
**Exposição de motivos:** Adição da Categoria 6 ao GLOSSARIO.md com 4 termos
introduzidos pela migração do pipeline de transcrição documental (D01/S05):
"artefato de extração", "front matter YAML", "pipeline de transcrição" e
"reflow". Primeiro ciclo de expansão do glossário por demanda de novo domínio
técnico incorporado ao ecossistema — confirmando o funcionamento da
Verificação 4 da S04 como mecanismo de crescimento orgânico do vocabulário.

### Alterações realizadas
- `GLOSSARIO.md` → v1.2: Categoria 6 adicionada (4 termos — total: 29)
- `backlog-versoes.md` → esta entrada (v0.22)
- `sumario.md` → M01 v0.22 atualizado
- `dtd-setis/CHANGELOG.md` → entrada [2.1]

---

## v0.21 — 2026-06-02

**Tipo de alteração:** Adição
**Autorizado por:** victorarimatea
**Exposição de motivos:** Migração do material produzido no Cowork para
o ecossistema GitHub. Criação do D01 (governanca-ses-df) com 28 documentos
transcritos sobre saúde digital, do S05 (skill-transcricao-documental)
formalizando o pipeline de transcrição, e regularização do D02
(doc-cadastro-ses-setis-dtd) com estrutura padrão. Primeiro preenchimento
da seção Documentos (D) do ecossistema. S02 (skill-iac-pdtic) também
regularizado no sumário — estava ativo mas não registrado.

### Alterações realizadas
- `sumario.md` → v1.1: D01, D02, S05 adicionados; S02 regularizado
- `CONTEXTO.md` → v1.4: D01, D02, S05 adicionados aos repositórios ativos
- `backlog-versoes.md` → esta entrada (v0.21)
- `dtd-setis/CHANGELOG.md` → entrada [2.0]
- `dtd-setis/ROADMAP.md` → governanca-ses-df marcado como ✅

---

## v0.20 — 2026-06-01

**Tipo de alteração:** Atualização
**Autorizado por:** victorarimatea
**Exposição de motivos:** Primeira execução da Verificação 4 (auditoria
de glossário) em operação real — identificou dois termos introduzidos
pela própria operação de criação da Verificação 4 que estavam ausentes
do GLOSSARIO.md: "auditoria de glossário" e "termo candidato". Adição
aprovada pelo mantenedor. Primeiro ciclo completo do mecanismo de
manutenção automática do glossário.

### Alterações realizadas
- `GLOSSARIO.md` → v1.1: 2 termos adicionados na Categoria 5
  ("auditoria de glossário" e "termo candidato")
- `backlog-versoes.md` → esta entrada (v0.20)
- `dtd-setis/CHANGELOG.md` → entrada [1.9]

---

## v0.19 — 2026-06-01

**Tipo de alteração:** Atualização
**Autorizado por:** victorarimatea
**Exposição de motivos:** Atualização da S04 para v1.5 com adição da
Verificação 4 — auditoria de glossário. O glossário criado nesta mesma
sessão (v0.18) agora tem mecanismo automático de manutenção: toda operação
verifica se novos termos foram introduzidos e propõe atualização do
GLOSSARIO.md antes do encerramento. O ecossistema passa a ter memória
terminológica viva e autorreprodutiva.

### Alterações realizadas
- `skill-github-orquestracao/SKILL.md` → v1.5: Verificação 4 adicionada
- `skill-github-orquestracao/backlog-versoes.md` → entrada v1.5
- `sumario.md` → S04 v1.5
- `backlog-versoes.md` → esta entrada (v0.19)
- `dtd-setis/CHANGELOG.md` → entrada [1.8]

---

## v0.18 — 2026-06-01

**Tipo de alteração:** Adição + Atualização
**Autorizado por:** victorarimatea
**Exposição de motivos:** Criação do GLOSSARIO.md — implementação identificada
como quase obrigatória em sistema maduro durante diagnóstico de maturidade.
O glossário formaliza 18 termos em 5 categorias cobrindo toda a terminologia
do ecossistema. Simultâneo: nomenclatura atualizada com referência ao glossário;
sumário atualizado para v1.0 refletindo a maturidade do M01; INDICE.md do M01
atualizado com entrada do glossário; S04 atualizada para v1.4.

### Alterações realizadas
- `GLOSSARIO.md` → criado (v1.0): 18 termos em 5 categorias
- `INDICE.md` → atualizado: GLOSSARIO.md adicionado, total 8 arquivos
- `nomenclatura.md` → v0.8: referência ao GLOSSARIO.md adicionada
- `sumario.md` → v1.0: GLOSSARIO.md no M01; M01 descrito como v0.18;
  S04 atualizado para v1.4
- `backlog-versoes.md` → esta entrada (v0.18)
- `dtd-setis/CHANGELOG.md` → entrada [1.7]

---

## v0.17 — 2026-06-01

**Tipo de alteração:** Adição + Atualização
**Autorizado por:** victorarimatea
**Exposição de motivos:** Implementação do padrão de índices locais em
todos os repositórios públicos do ecossistema, conforme proposta aprovada
durante diagnóstico de maturidade. A proposta resolve a navegação custosa
em repositórios com conteúdo rico, garantindo que qualquer ferramenta ou
humano chegue ao recurso certo sem leitura exaustiva. Simultâneo: S04
atualizada para v1.3 com OP-E clarificado, INDICE.md nas checklists e
Erro #005 registrado. Nomenclatura atualizada para v0.7 com Seção 10.

### Alterações realizadas
- `nomenclatura.md` → v0.7: Seção 10 adicionada — padrão obrigatório
  de INDICE.md em todos os repositórios, sem exceção
- `INDICE.md` criado em: ecossistema-sumario, saude-digital-taxonomia,
  skill-criador-de-skills, skill-poc-saude-digital,
  skill-github-orquestracao, dtd-setis (6 repositórios)
- `README.md` atualizado com link para INDICE.md em todos os 6 repositórios
- `skill-github-orquestracao/SKILL.md` → v1.3: OP-E, INDICE.md, Erro #005
- `skill-github-orquestracao/backlog-versoes.md` → entrada v1.3
- `sumario.md` → v0.9: S04 v1.3, M01 v0.16
- `backlog-versoes.md` → esta entrada (v0.17)
- `dtd-setis/CHANGELOG.md` → entrada [1.6]

---

## v0.16 — 2026-06-01

**Tipo de alteração:** Atualização
**Autorizado por:** victorarimatea
**Exposição de motivos:** Atualização da S04 para v1.2, incorporando o
Erro #004 — segundo ciclo completo de aprendizado contínuo da skill na
mesma sessão de criação. Padrão de busca de entradas em backlog-versoes.md
ampliado para cobrir '## v' e '### v'.

### Alterações realizadas
- `skill-github-orquestracao/SKILL.md` → v1.2: Erro #004 + padrão duplo
- `skill-github-orquestracao/backlog-versoes.md` → entrada v1.2
- `sumario.md` → v0.8: S04 atualizado para v1.2
- `backlog-versoes.md` → esta entrada (v0.16)
- `dtd-setis/CHANGELOG.md` → entrada [1.5]

---

## v0.15 — 2026-06-01

**Tipo de alteração:** Correção + Atualização
**Autorizado por:** victorarimatea
**Exposição de motivos:** Correção de 4 falhas identificadas no diagnóstico
de maturidade do ecossistema realizado durante rodada de perguntas e respostas
com o mantenedor. As falhas cobriam: porta de entrada sem instrução para o
Claude, conflito normativo entre protocolo e S04, drift de versão no sumário,
e ausência de backlog no portfólio público.

### Alterações realizadas
- `dtd-setis/README.md`: bloco de instrução obrigatória adicionado ao topo —
  Claude deve ler o CONTEXTO.md antes de qualquer ação
- `ecossistema-sumario/protocolo-atualizacoes.md` → v2.0: descontinuado
  formalmente; conteúdo original preservado; S04 indicada como substituta
- `ecossistema-sumario/sumario.md` → v0.7: versão do M01 corrigida
  de v0.11 para v0.14 (drift de versão — Erro #002 recorrente)
- `dtd-setis/backlog-versoes.md`: criado com histórico retroalimentado
  (corrige violação da nomenclatura.md — arquivo obrigatório ausente)
- `dtd-setis/CHANGELOG.md` → entrada [1.4]
- `ecossistema-sumario/backlog-versoes.md` → esta entrada (v0.15)

### Falso positivo corrigido
- Item 5 do diagnóstico (M02 backlog incompleto) foi descartado após
  leitura detalhada: a entrada v1.0 existe e está correta — o script
  de auditoria usava '## v' mas o M02 usa '### v' (ver Erro #004 S04)

---

## v0.14 — 2026-06-01

**Tipo de alteração:** Atualização
**Autorizado por:** victorarimatea
**Exposição de motivos:** Atualização da skill S04 para v1.1, incorporando
o primeiro ciclo completo de aprendizado contínuo: erro identificado na
própria sessão de criação da skill, corrigido e registrado antes do
encerramento — exatamente como a Regra 2 do CONTEXTO.md determina.

### Alterações realizadas
- `skill-github-orquestracao/SKILL.md` → v1.1: padrão Python urllib
  obrigatório para chamadas à API; Erro #003 registrado
- `skill-github-orquestracao/backlog-versoes.md` → entrada v1.1
- `sumario.md` → v0.6: S04 atualizado para v1.1

---

## v0.13 — 2026-06-01

**Tipo de alteração:** Atualização
**Autorizado por:** victorarimatea
**Exposição de motivos:** Registro no CONTEXTO.md de duas regras que eliminam
dependência de memória humana para acionar a skill de orquestração do ecossistema.
A Regra 1 (autodescoberta) garante que o Claude acione a S04 automaticamente ao
identificar operações no GitHub, sem precisar ser lembrado pelo usuário. A Regra 2
(aprendizado contínuo) garante que todo erro, aprendizado ou melhoria identificado
na sessão atualize a S04 antes do encerramento — fechando o ciclo de evolução
permanente do ecossistema.

### Alterações realizadas
- `CONTEXTO.md` → v1.3: adição da seção "Protocolo obrigatório para operações
  no GitHub" com Regra 1 (autodescoberta da S04) e Regra 2 (aprendizado contínuo
  e atualização automática da S04), incluindo tabela de critérios de disparo
  (Erro / Aprendizado / Melhoria) e regra de encerramento obrigatória

---

## v0.12 — 2026-06-01

**Tipo de alteração:** Adição
**Autorizado por:** victorarimatea
**Exposição de motivos:** Criação da skill de orquestração do ecossistema (S04),
concebida para garantir que nenhum arquivo fique desatualizado por esquecimento
a cada operação realizada nos repositórios GitHub. A skill nasceu da identificação
de dois erros recorrentes em sessões anteriores: README do portfólio não atualizado
ao criar novos repositórios, e drift de versões entre arquivos do M01. Opera em
duas fases separadas por aprovação explícita: planejamento (sem token) e execução
(com token). Incorpora registro permanente de erros aprendidos.

### Alterações realizadas
- Criação do repositório `skill-github-orquestracao` (público) com 3 arquivos:
  README.md, SKILL.md v1.0, backlog-versoes.md
- `sumario.md` → v0.5: S04 registrado na seção Skills; link adicionado na tabela
- `CONTEXTO.md` → v1.2: S04 adicionado na tabela de repositórios ativos
- `backlog-versoes.md` → esta entrada (v0.12)

---

## v0.11 — 2026-06-01

**Tipo de alteração:** Adição
**Autorizado por:** victorarimatea
**Exposição de motivos:** Criação do tipo P (Projetos) como novo tipo formal de repositório no ecossistema DTD/SETIS, a partir da decisão de estruturar memória institucional permanente para projetos da DTD. O tipo P nasce com estrutura interna padronizada, ciclo de vida controlado e política de visibilidade definida: repositórios privados, com monitoramento público curado no dtd-setis. Primeiro projeto registrado: P01 telessaude-poc-prisional, em decorrência da PoC do Totem Health360 no Sistema Prisional do DF.

### Alterações realizadas
- `nomenclatura.md` → v0.6: adição da Seção 4-A (estrutura interna de projetos), Seção 7.4 (extensões de backlog para tipo P), atualização dos exemplos da Seção 1 com `telessaude-poc-prisional`
- `sumario.md` → v0.4: adição da seção "Projetos (P)"; registro de P01 `telessaude-poc-prisional` (v0.1, status: em_execucao); tabela de links rápidos expandida com coluna de visibilidade
- `backlog-versoes.md` → esta entrada (v0.11)

---

## v0.10 — 2026-05-29

**Tipo de alteração:** Atualização
**Autorizado por:** victorarimatea
**Exposição de motivos:** Separação entre contexto durável e estado operacional transitório no CONTEXTO.md, que vinha acumulando itens de agenda e status de tramitação impróprios para um arquivo de inicialização. Criação do backlog de ações da DTD como fonte única para relatórios de atividade. Na mesma passada, correção de drift pré-existente: ausência da skill S03 e do repositório-mãe dtd-setis nos índices, e desalinhamento da versão do M01 (índices indicavam v0.5 enquanto o backlog já registrava v0.9).

### Alterações realizadas
- `CONTEXTO.md` -> v1.1: bloco de escopo; remoção de estado transitório (datas de reunião, versões em tramitação, tabela "o que já foi produzido"); tabela de repositórios completada com S03 e dtd-setis; referências ao protocolo e ao backlog de ações
- `backlog-acoes-dtd.md` -> criado: histórico retrospectivo de ações e produtos da DTD, com as duas entradas IAC migradas do CONTEXTO
- `nomenclatura.md` -> v0.5: arquivos obrigatórios do M01 completados (CONTEXTO, protocolo, backlog-acoes); seção 5.1 descrevendo o backlog de ações
- `README.md` -> tabela de arquivos atualizada (protocolo e backlog-acoes); versão do repo reconciliada para v0.10
- `sumario.md` -> v0.3: repositório-mãe dtd-setis registrado; versão do M01 reconciliada para v0.10
- `dtd-setis/CHANGELOG.md` -> entrada [0.9] registrando esta operação no portfólio

---

## v0.9 — 2026-05-28

**Tipo de alteração:** Adição
**Autorizado por:** victorarimatea
**Exposição de motivos:** Criação do protocolo-atualizacoes.md, documento de referência
que define o protocolo obrigatório de encerramento para qualquer operação realizada
no ecossistema. O documento nasceu da constatação de que operações de incorporação
de skills ou documentos sempre deixavam pontos em aberto (backlog, sumário, roadmap,
contexto) por falta de uma checklist sistemática. O protocolo cobre 6 tipos de
operação (OP-A a OP-F) com checklists específicas e um modelo de relatório de
encerramento padronizado. É candidato a skill autônoma quando a lógica estiver
madura e o ecossistema tiver mais membros ativos.

### Alterações realizadas
- Criação de `protocolo-atualizacoes.md` v1.0 no ecossistema-sumario
- `nomenclatura.md` referenciado como base para as regras de atualização
- Documento cobre: OP-A (criação de repositório), OP-B (atualização de skill),
  OP-C (atualização de matriz), OP-D (geração de documento institucional),
  OP-E (correção pontual), OP-F (atualização de planejamento ou visão)

---

## v0.8 — 2026-05-28

**Tipo de alteração:** Adição
**Autorizado por:** victorarimatea
**Exposição de motivos:** Incorporação da skill-poc-saude-digital (S03) ao ecossistema.
A skill foi consolidada a partir da experiência acumulada na elaboração da PoC MedNear,
caso zero do Marco Regulatório Interno de PoCs em Saúde Digital da SES-DF.
Inclui protocolo completo de 3 etapas de acentuação, conforme padrão do ecossistema.
O sumario.md foi estruturado pela primeira vez com conteúdo completo (v0.2).

### Alterações realizadas
- Criação do repositório `skill-poc-saude-digital` (público) com 4 arquivos
- `sumario.md` atualizado para v0.2: primeira versão com estrutura completa,
  entrada S03 registrada
- `backlog-versoes.md` atualizado: esta entrada (v0.8)

---

## v0.7 — 2026-05-27

**Tipo de alteração:** Adição
**Autorizado por:** victorarimatea
**Exposição de motivos:** Formalização do protocolo de acentuação em português
como padrão obrigatório do ecossistema. A regra foi descoberta na prática
durante a geração dos documentos IAC e agora é incorporada permanentemente
a todas as skills geradoras de documentos DOCX/PDF, garantindo que qualquer
skill futura criada pelo ecossistema nasça com este padrão.

### Alterações realizadas
- `nomenclatura.md` atualizado para v0.4: seção 9 adicionada
  (padrão de acentuação em documentos gerados)
- `skill-criador-de-skills/SKILL.md`: bloco REGRA DE ACENTUAÇÃO adicionado
  + instrução para propagar o bloco a toda nova skill criada
- `skill-iac-pdtic/SKILL.md`: bloco REGRA DE ACENTUAÇÃO adicionado
  com protocolo completo de 3 etapas (substituição global, títulos, verificação)

---

## v0.6 — 2026-05-27

**Tipo de alteração:** Adição
**Autorizado por:** victorarimatea
**Exposição de motivos:** Criação do CONTEXTO.md para permitir inicialização
rápida de novas sessões de trabalho sem necessidade de reexplicar o ecossistema.
O arquivo consolida em um único documento: identidade do mantenedor, estrutura
do ecossistema, convenções, modelo IAC, governança SES-DF, histórico de
produções e próximos passos planejados.

### Alterações realizadas
- Criação do `CONTEXTO.md` v1.0 com briefing completo do ecossistema
- Atualização do `README.md` para incluir `CONTEXTO.md` na tabela de arquivos
- Instrução de inicialização de sessão adicionada ao README

---

# Backlog de Versões — ecossistema-sumario

## v0.5 — 2026-05-27

**Tipo de alteração:** Atualização
**Autorizado por:** victorarimatea
**Exposição de motivos:** Registro das evoluções do ecossistema ocorridas em
27/05/2026 após extenso trabalho de desenvolvimento e refinamento do modelo IAC,
geração dos documentos IAC-V e IAC-H do PDTIC, e consolidação da estrutura
de governança da SES-DF como conhecimento do ecossistema.

### Alterações realizadas
- `sumario.md` atualizado para v0.5:
  - skill-iac-pdtic registrada como v2.0
  - Descrição da S02 atualizada para refletir IAC-V e IAC-H
  - Seção do modelo IAC adicionada como padrão do ecossistema
  - Registro de próximo repositório previsto: `governanca-ses-df` (tipo D)
- `nomenclatura.md` atualizado para v0.3:
  - Adição da seção 8 — Modelo IAC como padrão do ecossistema
  - Documentação de IAC-V e IAC-H
  - Estrutura obrigatória e nomenclatura de arquivos IAC
- `skill-iac-pdtic` atualizada para v2.0 (ver backlog da skill)

### Estado do ecossistema nesta versão
- Matrizes (M): 2 — M01 ecossistema-sumario (v0.5), M02 saude-digital-taxonomia (v1.0)
- Skills (S): 2 — S01 skill-criador-de-skills (v1.0), S02 skill-iac-pdtic (v2.0)
- Documentos (D): 0 — governanca-ses-df previsto

---

## v0.4 — 2026-05-26

**Tipo de alteração:** Adição
**Autorizado por:** victorarimatea
**Exposição de motivos:** Registro da segunda skill do ecossistema.
A skill-iac-pdtic (S02) foi criada via API do GitHub pela própria
skill-criador-de-skills (S01) — primeiro teste bem-sucedido do
fluxo automatizado do ecossistema.

### Alterações realizadas
- Adição da entrada S02 na seção [S] do `sumario.md`
- Ecossistema passa a ter 2 Matrizes (M) e 2 Skills (S) registradas

---

## v0.3 — 2026-05-26

**Tipo de alteração:** Adição
**Autorizado por:** victorarimatea
**Exposição de motivos:** Registro da primeira skill do ecossistema.

### Alterações realizadas
- Adição da entrada S01 na seção [S] do `sumario.md`

---

## v0.2 — 2026-05-26

**Tipo de alteração:** Adição
**Autorizado por:** victorarimatea
**Exposição de motivos:** Adoção do padrão mínimo com extensões por tipo de
repositório, preservando o formato rico do backlog da taxonomia.

### Alterações realizadas
- Adição da seção 7 ao `nomenclatura.md`
- Correção do cabeçalho de versão no `taxonomia.md`

---

## v0.1 — 2026-05-26

**Tipo de alteração:** Criação
**Autorizado por:** victorarimatea
**Exposição de motivos:** Fundação do ecossistema DTD/SETIS.

### Alterações realizadas
- Criação do repositório `ecossistema-sumario`
- Criação do `README.md`, `sumario.md`, `nomenclatura.md`, `backlog-versoes.md`

### Repositórios registrados
- M01 — ecossistema-sumario
- M02 — saude-digital-taxonomia
