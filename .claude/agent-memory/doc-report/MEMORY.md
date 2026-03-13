# doc-report — Memória Operacional

## Guia Rápido de Gráficos

| Dado | Gráfico | Implementação via doc-designer |
|------|---------|-------------------------------|
| Evolução temporal | Linha / Área SVG | sparkline com gradiente |
| Comparação categorias | Barras verticais SVG | rect com rx arredondado |
| Proporção | Pizza / Donut SVG | stroke-dasharray (circ. 502.6) |
| Ranking | Barras horizontais HTML | progress-bar com gradiente 90deg |
| Valor único | KPI Card | gradiente i9-blue→navy |

## Hierarquia dos 3 Níveis

1. KPI Cards (5 seg) — status imediato
2. Gráficos (30 seg) — tendências e movimentos
3. Tabelas (aprofundamento) — dados granulares

## Estruturas Padrão

- **Relatório Executivo Mensal**: Header → KPIs → Destaques → Atenção → Análise → Comparativo → Próximos Passos
- **Dashboard Operacional**: Header → KPIs → Gráfico Principal → Grid Secundário → Tabela

## Regras

- Máximo 6 KPI cards em destaque
- Sempre comparar com período anterior ou meta
- Placeholder de dados: `[DADO]`

## Relatórios Criados

| Data | Nome | Tipo | Período | Localização |
|------|------|------|---------|-------------|
| 2026-03-13 | — | — | — | Agente criado |
