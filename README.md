# ecossistema-sumario

**Tipo:** Matriz Central (M)
**Versão:** v0.10 — 2026-05-29
**Mantenedor:** victorarimatea
**Status:** Ativo

> Este é o repositório âncora do ecossistema DTD/SETIS.
> Toda skill do ecossistema consulta este repositório primeiro.
> Nenhuma skill, documento ou matriz pode ser criado sem registro aqui.

## Arquivos deste repositório

| Arquivo | Função |
|---|---|
| `CONTEXTO.md` | Briefing completo do ecossistema — leia primeiro em novas sessões |
| `sumario.md` | Índice vivo de todos os repositórios do ecossistema |
| `nomenclatura.md` | Regras de nomes, versões, estrutura de arquivos e modelo IAC |
| `backlog-versoes.md` | Histórico auditável de todas as alterações neste repositório |
| `protocolo-atualizacoes.md` | Protocolo obrigatório de encerramento de operações |
| `backlog-acoes-dtd.md` | Histórico retrospectivo de ações e produtos da DTD |

## Como iniciar uma nova sessão de trabalho

Cole no início de qualquer conversa com o Claude:

```
Leia https://raw.githubusercontent.com/victorarimatea/ecossistema-sumario/main/CONTEXTO.md
e me diga o que entendeu sobre o ecossistema antes de começarmos.
```

## Como este repositório é usado

As skills do ecossistema acessam `sumario.md` para saber quais
repositórios existem, seus endereços e sua função antes de executar
qualquer tarefa. Alterações neste repositório requerem autorização
explícita do mantenedor e devem ser registradas em `backlog-versoes.md`.
