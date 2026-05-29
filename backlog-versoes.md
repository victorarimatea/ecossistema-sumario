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
