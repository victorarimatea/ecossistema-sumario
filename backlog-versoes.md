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
