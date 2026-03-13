# Project Organizer — Memória Operacional

## Histórico

| Data | Evento |
|------|--------|
| 2026-03-13 | Agente criado via /criar-agente |
| 2026-03-13 | Pastas principais renomeadas para inglês; temp-icons-preview.html removido |

## Estrutura Atual

```
i9_docs/
├── presentations/           ← Apresentações HTML
│   ├── new-cycle/
│   ├── investment/
│   └── commercial-deck-pdv/
├── reports/                 ← Relatórios de auditoria
│   └── audit/
├── docs/                    ← Docs técnicas
│   ├── ecosystem/
│   └── prompts/
├── proposals/               ← Propostas comerciais
│   └── i9on/
├── templates/               ← Templates HTML base
├── assets/                  ← Logos, ícones, estilos
├── design-system/           ← Design system
├── scripts/                 ← Scripts auxiliares
└── agents/                  ← Catálogo de agents (raiz)
```

## Padrões Confirmados

- Nomes de arquivo e pasta: kebab-case, sem acentos, sem espaços, sem maiúsculas
- Idioma das pastas: inglês (migrado em 2026-03-13)
- Nomes de produto (ex: i9on) mantidos como estão, sem tradução
- Formato principal: HTML5 com CSS3, Material Design Icons, Google Fonts (Inter)
- `.claude/` é escopo exclusivo do `agent-manager` — nunca atuar aqui

## Decisões de Design

{Preencher conforme decisões são tomadas}

## Antipadrões Identificados

{Preencher conforme erros recorrentes são identificados}

## Próximas Melhorias

- [ ] Mapear subpastas detalhadas de cada diretório principal
- [ ] Documentar convencoes de datas nos nomes de arquivo
