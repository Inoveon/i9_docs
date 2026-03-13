# Agent Manager — Memória Operacional

## Histórico

| Data | Evento |
|------|--------|
| 2026-03-13 | Agente criado via /criar-agente |

## Agentes do Projeto

| Agente | Tipo | Descrição |
|--------|------|-----------|
| `agent-manager` | Transversal | Gerencia estrutura de agentes |
| `project-organizer` | Transversal | Organiza estrutura de pastas do projeto (exceto `.claude/`) |
| `doc-designer` | Documentação HTML | Design profissional de apresentações, relatórios e documentos HTML i9ON |

## Arquitetura Identificada

Projeto i9_docs — repositório de documentação corporativa:
- `apresentacoes/` — Apresentações HTML (investimento, novo ciclo)
- `relatorios/` — Relatórios de auditoria
- `documentacao/` — Documentação técnica do ecossistema
- `propostas/` — Propostas comerciais
- `agents/` — Catálogo de 21 agents documentados (raiz, não .claude/)
- `templates/` — Templates HTML base
- `assets/` — Logos e estilos compartilhados

## Padrões Confirmados

- Stack: HTML5, CSS3, JS ES6+, Material Design Icons, Google Fonts (Inter)
- Agentes Claude Code ficam em `.claude/agents/`
- Documentação de agents (catálogo) fica em `agents/` na raiz

## Decisões de Design

{Preencher conforme decisões são tomadas}

## Antipadrões Identificados

{Preencher conforme erros recorrentes são identificados}

## Próximas Melhorias

- [x] Criar agente `doc-designer` para documentos HTML (criado em 2026-03-13)
- [ ] Criar agentes especializados adicionais (doc-slides, doc-report, etc.)
- [ ] Mapear templates existentes e vincular a agentes
