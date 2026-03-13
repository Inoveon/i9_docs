# Agentes Claude Code — i9_docs

Agentes especialistas para o repositório de documentação corporativa Inoveon.

## Mapa de Agentes

```
agent-manager              ← gerencia estrutura de agentes (.claude/)
project-organizer          ← organiza estrutura de pastas do projeto

Orquestração:
  doc-orchestrator         ← recebe demandas e delega para os agentes corretos

Produção de Documentos:
  doc-writer               ← conteúdo: copy, narrativa, estrutura textual
  doc-slides               ← apresentações: narrativa e estrutura de slides
  doc-proposal             ← propostas comerciais: escopo, ROI, investimento
  doc-report               ← relatórios e dashboards: KPIs, gráficos, análise
  doc-designer             ← design: HTML, SVG, layout, design system Inoveon
  doc-reviewer             ← qualidade: revisão final antes da entrega
```

## Fluxo de Produção

```
Briefing
   ↓
doc-writer        → define conteúdo e narrativa
   ↓ (se apresentação)    ↓ (se proposta)    ↓ (se relatório)
doc-slides         doc-proposal          doc-report
   ↓                    ↓                     ↓
doc-designer      → implementa HTML + SVG (design system Inoveon)
   ↓
doc-reviewer      → revisa qualidade e consistência
   ↓
project-organizer → salva no lugar certo
```

## Descrição dos Agentes

| Agente | Tipo | Escopo |
|--------|------|--------|
| `agent-manager` | Transversal | Cria, renomeia e organiza agentes em `.claude/agents/` e `.claude/agent-memory/` |
| `project-organizer` | Transversal | Organiza estrutura de pastas: `apresentacoes/`, `relatorios/`, `documentacao/`, `propostas/`, `templates/`, `assets/` |
| `doc-orchestrator` | Orquestrador | Recebe demandas do usuário, interpreta o tipo e delega para os agentes na sequência correta |
| `doc-writer` | Conteúdo | Escreve copy, narrativas e estruturas textuais para todos os tipos de documento |
| `doc-slides` | Apresentações | Estrutura narrativa e sequência lógica de slides para pitch decks, decks comerciais e executivos |
| `doc-proposal` | Propostas | Proposta comercial completa: escopo, entregáveis, cronograma, tabela de investimento, ROI, termos |
| `doc-report` | Relatórios | Relatórios e dashboards: escolha de KPIs, tipo de gráfico, hierarquia de informação |
| `doc-designer` | Design HTML | Implementa HTML + SVG com design system Inoveon. Gráficos SVG puros, zero dependências externas |
| `doc-reviewer` | Qualidade | Gate final: revisa design system, conteúdo, gramática, marca e conformidade antes da entrega |

## Como Usar

```
@doc-orchestrator  criar apresentação para investidores   ← ponto de entrada recomendado
@doc-orchestrator  fazer proposta para cliente X
@doc-orchestrator  gerar relatório de KPIs do mês

@doc-writer     escrever conteúdo para apresentação sobre produto X
@doc-slides     estruturar pitch deck para investidores
@doc-proposal   criar proposta comercial para cliente Y
@doc-report     criar dashboard de KPIs do mês
@doc-designer   implementar o HTML da apresentação
@doc-reviewer   revisar o documento antes de entregar
@agent-manager  criar novo agente especialista
```

## Como Criar Novo Agente

Use a skill `/criar-agente` ou peça ao `@agent-manager`.
Padrão de nomenclatura: `doc-{função}` para documentação, nome direto para transversais.
