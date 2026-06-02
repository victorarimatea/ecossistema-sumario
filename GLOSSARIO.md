# Glossário — Ecossistema DTD/SETIS

**Versão:** v1.3 — 2026-06-02
**Repositório:** ecossistema-sumario (M01)
**Mantenedor:** victorarimatea

> Definições formais dos termos utilizados no ecossistema DTD/SETIS.
> Este glossário é a fonte de verdade para qualquer dúvida de terminologia.
> Termos em uso nos documentos, skills e matrizes devem estar aqui definidos.
> Atualizar sempre que um novo termo for introduzido no ecossistema.

---

## Como usar este glossário

- Para entender um termo encontrado em qualquer documento do ecossistema,
  consulte este arquivo primeiro.
- Para introduzir um novo termo no ecossistema, defini-lo aqui é obrigatório
  antes de usá-lo em outras documentações.
- Os termos estão organizados em ordem alfabética dentro de cada categoria.

---

## Categoria 1 — Tipos de repositório

**Documento (tipo D)**
Repositório dedicado ao armazenamento e versionamento de documentos
institucionais: instrumentos normativos, históricos de análise, pareceres
formais. Exemplo: `pdtic-historico`. Identificado pela letra D no sumário.

**Matriz (tipo M)**
Repositório que contém conhecimento estrutural do ecossistema — convenções,
taxonomias, sumários, protocolos. É fonte de verdade consultada por skills
e por qualquer instância do Claude antes de agir. Exemplo: `ecossistema-sumario`
(M01), `saude-digital-taxonomia` (M02). Identificado pela letra M no sumário.

**Projeto (tipo P)**
Repositório privado que registra e acompanha o desenvolvimento de um projeto
institucional específico da DTD. Contém atas de reunião, stakeholders,
documentos aprovados e backlog de decisões. Exemplo: `telessaude-poc-prisional`
(P01). Identificado pela letra P no sumário.

**Skill (tipo S)**
Repositório que contém instruções estruturadas para o Claude executar uma
tarefa específica de forma padronizada e repetível. O arquivo principal é
o `SKILL.md`. Exemplo: `skill-github-orquestracao` (S04). Identificado
pela letra S no sumário.

---

## Categoria 2 — Arquivos obrigatórios

**backlog-versoes.md**
Arquivo presente em todo repositório do ecossistema. Registra o histórico
de decisões e motivações por trás de cada alteração — responde à pergunta
"por que isso foi mudado?". Complementa o `CHANGELOG.md`, que registra
o quê foi mudado. Ver distinção completa em `CHANGELOG.md` abaixo.

**CHANGELOG.md**
Arquivo presente exclusivamente no repositório `dtd-setis` (portfólio público).
Registra o histórico de entregas e versões do ecossistema como um todo —
responde à pergunta "o que foi construído e quando?". Não substitui o
`backlog-versoes.md`: o changelog registra o resultado; o backlog registra
o raciocínio. Toda entrada do changelog tem uma entrada de backlog
correspondente em algum repositório, mas o inverso não é verdade.

**CONTEXTO.md**
Arquivo exclusivo do M01. Briefing completo do ecossistema para inicialização
de sessões do Claude. Contém: estrutura atual, repositórios ativos, convenções,
protocolo de operações GitHub (S04), regras de autodescoberta e aprendizado
contínuo. Leitura obrigatória antes de qualquer sessão de trabalho.

**GLOSSARIO.md**
Este arquivo. Definições formais de todos os termos do ecossistema. Exclusivo
do M01. Deve ser atualizado sempre que um novo termo for introduzido.

**INDICE.md**
Arquivo presente em todo repositório do ecossistema. Mapa completo de
conteúdo: lista todos os arquivos e pastas com descrição e orientação de
quando consultar cada um. Permite navegação direta sem leitura exaustiva
do repositório — essencial para evitar consumo desnecessário de créditos
e tempo em repositórios com conteúdo rico.

