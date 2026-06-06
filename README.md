# hub-fonte

**Tipo:** Matriz Central (M01)
**Versão:** v0.25 — 2026-06-06
**Mantenedor:** victorarimatea
**Status:** Ativo

> Este é o repositório âncora do ecossistema DTD/SETIS.
> Toda skill do ecossistema consulta este repositório primeiro.
> Nenhuma skill, documento ou matriz pode ser criado sem registro aqui.

## Arquivos deste repositório

| Arquivo | Função |
|---|---|
| `ONBOARDING.md` | Porta de entrada para agentes e colaboradores externos — roteamento por propósito |
| `CONTEXTO.md` | Briefing completo do ecossistema — leia primeiro em novas sessões |
| `sumario.md` | Índice vivo de todos os repositórios do ecossistema |
| `nomenclatura.md` | Regras de nomes, versões, estrutura de arquivos e modelo IAC |
| `GLOSSARIO.md` | Definições formais de todos os termos do ecossistema |
| `backlog-versoes.md` | Histórico auditável de todas as alterações neste repositório |
| `protocolo-atualizacoes.md` | ~~Protocolo de operações~~ DESCONTINUADO — substituído pela S04 |
| `backlog-acoes-dtd.md` | Histórico retrospectivo de ações e produtos da DTD |

## Como iniciar uma nova sessão de trabalho

Cole no início de qualquer conversa com o Claude:

```
Leia https://raw.githubusercontent.com/victorarimatea/hub-fonte/main/CONTEXTO.md
e me diga o que entendeu sobre o ecossistema antes de começarmos.
```

## Como este repositório é usado

As skills do ecossistema acessam `sumario.md` para saber quais
repositórios existem, seus endereços e sua função antes de executar
qualquer tarefa. Alterações neste repositório requerem autorização
explícita do mantenedor e devem ser registradas em `backlog-versoes.md`.

---

## Navegação rápida

→ **[INDICE.md](./INDICE.md)** — mapa completo de todos os arquivos deste repositório
