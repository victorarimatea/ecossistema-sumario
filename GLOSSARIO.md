# Glossário — Ecossistema DTD/SETIS

**Versão:** v2.0 — 2026-06-06
**Repositório:** hub-fonte (M01)
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


---

# PARTE I — Ecossistema DTD/SETIS (infraestrutura)

## Categoria 1 — Tipos de repositório

**Documento (tipo D)**
Repositório dedicado ao armazenamento e versionamento de documentos
institucionais: instrumentos normativos, históricos de análise, pareceres
formais. Exemplo: `pdtic-historico`. Identificado pela letra D no sumário.

**Matriz (tipo M)**
Repositório que contém conhecimento estrutural do ecossistema — convenções,
taxonomias, sumários, protocolos. É fonte de verdade consultada por skills
e por qualquer instância do Claude antes de agir. Exemplo: `hub-fonte`
(M01), `mat-saude-digital-taxonomia` (M02). Identificado pela letra M no sumário.

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

**Workflow (tipo W)**
Repositório que codifica um processo institucional completo com etapas,
responsáveis, entradas, saídas e critérios de conclusão. Estrutura obrigatória:
WORKFLOW.md (processo completo em 8+ seções), README.md, INDICE.md,
backlog-versoes.md, pasta execucoes/. Nomenclatura: `wkf-[nome]`. Identificador
de série: W01, W02, W03… Exemplos: wkf-registro-sessao (W03),
wkf-auditoria-consistencia (W05), wkf-sessao-agente (W06). Identificado
pela letra W no sumário.

---

## Categoria 2 — Arquivos obrigatórios

**backlog-versoes.md**
Arquivo presente em todo repositório do ecossistema. Registra o histórico
de decisões e motivações por trás de cada alteração — responde à pergunta
"por que isso foi mudado?". Complementa o `CHANGELOG.md`, que registra
o quê foi mudado. Ver distinção completa em `CHANGELOG.md` abaixo.

**CHANGELOG.md**
Arquivo presente exclusivamente no repositório `hub-entrada` (portfólio público).
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

**OP-A, OP-B, OP-C, OP-D, OP-E, OP-F, OP-P, OP-W, OP-AG**
Códigos de classificação de operações no ecossistema, definidos na S04:
OP-A (criação de repositório), OP-B (atualização de skill), OP-C
(atualização de matriz), OP-D (geração de documento), OP-E (correção
pontual), OP-F (atualização de planejamento), OP-P (atualização de
projeto), OP-W (atualização de workflow), OP-AG (atualização de agenda).
Cada tipo tem checklist própria de arquivos a atualizar.

---

## Categoria 5 — Conceitos de qualidade e governança

**Auditoria de glossário**
*Ver também: Auditabilidade de IA (Parte II, Cat. 11) — conceito distinto, voltado a sistemas de inteligência artificial.*
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
O repositório `hub-entrada` — ponto de acesso público ao ecossistema
DTD/SETIS. Contém o README com diagrama geral, lista de repositórios,
skills disponíveis, instrução obrigatória de inicialização para o Claude
e link para o monitoramento de projetos. Qualquer pessoa ou ferramenta
que acesse o ecossistema deve começar aqui.

**Repositório âncora**
O repositório `hub-fonte` (M01) — repositório que contém as
matrizes de conhecimento que regem todo o ecossistema. É a fonte de
verdade para convenções (nomenclatura), estrutura (sumário), contexto
(CONTEXTO.md) e terminologia (GLOSSARIO.md). Toda skill lê o repositório
âncora antes de executar qualquer tarefa. Distinto da "porta de entrada"
(`hub-entrada`): a porta de entrada é pública e orientada ao humano; o
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

---

## Categoria 8 — Agenda e Registros de Reunião

**Agenda (tipo A)**
Repositório do tipo A que contém o acervo cronológico de registros de reunião
de uma unidade organizacional. Distinto de todos os outros tipos do ecossistema
por ser indexado por tempo de ocorrência dos eventos (não pela ordem de criação
no ecossistema). A estrutura de pastas `reunioes/AAAA/MM/` e a nomenclatura
`AAAA-MM-DD-[CLASSIFICACAO]-[descricao].md` garantem ordenação cronológica
natural. Repositórios do tipo A são nomeados `agenda-[unidade]` e são privados
por padrão — contêm informações institucionais sensíveis sobre reuniões internas.
Exemplo: `agenda-dtd` (A01).

**data_registro**
Campo do Front Matter YAML de registros de reunião que indica quando o arquivo
foi inserido no repositório A — distinto da `data_reuniao`. Serve para
rastreabilidade de quando o registro foi formalizado, especialmente em casos
de registros retroativos (reuniões que ocorreram antes da criação do repositório
A ou antes da disponibilidade de token para depósito automático). A data de
commit no git também registra essa informação automaticamente.

