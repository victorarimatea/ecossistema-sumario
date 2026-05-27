# CONTEXTO.md — Ecossistema DTD/SETIS

**Versão:** v1.0 — 2026-05-27
**Mantenedor:** victorarimatea
**Propósito:** Briefing completo para inicialização de novas sessões de trabalho.
Leia este arquivo antes de qualquer outra ação.

---

## Quem é o mantenedor

**Victor Leonardo Arimatea Queiroz**
Diretor de Transformação Digital — Diretoria de Transformação Digital (DTD)
Secretaria Executiva de Tecnologia da Informação em Saúde (SETIS)
Secretaria de Estado de Saúde do Distrito Federal (SES-DF)
Matrícula: 1657757-4

A DTD foi criada há 6 meses. Victor é o único servidor da unidade no momento —
toda a construção deste ecossistema é trabalho individual, desenvolvido em
paralelo com projetos institucionais de alta complexidade.

---

## O que é este ecossistema

Um sistema de automação e governança documental construído do zero, combinando:
- Repositórios GitHub como memória institucional permanente
- Skills do Claude como agentes de automação especializados
- Matrizes de conhecimento como fontes de verdade compartilhadas
- Instrumentos padronizados (IAC) como produtos de governança

O objetivo de longo prazo é que uma única instrução possa acionar múltiplas
skills, consultar vários repositórios, produzir documentos institucionais
completos e registrar tudo em backlogs auditáveis — com mínima intervenção
manual do mantenedor.

---

## Estrutura atual do ecossistema (maio/2026)

### Repositórios ativos

| ID | Tipo | Nome | Versão | Descrição |
|---|---|---|---|---|
| M01 | Matriz | ecossistema-sumario | v0.5 | Âncora do ecossistema: sumário, nomenclatura, contexto |
| M02 | Matriz | saude-digital-taxonomia | v1.0 | Taxonomia estruturada de saúde digital |
| S01 | Skill | skill-criador-de-skills | v1.0 | Cria novos repositórios de skill via API GitHub |
| S02 | Skill | skill-iac-pdtic | v2.0 | Gera IAC-V e IAC-H do PDTIC da SES-DF |

### Repositórios planejados (não criados ainda)

| Tipo | Nome sugerido | Propósito |
|---|---|---|
| D | governanca-ses-df | Matrizes normativas: Portaria 193/2024, PTD-SES, base normativa de saúde digital |
| D | pdtic-historico | Histórico de versões do PDTIC com IACs gerados |
| S | skill-iac-generico | IAC para qualquer par de documentos (versão sem especialização temática) |

---

## Convenções do ecossistema

### Nomenclatura de repositórios
`[dominio]-[especificidade]` em kebab-case minúsculo.
O tipo (M/S/D) não entra no nome — fica registrado no sumário.

### Versionamento
`vMAJOR.MINOR — AAAA-MM-DD`
MAJOR sobe em mudanças incompatíveis com versões anteriores.
MINOR sobe em melhorias e correções.

### Arquivos obrigatórios em todo repositório
`README.md`, `backlog-versoes.md`
Skills (tipo S) adicionam: `SKILL.md`
Matrizes M01 adicionam: `sumario.md`, `nomenclatura.md`, `CONTEXTO.md`

### Backlogs
Entrada mais recente sempre no topo.
Campos obrigatórios: Tipo de alteração, Autorizado por, Exposição de motivos.
Matrizes de conhecimento usam campos adicionais: Tópico afetado, Fonte, Proposto por.

---

## O modelo IAC — Instrumento de Análise Comparativa

Padrão de governança documental criado pela DTD/SETIS. Versão atual: **v0.2**.

### Dois modos

**IAC-V (Vertical):** compara versões do mesmo documento.
Pergunta central: *O que mudou?*
Exemplo: PDTIC v1.5 → v1.8

**IAC-H (Horizontal):** verifica conformidade entre documentos distintos.
Pergunta central: *Estão alinhados?*
Exemplo: PDTIC v1.8 × PTD-SES 2024-2027 — índice de alinhamento: 69%

