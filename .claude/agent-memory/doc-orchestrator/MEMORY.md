# DOC-ORCHESTRATOR — Memória Operacional

## Histórico

| Data | Evento |
|------|--------|
| 2026-03-13 | Agente criado via /criar-agente |

## Propósito

Orquestrador central do fluxo de produção de documentos Inoveon.
Recebe demandas, interpreta tipo e delega para os agentes corretos em sequência.

## Fluxo Confirmado

```
demanda → doc-writer → [doc-slides|doc-proposal|doc-report] → doc-designer → doc-reviewer → project-organizer
```

## Fonte de Verdade da Empresa

Sempre consultar `.claude/shared/inoveon-info.md` antes de qualquer delegação.
Nunca inventar dados da empresa.

## Padrões Confirmados

- Sempre usar "Inoveon" — nunca "i9ON"
- Nunca pular o doc-reviewer
- Usar AskUserQuestion para dados faltantes

## Próximas Melhorias

- [ ] Documentar padrões de briefing validados em produção
- [ ] Registrar tipos de demanda mais frequentes