**data_reuniao**
Campo do Front Matter YAML de registros de reunião que indica quando a reunião
efetivamente aconteceu. Determina a posição do arquivo na estrutura de pastas
(`reunioes/AAAA/MM/`), no nome do arquivo (`AAAA-MM-DD-...`) e no índice
cronológico do repositório A. Uma reunião ocorrida em maio aparece em maio no
índice mesmo que o registro tenha sido criado em junho.

**índice cronológico**
O INDICE.md de repositórios do tipo A lista as reuniões em ordem de ocorrência
(`data_reuniao`), não de inserção no repositório. É o único caso no ecossistema
em que o índice não segue a ordem de criação dos arquivos. Permite que o índice
funcione como linha do tempo consultável da agenda institucional — mesmo quando
os registros são inseridos retroativamente ou fora de ordem.

**PLAUD NOTE Pro**
Dispositivo de hardware de captura e transcrição de reuniões utilizado pelo
Diretor de Transformação Digital da DTD/SETIS/SES-DF. Grava o áudio das reuniões
e gera automaticamente sínteses estruturadas que servem como input para o
workflow W02 (`workflow-registro-reuniao`) e a skill S06 (`skill-registro-reuniao`).
A aquisição do dispositivo foi uma decisão estratégica de produtividade que
habilitou a construção do workflow de registro institucional de reunião.

**registro institucional de reunião**
Documento padronizado produzido pela skill S06 a partir de resumos de reunião,
com 8 seções obrigatórias: título (com classificação), metadados, contexto,
principais pontos discutidos, decisões, encaminhamentos, pontos críticos e
referência. Redigido em linguagem institucional (padrão SES-DF / administração
pública), diretamente utilizável em processos formais (SEI) sem edição adicional.
Armazenado no repositório A da unidade responsável e referenciado no projeto P
quando associado a projeto formal.

---

---

# PARTE II — Saúde Digital (domínio normativo)

> Termos extraídos e revisados a partir das fontes normativas e regulatórias
> que fundamentam a atuação da DTD/SETIS/SES-DF. Incluídos na versão v1.5
> a partir de análise conduzida no NotebookLM sobre o corpus documental do
> repositório D01 (`doc-governanca-ses-df`).

---

## Categoria 9 — Modalidades Assistenciais e Atos Remotos

**Telecirurgia**
Realização de procedimento cirúrgico a distância, com utilização de equipamento
robótico e mediada por tecnologias interativas seguras.

**Teleconsulta**
Consulta médica não presencial, mediada por Tecnologias Digitais, de Informação
e de Comunicação (TDICs), com médico e paciente localizados em diferentes espaços.

**Teleconsultoria**
Ato de consultoria mediado por TDICs entre médicos, gestores e outros profissionais
de saúde, com a finalidade de prestar esclarecimentos sobre procedimentos
administrativos e ações de saúde.

**Telediagnóstico**
Ato médico realizado à distância, geográfica e/ou temporal, com a transmissão de
gráficos, imagens e dados para emissão de laudo ou parecer por médico com registro
de qualificação de especialista (RQE).

**Teleinterconsulta**
Troca de informações e opiniões entre médicos ou profissionais de saúde, com ou
sem a presença do paciente, para auxílio diagnóstico ou terapêutico, clínico ou
cirúrgico.

**Telemedicina**
Exercício da medicina mediado por TDICs para fins de assistência, educação,
pesquisa, prevenção de doenças e lesões, gestão e promoção de saúde.

**Telemonitoramento ou Televigilância**
Ato realizado sob coordenação e supervisão médica para monitoramento ou vigilância
a distância de parâmetros de saúde e/ou doença, por meio de aquisição direta de
imagens, sinais e dados.

**Telessaúde**
Termo de abrangência ampla que se aplica ao uso das TDICs para transferir
informações e serviços clínicos, administrativos e educacionais, realizados por
diversos profissionais de saúde, respeitadas suas competências legais.

**Teletriagem**
Ato realizado por médico com avaliação dos sintomas do paciente, a distância,
para regulação assistencial, com definição e direcionamento ao tipo adequado de
assistência ou especialista.

---

## Categoria 10 — Dados, Privacidade e Segurança da Informação

**Anonimização**
Utilização de meios técnicos razoáveis e disponíveis no momento do tratamento,
por meio dos quais um dado perde a possibilidade de associação, direta ou
indireta, a um indivíduo.

**Cibersegurança**
Estado em que informações e sistemas são protegidos contra atividades não
autorizadas (acesso, uso, interrupção ou destruição), mantendo a
confidencialidade, integridade e disponibilidade.

**Dado Pessoal**
Informação relacionada a pessoa natural identificada ou identificável.