### Estrutura obrigatória (ambos os modos)
Capa com ficha técnica → Sumário → Apresentação → Contexto normativo →
Análise (modificações ou convergências/lacunas) → Encaminhamentos/Recomendações →
Modelo IAC para uso futuro

### Regras críticas de linguagem institucional
- O **SGTD** revisa, manifesta, recomenda e encaminha. NUNCA delibera.
- **Deliberação** sobre planos compete ao **Fórum de Subsecretários** (Art. 7º, I — Portaria 193/2024).
- Documentos institucionais registram **constatações técnicas**, nunca a origem de manifestações.

---

## Estrutura de governança da SES-DF relevante para o ecossistema

### Portaria nº 193/2024 — CIG/SES
- **CIG/SES:** colegiado consultivo do Secretário de Estado
- **Fórum de Subsecretários:** delibera sobre planos e programas (Art. 7º, I)
  — instância que **aprova formalmente** o PDTIC
- **SGTD** (Subcomitê VI): revisa PDTIC e PTD, encaminha ao Fórum (Art. 34, VIII)
  — Victor é presidente do SGTD como Diretor de Transformação Digital

### Instrumentos de planejamento
- **PDTIC 2024-2027:** plano de TIC da SES-DF. Versão vigente: v1.5. Versão proposta: v1.8 (aguarda Fórum)
  - Aprovação: Fórum de Subsecretários (via SGTD) → portal da SES-DF
- **PTD-SES 2024-2027:** plano de transformação digital com impacto assistencial
  - Aprovação: CGTD/SEEC (nível GDF — Portaria 718/2024)
- Processo SEI de referência: 00060-00227811/2026-80

### Datas importantes (contexto maio/2026)
- 11/06/2026: reunião ordinária do SGTD (pauta: revisão do PDTIC v1.8)
- 17/06/2026: reunião do Fórum de Subsecretários (pauta: aprovação formal do PDTIC v1.8)

---

## O que já foi produzido (maio/2026)

### Documentos IAC gerados neste projeto

| Documento | Modo | Versão | Status |
|---|---|---|---|
| IAC Análise de Revisão do PDTIC 2024-2027 | IAC-V | v0.2 | Distribuído ao SGTD |
| IAC Análise de Conformidade PDTIC × PTD-SES | IAC-H | v0.1 | Produzido, aguarda distribuição |

### Lições aprendidas incorporadas às skills
- Acentuação completa em português requer duas rodadas de substituição no pipeline Node.js/DOCX
- Títulos de seções precisam de correção individual além da substituição global
- Verificação automática do DOCX gerado é obrigatória antes de entregar

---

## Próximos passos planejados

1. **Criar repositório `governanca-ses-df`** com Portaria 193/2024, PTD-SES,
   base normativa de saúde digital e matriz de competências institucionais
2. **Atualizar `skill-iac-pdtic`** para consultar `governanca-ses-df` na Etapa 1
3. **Criar repositório `pdtic-historico`** para registrar versões aprovadas do PDTIC
   com os IACs correspondentes
4. **Criar `skill-iac-generico`** — versão sem especialização temática do IAC
5. **Configurar o ecossistema como Projeto no Claude** carregando os SKILL.md
   para ativação permanente das skills

---

## Como iniciar uma nova sessão de trabalho

Cole no início da conversa:

```
Leia https://raw.githubusercontent.com/victorarimatea/ecossistema-sumario/main/CONTEXTO.md
e me diga o que entendeu sobre o ecossistema antes de começarmos.
```

O Claude vai absorver todo o contexto e você continua de onde parou.

---

## Tecnologias e acessos relevantes

- **GitHub:** github.com/victorarimatea (repositórios públicos: ecossistema-sumario, saude-digital-taxonomia, skill-criador-de-skills; privados: skill-iac-pdtic)
- **API GitHub:** Personal Access Token com permissão `repo` — gerado sob demanda, revogar após uso
- **Claude:** claude.ai — projeto "Ecossistema DTD/SETIS" com arquivos do PDTIC carregados
- **Documentos no projeto Claude:** PDTIC v1.5, PDTIC v1.8, Decreto 48.503/2026, Processo SEI 00060-00227811/2026-80, Portaria 193/2024, Portaria 718/2024, PTD-SES 2024-2027
