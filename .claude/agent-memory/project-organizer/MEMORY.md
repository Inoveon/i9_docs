# Project Organizer — Memória Operacional

## Histórico

| Data | Evento |
|------|--------|
| 2026-03-13 | Agente criado via /criar-agente |

## Estrutura Identificada

```
i9_docs/
├── apresentacoes/   ← Apresentações HTML
├── relatorios/      ← Relatórios de auditoria
├── documentacao/    ← Docs técnicas
├── propostas/       ← Propostas comerciais
├── templates/       ← Templates HTML base
├── assets/          ← Logos, ícones, estilos
├── scripts/         ← Scripts auxiliares
└── agents/          ← Catálogo de agents (raiz)
```

## Padrões Confirmados

- Nomes de arquivo: kebab-case, sem acentos, sem espaços, sem maiúsculas
- Formato principal: HTML5 com CSS3, Material Design Icons, Google Fonts (Inter)
- `.claude/` é escopo exclusivo do `agent-manager` — nunca atuar aqui

## Candidatos a Limpeza Identificados

- `temp-icons-preview.html` — arquivo temporário na raiz (verificar antes de remover)

## Decisões de Design

{Preencher conforme decisões são tomadas}

## Antipadrões Identificados

{Preencher conforme erros recorrentes são identificados}

## Próximas Melhorias

- [ ] Mapear subpastas detalhadas de cada diretório principal
- [ ] Documentar convencoes de datas nos nomes de arquivo