**Dado Pessoal Sensível**
Dado pessoal sobre origem racial ou étnica, convicção religiosa, opinião
política, saúde, vida sexual, dado genético ou biométrico, quando vinculado
a uma pessoa natural.

**Encarregado (DPO)**
Pessoa indicada pelo controlador e operador para atuar como canal de comunicação
entre a instituição, os titulares dos dados e a Autoridade Nacional de Proteção
de Dados (ANPD).

**Pseudonimização**
Tratamento por meio do qual um dado perde a possibilidade de associação a um
indivíduo, senão pelo uso de informação adicional mantida separadamente pelo
controlador.

**Tratamento de Dados**
Toda operação realizada com dados pessoais, como coleta, recepção, classificação,
utilização, acesso, processamento, armazenamento, eliminação e transferência.

---

## Categoria 11 — Infraestrutura, Tecnologia e Inteligência Artificial

**Auditabilidade de IA**
Capacidade de um sistema de IA ser submetido a avaliação independente de seus
algoritmos, dados, processos de concepção ou resultados para verificar
conformidade ética e legal.
*Ver também: Auditoria de glossário (Parte I, Cat. 5) — conceito distinto,
voltado ao processo interno de verificação terminológica do ecossistema.*

**Inteligência Artificial Generativa (IA Generativa)**
Sistema de IA destinado a gerar ou modificar significativamente conteúdos
(texto, imagem, áudio) a partir de entradas (*prompts*) fornecidas pelo usuário.

**Interoperabilidade**
Capacidade de dois ou mais dispositivos ou sistemas para trocar informações e
utilizá-las para a correta execução de uma função especificada sem alterar o
conteúdo dos dados.

**Modelo de Linguagem de Larga Escala (LLM)**
Subclassificação de IA generativa consistente em modelos de processamento de
linguagem natural capazes de compreender e gerar linguagem em formato escrito.

**Sistema de Inteligência Artificial (Sistema de IA)**
Sistema baseado em máquina que, com diferentes níveis de autonomia, processa
dados para gerar resultados como decisões, recomendações ou predições que
influenciam ambientes virtuais ou físicos.

**Software como Dispositivo Médico (SaMD)**
Software destinado a finalidades médicas (diagnóstico, prevenção, tratamento)
que realiza essas funções sem fazer parte do hardware de um dispositivo médico.

---

## Categoria 12 — Estratégia, Gestão e Governança Digital

**Governança em Saúde Digital**
Conjunto de lideranças, estratégias, políticas e regras para promover, orientar,
monitorar e inovar a saúde digital sob os princípios de privacidade e
planejamento financeiro.

**Índice Nacional de Maturidade em Saúde Digital (INMSD)**
Representação dos resultados de métricas utilizadas para o diagnóstico,
monitoramento e avaliação do grau de digitalização de estados e municípios.

**Prontuário Médico / Registro Eletrônico de Saúde (RES)**
Sistema informatizado para a guarda, o armazenamento e o manuseio do histórico
clínico do paciente, assegurando integridade, autenticidade e confidencialidade.

**Saúde Digital**
Campo que norteia as ações relativas ao uso de tecnologias digitais integradas
ao sistema de saúde para o período de 2020 a 2028, visando a implementação da
Rede Nacional de Dados em Saúde (RNDS).

---

## Categoria 13 — Monitoramento e Inteligência Organizacional

**Gestão por Exceção**
Modelo gerencial em que a atenção e o acionamento são direcionados
prioritariamente para desvios relevantes em relação ao comportamento esperado,
em vez de acompanhamento contínuo e periódico de todos os indicadores.
No contexto do ecossistema, a gestão por exceção pode ser aplicada a processos
estáveis onde o briefing periódico seria redundante — o agente só é acionado
quando um limiar de desvio é atingido.

**Pergunta orientadora:**
O que saiu do padrão e exige atenção agora?

**Monitoramento de Conformidade**
Processo contínuo de verificação da aderência de processos, sistemas, projetos
e decisões a normas legais, regulatórias, técnicas ou institucionais.
No contexto do ecossistema, pode acompanhar aderência à LGPD, normas de
interoperabilidade, requisitos contratuais, diretrizes da SES-DF, resoluções
profissionais e marcos regulatórios de saúde digital.

**Pergunta orientadora:**
Estamos atuando dentro das regras aplicáveis?

**Monitoramento de Desempenho**
Processo contínuo de acompanhamento de indicadores relacionados à eficiência,
produtividade, efetividade ou alcance de metas institucionais.
No contexto do ecossistema, o monitoramento de desempenho pode acompanhar
tempo-resposta, volume de atendimentos, cumprimento de prazos, produtividade
de equipes, evolução de indicadores estratégicos e aderência a metas pactuadas.