**nomenclatura.md**
Arquivo exclusivo do M01. Define as convenções obrigatórias do ecossistema:
nomenclatura de repositórios, arquivos, versões, estrutura interna de cada
tipo, padrão IAC, padrão de acentuação. Toda criação ou atualização de
repositório deve verificar conformidade com este arquivo.

**sumario.md**
Arquivo exclusivo do M01. Índice geral do ecossistema: lista todos os
repositórios ativos com tipo, versão, status e descrição. É o ponto de
entrada para saber o que existe no ecossistema. Ver também: repositório âncora.

---

## Categoria 3 — Instrumentos institucionais

**IAC — Instrumento de Análise Comparativa**
Documento padronizado de governança documental criado pela DTD. Opera em
dois modos: IAC-V (Vertical) para comparar versões diferentes do mesmo
documento, e IAC-H (Horizontal) para verificar conformidade entre documentos
distintos. Gerado pela skill S02 (`skill-iac-pdtic`). Estrutura obrigatória
de 8 seções definida na `nomenclatura.md`.

**PoC — Prova de Conceito**
Documento padronizado de avaliação de soluções tecnológicas em saúde,
criado pela DTD. Estrutura com 11 seções obrigatórias: contexto, objetivos,
escopo, fluxo operacional, governança, cronograma, métricas, gestão de
riscos, aspectos regulatórios, deliberações pendentes e resultado esperado.
Gerado pela skill S03 (`skill-poc-saude-digital`). Não configura pesquisa
clínica (Resolução CNS nº 466/2012) quando de caráter técnico-operacional.

---

## Categoria 4 — Operações e versionamento

**Breaking / Non-breaking**
Classificação de impacto de uma atualização de skill. Breaking: a mudança
torna versões anteriores da skill incompatíveis ou inválidas — requer
atenção de quem usa a skill. Non-breaking: melhoria compatível com o
comportamento anterior — pode ser adotada sem ajustes.

**MAJOR / MINOR (versionamento)**
Componentes do número de versão no formato `vMAJOR.MINOR`. MAJOR é
incrementado quando a mudança torna versões anteriores incompatíveis
ou inválidas. MINOR é incrementado para melhorias, adições e correções
compatíveis com a versão anterior. Exemplo: v1.0 → v1.1 (MINOR);
v1.3 → v2.0 (MAJOR).

**OP-A, OP-B, OP-C, OP-D, OP-E, OP-F, OP-P**
Códigos de classificação de operações no ecossistema, definidos na S04:
OP-A (criação de repositório), OP-B (atualização de skill), OP-C
(atualização de matriz), OP-D (geração de documento), OP-E (correção
pontual), OP-F (atualização de planejamento), OP-P (atualização de
projeto). Cada tipo tem checklist própria de arquivos a atualizar.

---

## Categoria 5 — Conceitos de qualidade e governança

**Auditoria de glossário**
Verificação obrigatória realizada ao final de toda operação da S04
(exceto OP-E sem conteúdo novo). Consiste em varrer os arquivos criados
ou alterados na operação em busca de termos técnicos novos — substantivos
específicos do ecossistema, siglas, conceitos operacionais — e compará-los
com o `GLOSSARIO.md`. Termos ausentes são propostos para adição antes do
encerramento da operação. Implementada como Verificação 4 da Etapa 6 da
skill-github-orquestracao (S04 v1.5). Garante que o glossário cresça
naturalmente com o ecossistema sem depender de atualização manual.

**Termo candidato**
Termo identificado durante uma auditoria de glossário que está em uso em
documentos do ecossistema mas ainda não possui definição formal no
`GLOSSARIO.md`. Todo termo candidato deve ser avaliado pelo mantenedor
antes de ser incorporado: o mantenedor pode aprovar a adição com a
definição proposta, solicitar ajuste na definição, ou rejeitar a inclusão
caso o termo seja referência interna de estrutura sem necessidade de
definição formal (exemplo: "Verificação 4" como referência a etapa
numerada da S04).