**Pergunta orientadora:**
Estamos alcançando os resultados esperados?

**Monitoramento de Qualidade**
Processo contínuo de acompanhamento da conformidade, completude, consistência
e adequação dos processos, registros ou entregas em relação a padrões
previamente definidos.
No contexto do ecossistema, o monitoramento de qualidade pode observar se
fichas digitais estão completas, se campos obrigatórios foram preenchidos,
se protocolos foram seguidos, se dados estão consistentes e se produtos
institucionais atendem aos critérios mínimos de governança.

**Pergunta orientadora:**
Estamos fazendo da forma correta?

**Monitoramento de Segurança**
Processo contínuo de identificação de riscos, ameaças, falhas, eventos adversos
ou violações que possam comprometer pessoas, processos, sistemas, dados ou a
continuidade dos serviços.
No contexto do ecossistema, pode envolver segurança da informação, privacidade,
acessos indevidos, falhas operacionais, eventos adversos assistenciais e riscos
institucionais.

**Pergunta orientadora:**
Há algum risco emergente que exige resposta?

**Monitoramento de Tendências**
Processo de acompanhamento de padrões emergentes, variações progressivas ou
mudanças de comportamento em dados, processos ou contextos institucionais.
No contexto do ecossistema, pode apoiar a identificação precoce de aumento de
demanda, mudança no perfil assistencial, saturação de serviços, riscos sazonais
ou oportunidades de inovação.

**Pergunta orientadora:**
Que mudança está começando a aparecer?

**Monitoramento Estratégico**
Processo contínuo de acompanhamento do ambiente externo e dos objetivos
institucionais de longo prazo, identificando movimentos relevantes em regulação,
mercado, tecnologia, política e cenário setorial que possam impactar a direção
da organização.
No contexto do ecossistema, o monitoramento estratégico é operacionalizado pela
skill S07 (`skl-briefing-saude-digital`), que realiza varredura periódica de
fontes externas classificando os achados pela taxonomia de saúde digital (M02).

**Pergunta orientadora:**
O que está mudando no ambiente que precisa da nossa atenção?

**Monitoramento Operacional**
Processo contínuo de acompanhamento do funcionamento cotidiano de processos,
serviços e sistemas institucionais, verificando se as operações estão ocorrendo
conforme planejado, dentro dos parâmetros esperados de fluxo, prazo e
disponibilidade.
No contexto do ecossistema, o monitoramento operacional pode acompanhar a
execução de workflows, o status de projetos em andamento, a disponibilidade
de sistemas de saúde, o cumprimento de etapas de processos institucionais e
a regularidade de registros operacionais.

**Pergunta orientadora:**
O que está acontecendo agora?

---

## Categoria 14 — Análise de Dados e Business Intelligence

**Analytics**
Disciplina dedicada à extração de conhecimento a partir de dados, abrangendo
desde a análise descritiva de eventos passados até modelos preditivos e
prescrições de ação. No ecossistema, Analytics é a capacidade analítica que
sustenta a tomada de decisão baseada em evidências.

**Análise Descritiva**
Modalidade analítica que organiza e resume dados históricos para responder
à pergunta: *O que aconteceu?*

**Análise Diagnóstica**
Modalidade analítica que investiga causas e correlações em dados históricos
para responder à pergunta: *Por que aconteceu?*

**Análise Preditiva**
Modalidade analítica que utiliza modelos estatísticos e de aprendizado de
máquina para antecipar comportamentos futuros e responder à pergunta:
*O que provavelmente acontecerá?*

**Análise Prescritiva**
Modalidade analítica que recomenda cursos de ação com base em dados e modelos,
respondendo à pergunta: *O que devemos fazer?*

**Business Intelligence (BI)**
Conjunto de processos, metodologias e ferramentas destinados à coleta,
integração e análise retrospectiva de dados para apoiar decisões gerenciais
e estratégicas. Distinto de Analytics pela ênfase no histórico e nos relatórios
estruturados, em oposição à modelagem preditiva.

---

## Categoria 15 — Gestão Orientada a Dados

**Consciência Situacional**
Capacidade de compreender o estado atual de um sistema, seus riscos, suas
variáveis em movimento e suas possíveis evoluções — de forma a permitir
resposta rápida e fundamentada. Precondição para a gestão por exceção e
para o monitoramento preditivo.
*Ver também: Sistema de Consciência Situacional (Cat. 17).*

**Gestão Orientada a Dados (Data-Driven Management)**
Modelo de gestão em que decisões são fundamentadas predominantemente em
evidências obtidas por meio de coleta, análise e interpretação de dados,
em substituição à intuição isolada ou à experiência não documentada.

**Maturidade Analítica**
Grau de capacidade institucional para utilizar dados na operação, gestão e
estratégia. Organizações com baixa maturidade analítica operam com dados
fragmentados e análises pontuais; organizações com alta maturidade analítica
integram dados em tempo real, automatizam análises e orientam decisões
estratégicas por modelos preditivos.

**Observabilidade Organizacional**
Capacidade institucional de compreender o comportamento de seus processos,
sistemas e entregas a partir dos dados gerados pelas próprias operações —
sem depender exclusivamente de auditorias externas ou relatos manuais.
No ecossistema, a observabilidade organizacional é construída pela combinação
de repositórios versionados, logs de execução, backlogs de decisão e
registros institucionais rastreáveis.

**Tomada de Decisão Baseada em Evidências**
Processo decisório fundamentado em dados, análises e conhecimento validado,
em contraposição a decisões baseadas exclusivamente em precedente, pressão
política ou percepção não verificada.

---

## Categoria 16 — Arquitetura de Dados

**Data Lake**
Repositório destinado ao armazenamento de grandes volumes de dados em formato
bruto, preservando a estrutura original das fontes para processamento e análise
posterior. Distinto do Data Warehouse pela ausência de transformação prévia
dos dados no momento da ingestão.

**Data Warehouse**
Repositório estruturado, integrado e orientado a assunto, destinado ao
armazenamento de dados tratados e consolidados para fins de análise e
tomada de decisão. Distinto do Data Lake pela ênfase na estruturação e
na qualidade dos dados para consulta analítica.

**Fonte de Dados**
Sistema, dispositivo, processo ou repositório responsável pela geração ou
custódia primária de dados. No ecossistema, fontes de dados incluem sistemas
assistenciais (prontuários, RNDS), sistemas administrativos (SEI, contratos)
e repositórios institucionais (GitHub, agendas).

**Integração**
Processo de intercâmbio estruturado de informações entre sistemas distintos,
garantindo que dados produzidos em uma fonte sejam disponibilizados,
compreendidos e utilizáveis em outro sistema receptor.
*Ver também: Interoperabilidade (Cat. 11) para definição normativa no
contexto de saúde digital.*

**Pipeline de Dados**
Fluxo automatizado responsável por coletar, transformar, validar e
disponibilizar dados de uma ou mais fontes para um destino de consumo
(análise, relatório, sistema receptor). No ecossistema, o conceito de
pipeline de dados é análogo ao pipeline de transcrição documental (Cat. 6)
— uma sequência estruturada de etapas com entradas, saídas e verificações
definidas.

---

## Categoria 17 — Conceitos Proprietários do Ecossistema

> Esta categoria reúne termos de autoria do ecossistema DTD/SETIS —
> conceitos que não seguem uma definição de mercado preexistente, mas
> constituem a identidade conceitual própria deste projeto. Devem ser
> tratados com atenção especial: qualquer alteração de definição aqui
> pode impactar documentos, skills e instrumentos que os referenciam.

**Ativo Informacional**
Qualquer documento, dado, modelo, indicador, regra de negócio ou
conhecimento institucional considerado relevante para a organização —
que possui valor, deve ser preservado, pode ser consultado e precisa
ser gerido ao longo do tempo. No ecossistema, ativos informacionais
incluem repositórios GitHub, registros de reunião, transcrições
normativas, IACs produzidos e backlogs de decisão.

**Conhecimento Estratégico**
Conhecimento utilizado para orientar decisões de gestão, planejamento
e governança institucional. Distinto do conhecimento operacional pela
sua orientação para o longo prazo e para a definição de direção —
não para a execução cotidiana. No ecossistema, o conhecimento estratégico
está concentrado nas Matrizes (tipo M) e nos instrumentos IAC e PoC.

**Conhecimento Operacional**
Conhecimento produzido pela execução cotidiana dos processos —
acumulado em logs de execução, registros de reunião, backlogs de decisão
e workflows documentados. Distinto do conhecimento estratégico pela
sua origem na prática e pela sua utilidade imediata para quem executa.

**Mapa Cognitivo Institucional**
Representação estruturada das relações entre documentos, indicadores,
processos, sistemas, projetos e decisões de uma organização — permitindo
que gestores e agentes compreendam como os elementos institucionais se
conectam e se influenciam mutuamente. No ecossistema, o mapa cognitivo
institucional é construído progressivamente pela combinação do sumário,
do glossário, da taxonomia de saúde digital e dos workflows documentados.

**Memória Institucional**
Conjunto estruturado de conhecimentos, decisões, experiências e documentos
acumulados ao longo do tempo por uma organização — preservado de forma
que possa ser consultado, auditado e reutilizado independentemente das
pessoas que os produziram. No ecossistema, a memória institucional é o
objetivo central dos repositórios tipo D, W e A, e do projeto P02
(`hub-memoria`).