**Drift documental**
Condição em que dois ou mais arquivos do ecossistema que deveriam estar
sincronizados passam a apresentar informações divergentes por falta de
propagação de uma atualização. Exemplo clássico: `sumario.md` registrando
versão v0.11 de um repositório quando o `backlog-versoes.md` já está em
v0.14. O drift é detectado na Etapa 6 (Verificação 1) da S04 e corrigido
imediatamente, ainda com o token ativo.

**Falso positivo (no contexto de auditoria)**
Resultado incorreto de um script de auditoria que indica ausência de algo
que na verdade existe. No ecossistema, falsos positivos ocorreram por:
padrão de busca de texto restrito (Erros #004 e #005), janela de busca
insuficiente (Erro #005), e leitura de trecho em vez do conteúdo completo
(Erro #006). A S04 incorpora correções para cada caso identificado.

**Porta de entrada**
O repositório `dtd-setis` — ponto de acesso público ao ecossistema
DTD/SETIS. Contém o README com diagrama geral, lista de repositórios,
skills disponíveis, instrução obrigatória de inicialização para o Claude
e link para o monitoramento de projetos. Qualquer pessoa ou ferramenta
que acesse o ecossistema deve começar aqui.

**Repositório âncora**
O repositório `ecossistema-sumario` (M01) — repositório que contém as
matrizes de conhecimento que regem todo o ecossistema. É a fonte de
verdade para convenções (nomenclatura), estrutura (sumário), contexto
(CONTEXTO.md) e terminologia (GLOSSARIO.md). Toda skill lê o repositório
âncora antes de executar qualquer tarefa. Distinto da "porta de entrada"
(`dtd-setis`): a porta de entrada é pública e orientada ao humano; o
repositório âncora é técnico e orientado ao Claude.

---

## Categoria 6 — Pipeline de Transcrição Documental

**Artefato de extração**
Elemento capturado indevidamente pelo extrator de PDF que não faz parte
do texto normativo do documento. Exemplos típicos: timestamps do DOU
(`27/04/2026, 23:46`), URLs de acesso, cabeçalhos de página repetidos
(`DIÁRIO OFICIAL DA UNIÃO`), numerações de página (`3/118`), metadados
de portais (`Publicado em:`, `Órgão:`, `Edição:`), rodapés de sistemas
legais (`Saúde Legis - Sistema de Legislação da Saúde`). Artefatos são
eliminados pelo filtro `SKIP_EXACT` / `SKIP_RE` da Etapa 2 do pipeline
antes de qualquer processamento do conteúdo. A presença de artefatos no
arquivo transcrito é critério de falha na auto-verificação (Etapa 5).

**Front Matter YAML**
Bloco de metadados estruturados em formato YAML colocado no início de cada
arquivo Markdown transcrito, delimitado por `---`. Contém 13 campos
obrigatórios que identificam e descrevem o documento: `id_documento`,
`titulo`, `tipo_documental`, `instituicao_origem`, `autor`, `data_criacao`,
`data_publicacao`, `idioma`, `status_documental`, `arquivo_original`,
`fonte_externa`, `data_transcricao` e `versao_transcricao`. Documentos
bilíngues (Fase 2) recebem 3 campos adicionais: `idioma_original`,
`versao_idioma` e `documento_par`. O Front Matter é a Seção 1 da estrutura
obrigatória de 5 seções de cada arquivo transcrito e serve como base para
indexação, busca e rastreabilidade futura dos documentos do ecossistema.

**Pipeline de transcrição**
Conjunto estruturado de etapas, filtros, algoritmos e verificações que
converte documentos PDF regulatórios em arquivos Markdown estruturados,
auditáveis e reutilizáveis. No ecossistema DTD/SETIS/SES-DF, o pipeline
é formalizado pela skill S05 (`skill-transcricao-documental`) e especificado
tecnicamente no `WORKFLOW-ESPECIFICACAO.md` do repositório D01
(`governanca-ses-df`). Opera em 7 etapas: leitura de contexto, extração do
PDF, limpeza e reflow, estrutura jurídica, montagem do Markdown,
auto-verificação e atualização do workflow. Desenvolvido ao longo das
Fases 1 e 2 Tier 1, com 8 problemas documentados (P01–P08) e roadmap de
automação progressiva.

**Reflow**
Operação de processamento de texto que reconstrói parágrafos coerentes a
partir de blocos de texto fragmentados pela extração de PDF. Durante a
extração por `get_text("blocks")`, PDFs com justificação extrema ou colunas
estreitas produzem quebras de linha artificiais dentro de parágrafos —
cada linha do PDF vira uma linha separada no texto extraído. O reflow
(`reflow_block_lines()`) resolve isso juntando as linhas de cada bloco com
espaço, exceto quando a linha seguinte inicia um marcador estrutural jurídico
(artigo, parágrafo, inciso, etc.) ou quando a linha anterior termina com
hífen (hifenização — junção sem espaço). Quebras espúrias não corrigidas
pelo reflow são detectadas na auto-verificação (Etapa 5) como alerta: mais
de 3 linhas consecutivas com menos de 40 caracteres.


---

---

## Categoria 7 — Workflows e Processos Organizacionais

**Estado final esperado**
Conjunto de critérios verificáveis que define quando uma execução de workflow
foi bem-sucedida. Distinto de "objetivo" — o estado final esperado é operacional
e auditável: cada critério é uma condição binária que pode ser checada por um
agente humano ou de IA ao final da execução. Na estrutura do WORKFLOW.md, ocupa
a Seção 3 e funciona como o benchmark de qualidade do processo.

**EXECUCOES.md**
Arquivo obrigatório na raiz de repositórios do tipo P (Projetos) que lista todos
os workflows acionados no contexto daquele projeto. Não duplica o conteúdo dos
logs de execução — apenas referencia cada log com link para o repositório W onde
o log completo reside. Garante que o projeto tenha visão consolidada de todos os
processos que foram executados em seu contexto, sem criar drift documental.

**Log de execução**
Arquivo criado em `workflow-[descritor]/execucoes/` a cada execução registrada
de um workflow. Contém: data e contexto de acionamento, executor, projeto
associado, resumo de etapas, decisões tomadas, desvios do padrão, artefatos
gerados, status e lições aprendidas. É a fonte de verdade do histórico de
execuções — o `EXECUCOES.md` do projeto apenas o referencia. Em sessões
autenticadas com token, a criação do log é obrigatória antes do encerramento.

**Subprocesso**
Workflow consumido por outro workflow de nível superior como parte de suas
etapas. O subprocesso é um workflow completo e autônomo — tem seu próprio
repositório W, seu próprio WORKFLOW.md e seus próprios logs de execução.
Quando consumido por um workflow pai, é referenciado na Seção 5 do WORKFLOW.md
do pai sem duplicar seu conteúdo. Exemplo: `workflow-transcricao-documental`
pode ser consumido como subprocesso por `workflow-iac-conformidade` quando
este identifica um gap normativo que requer transcrição antes de prosseguir.

**Workflow**
Repositório do tipo W que contém a descrição organizacional completa de um
processo da DTD/SETIS/SES-DF — desde a missão e contexto até o roadmap de
automação. Distinto de skill (tipo S): enquanto a skill contém as instruções
técnicas para uma IA executar uma tarefa, o workflow descreve o processo do
ponto de vista organizacional, incluindo etapas manuais, histórico de problemas,
memória institucional e log de execuções. Um workflow pode existir sem skill
associada (processo ainda manual). Uma skill sem workflow é tecnicamente válida
mas organizacionalmente incompleta. A relação é: o workflow é anterior e superior
à skill; a skill automatiza uma ou mais etapas do workflow.

---

*Última revisão: 2026-06-02 — victorarimatea*
*Para propor novos termos: abrir issue ou atualizar diretamente via S04.*