**Radar Institucional**
Camada de monitoramento responsável por identificar continuamente riscos,
oportunidades, tendências e desvios relevantes no ambiente interno e
externo da organização — sintetizando sinais dispersos em alertas
acionáveis para a gestão. No ecossistema, o radar institucional é
operacionalizado parcialmente pela skill S07 (`skl-briefing-saude-digital`)
no eixo de monitoramento estratégico externo, com expansão prevista para
os demais eixos de monitoramento (Cat. 13).

**Sistema de Consciência Situacional**
Conjunto integrado de capacidades — dados, processos, skills e instrumentos
— destinado a permitir que gestores compreendam continuamente o estado atual
da organização: o que está acontecendo, o que está em risco, o que está
mudando e o que exige decisão. No ecossistema, o Sistema de Consciência
Situacional é o nome dado à arquitetura de monitoramento que o ecossistema
DTD/SETIS está construindo progressivamente.
*Ver também: Consciência Situacional (Cat. 15).*


---


### SEV1 — Severidade 1 (Crítica)
Nível mais alto da escala de severidade de divergências do ecossistema DTD/SETIS,
baseada no padrão ITIL/ISO 20000. Indica uma inconsistência que compromete a
integridade operacional do ecossistema ou impede a execução de operações críticas.
Requer correção imediata antes de qualquer outra ação. Exemplo: repositório âncora
inacessível, sumario.md corrompido.

### SEV2 — Severidade 2 (Alta)
Segundo nível da escala de severidade. Indica dados incorretos em arquivos de
referência central (sumario.md, CONTEXTO.md, README do hub-entrada) que produzem
divergência entre o estado declarado e o estado real do ecossistema. Requer
correção na mesma sessão em que foi identificado. Exemplo: versão incorreta de
repositório registrada no sumario.md.

### SEV3 — Severidade 3 (Médio)
Terceiro nível da escala de severidade. Indica inconsistências detectáveis por
auditoria — arquivos obrigatórios ausentes, campos incompletos, entradas de
backlog faltando. Não impede operação imediata mas compromete rastreabilidade
e conformidade estrutural. Deve ser corrigido na próxima sessão disponível.

### SEV4 — Severidade 4 (Baixo)
Nível mais baixo da escala de severidade. Indica oportunidades de melhoria ou
candidatos ao glossário identificados durante auditoria. Não compromete operação
nem rastreabilidade. Pode ser agendado para sessão futura ou aceito como estado
tolerado pelo mantenedor.

### Auditoria de Consistência (W05)
Processo independente de verificação do ecossistema DTD/SETIS, executado em
5 camadas (versões, arquivos obrigatórios, hub-entrada, backlogs, glossário),
que confronta o estado declarado nos arquivos de referência com o estado real
dos repositórios. Por princípio de design, é separado do executor (S04) —
nunca solicita token, nunca altera arquivos, nunca é executado pelo mesmo agente
no mesmo fluxo que vai corrigir as divergências encontradas. Sua única saída é
um relatório classificado por severidade SEV1–SEV4. Acionado obrigatoriamente
no início de toda sessão de trabalho e como pré-condição do W04.


### Commander's Intent (Intenção do Comandante)
Princípio de design originado na doutrina militar e adaptado ao ecossistema
DTD/SETIS. Cada skill e workflow deve declarar explicitamente seu estado final
desejado — o resultado que o processo existe para produzir. Quando uma situação
não coberta pelas instruções escritas surgir, a decisão correta é aquela que
mais se aproxima desse estado desejado. Garante que lacunas nos procedimentos
escritos tenham um árbitro principiado, não apenas um gap. Introduzido na S04
v2.4 e adotado como padrão universal do ecossistema. Também referenciado como
"Intenção do Comandante" em português.

### staging area
Camada de governança que separa ideias brutas de fatos operacionais no
ecossistema DTD/SETIS. Toda ideia emergente — independentemente do destino
final (ROADMAP, hub-aprendizagem, nova skill, novo workflow) — passa
obrigatoriamente pela staging antes de ser registrada como fato operacional.
Implementada no arquivo `staging.md` do hub-entrada, organizada em seções:
A (ideias em avaliação), B (decisões pendentes do mantenedor), C (ideias
brutas mineradas em sessão). Nenhuma ideia avança sem aprovação explícita
do mantenedor. Não há atalho que bypasse essa camada.

### wkf-sessao-agente (W06)
Workflow que governa o processo completo de uma sessão de trabalho assistida
por agente de IA no ecossistema DTD/SETIS. Processo pai do W03 (registro de
sessão) e do W05 (auditoria de consistência). Estruturado em três fases:
Abertura (leitura de contexto + Handoff da sessão anterior), Trabalho
(execução da missão via S04), e Fechamento (W03 + mineração de ideias +
auditoria W05 iterativa). Introduzido em 2026-06-06. Ver também: Handoff,
separação executor/auditor, staging area.

### hub-aprendizagem (D03)
Repositório documental de natureza reflexiva do ecossistema DTD/SETIS.
Registra boas práticas, benchmarks e lições aprendidas da construção do
ecossistema em formato de capítulos — destinado a preservar o conhecimento
acumulado de forma narrativa e explicativa. Classificado como Tipo D
(Documento) por decisão do mantenedor em 2026-06-06, com anotação de
natureza reflexiva: documenta o próprio ecossistema, não o ambiente externo.

### mat-cadastro-ses-setis-dtd (D02)
Repositório do tipo Documento (D) que contém a Matriz de Cadastros de
referência validada para uso interno da DTD/SETIS/SES-DF. Consolida os
cadastros institucionais relevantes para as operações da Diretoria de
Transformação Digital.

### engenharia reversa (no contexto do ecossistema)
Técnica aplicada em sessão de 2026-06-05 para mapear retrospectivamente
os erros e falhas estruturais acumuladas no ecossistema DTD/SETIS desde
sua fundação. Resultou na identificação de 13 pontos de falha e 4 GAPs
estruturais, que orientaram a criação do W05 e a evolução da S04 para
versões v2.5 e v2.6. No contexto do ecossistema, refere-se à análise
sistemática de causas raiz a partir de artefatos existentes, sem acesso
aos registros originais de decisão.

### separação executor/auditor
Princípio de design do ecossistema DTD/SETIS que estabelece que o agente
que executa uma operação não deve auditar o próprio trabalho. Fundamentado
na observação empírica de que agentes de IA operam com viés de confirmação
estrutural — ao auditar o próprio trabalho no mesmo contexto em que o
executaram, tendem a não detectar erros introduzidos pela própria operação.
Implementado operacionalmente pelo W05, que é sempre executado em chat
separado, com contexto limpo, por instância independente do agente. Demonstrado
empiricamente em 2026-06-06: auditoria independente encontrou 3 erros
introduzidos pela operação de correção anterior, invisíveis para o executor.

### Handoff
Protocolo de passagem de bastão entre sessões de trabalho no ecossistema
DTD/SETIS. O relatório W05 zerado do fechamento de uma sessão é a
pré-condição de abertura da sessão seguinte — garantindo que cada sessão
começa sabendo exatamente o estado que herdou. Conceito originado em
sistemas distribuídos e orquestração de agentes, em amadurecimento no
ecossistema como padrão para articulação entre múltiplos workflows, chats
e agentes. O termo "passagem de bastão" é usado como equivalente coloquial
em português. Formalizado no W06 (wkf-sessao-agente) em 2026-06-06.


### wkf-auditoria-consistencia (W05)
Workflow de Auditoria de Consistência do Ecossistema DTD/SETIS. Processo
independente da S04 que verifica sistematicamente se o estado declarado
do ecossistema corresponde ao estado real — percorrendo o grafo completo
de dependências em 5 camadas (versões, arquivos obrigatórios, hub-entrada,
backlogs, glossário) e classificando cada divergência por severidade
SEV1–SEV4. Por princípio de design, nunca solicita token, nunca altera
repositórios e nunca é executado pelo mesmo agente no mesmo fluxo que
vai corrigir as divergências encontradas (ver: separação executor/auditor).
Subprocesso filho do W06. Acionado obrigatoriamente no fechamento de toda
sessão W06 em chat separado com contexto limpo. Introduzido em 2026-06-05.

## Índice Alfabético Unificado

> Lista de todos os termos definidos neste glossário, com referência à categoria.
> Atualizado a cada versão.

| Termo | Categoria |
|---|---|
| Agenda (tipo A) | Cat. 8 |
| Analytics | Cat. 14 |
| Análise Descritiva | Cat. 14 |
| Análise Diagnóstica | Cat. 14 |
| Análise Preditiva | Cat. 14 |
| Análise Prescritiva | Cat. 14 |
| Anonimização | Cat. 10 |
| Artefato de extração | Cat. 6 |
| Ativo Informacional | Cat. 17 |
| Auditabilidade de IA | Cat. 11 |
| Auditoria de glossário | Cat. 5 |
| backlog-versoes.md | Cat. 2 |
| Breaking / Non-breaking | Cat. 4 |
| Business Intelligence (BI) | Cat. 14 |
| CHANGELOG.md | Cat. 2 |
| Cibersegurança | Cat. 10 |
| Conhecimento Estratégico | Cat. 17 |
| Conhecimento Operacional | Cat. 17 |
| Consciência Situacional | Cat. 15 |
| CONTEXTO.md | Cat. 2 |
| Dado Pessoal | Cat. 10 |
| Dado Pessoal Sensível | Cat. 10 |
| data_registro | Cat. 8 |
| data_reuniao | Cat. 8 |
| Data Lake | Cat. 16 |
| Data Warehouse | Cat. 16 |
| Documento (tipo D) | Cat. 1 |
| Drift documental | Cat. 5 |
| Encarregado (DPO) | Cat. 10 |
| Estado final esperado | Cat. 7 |
| EXECUCOES.md | Cat. 7 |
| Falso positivo | Cat. 5 |
| Fonte de Dados | Cat. 16 |
| Front Matter YAML | Cat. 6 |
| Gestão por Exceção | Cat. 13 |
| Gestão Orientada a Dados (Data-Driven Management) | Cat. 15 |
| GLOSSARIO.md | Cat. 2 |
| Governança em Saúde Digital | Cat. 12 |
| IAC — Instrumento de Análise Comparativa | Cat. 3 |
| Índice cronológico | Cat. 8 |
| Índice Nacional de Maturidade em Saúde Digital (INMSD) | Cat. 12 |
| INDICE.md | Cat. 2 |
| Integração | Cat. 16 |
| Inteligência Artificial Generativa (IA Generativa) | Cat. 11 |
| Interoperabilidade | Cat. 11 |
| Log de execução | Cat. 7 |
| MAJOR / MINOR (versionamento) | Cat. 4 |
| Mapa Cognitivo Institucional | Cat. 17 |
| Matriz (tipo M) | Cat. 1 |
| Maturidade Analítica | Cat. 15 |
| Memória Institucional | Cat. 17 |
| Modelo de Linguagem de Larga Escala (LLM) | Cat. 11 |
| Monitoramento de Conformidade | Cat. 13 |
| Monitoramento de Desempenho | Cat. 13 |
| Monitoramento de Qualidade | Cat. 13 |
| Monitoramento de Segurança | Cat. 13 |
| Monitoramento de Tendências | Cat. 13 |
| Monitoramento Estratégico | Cat. 13 |
| Monitoramento Operacional | Cat. 13 |
| nomenclatura.md | Cat. 2 |
| Observabilidade Organizacional | Cat. 15 |
| OP-A, OP-B, OP-C, OP-D, OP-E, OP-F, OP-P | Cat. 4 |
| Pipeline de Dados | Cat. 16 |
| Pipeline de transcrição | Cat. 6 |
| PLAUD NOTE Pro | Cat. 8 |
| PoC — Prova de Conceito | Cat. 3 |
| Porta de entrada | Cat. 5 |
| Projeto (tipo P) | Cat. 1 |
| Prontuário Médico / Registro Eletrônico de Saúde (RES) | Cat. 12 |
| Pseudonimização | Cat. 10 |
| Radar Institucional | Cat. 17 |
| Reflow | Cat. 6 |
| Registro institucional de reunião | Cat. 8 |
| Repositório âncora | Cat. 5 |
| Saúde Digital | Cat. 12 |
| Sistema de Consciência Situacional | Cat. 17 |
| Sistema de Inteligência Artificial (Sistema de IA) | Cat. 11 |
| Skill (tipo S) | Cat. 1 |
| Software como Dispositivo Médico (SaMD) | Cat. 11 |
| Subprocesso | Cat. 7 |
| sumario.md | Cat. 2 |
| Telecirurgia | Cat. 9 |
| Teleconsulta | Cat. 9 |
| Teleconsultoria | Cat. 9 |
| Telediagnóstico | Cat. 9 |
| Telemonitoramento ou Televigilância | Cat. 9 |
| Teleinterconsulta | Cat. 9 |
| Telemedicina | Cat. 9 |
| Telessaúde | Cat. 9 |
| Teletriagem | Cat. 9 |
| Termo candidato | Cat. 5 |
| Tomada de Decisão Baseada em Evidências | Cat. 15 |
| Tratamento de Dados | Cat. 10 |
| Workflow | Cat. 7 |



*Última revisão: 2026-06-04 — victorarimatea*
*Para propor novos termos: abrir issue ou atualizar diretamente via S04.*

- **Commander's Intent / Intenção do Comandante** → Categoria 17
- **D02 / mat-cadastro-ses-setis-dtd** → Categoria 17
- **D03 / hub-aprendizagem** → Categoria 17
- **engenharia reversa** → Categoria 17
- **Handoff** → Categoria 17
- **SEV1 / SEV2 / SEV3 / SEV4** → Categoria 17
- **separação executor/auditor** → Categoria 17
- **staging area** → Categoria 17
- **W05 / wkf-auditoria-consistencia** → Categoria 17
- **W06 / wkf-sessao-agente** → Categoria 17
- **Workflow (tipo W)** → Categoria 1

