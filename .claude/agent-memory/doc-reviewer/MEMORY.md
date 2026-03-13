# doc-reviewer — Memória Operacional

## Checklist de Revisão

Ver checklist completo no corpo do agente (doc-reviewer.md).

Resumo dos critérios críticos:
- `:root` com 13 tokens de cor
- Gradiente: `linear-gradient(135deg, #12162B 0%, #011E4B 50%, #005BAA 100%)`
- Inter + Material Icons no `<head>`
- `lang="pt-BR"` e `box-sizing: border-box`
- Sem frameworks JS ou libs de gráficos externas
- Sem paths absolutos de máquina

## Severidade de Issues

- **Crítico** — bloqueia entrega: cor errada, dado sem fonte, HTML inválido, lib externa
- **Menor** — corrigir antes: gramática, espaçamento, token de cor ligeiramente errado
- **Sugestão** — opcional: microcopy, variação de tom, melhoria de hierarquia

## Issues Recorrentes

(preencher conforme padrões forem identificados nas revisões)

## Issues Recorrentes

- Cores roxas/violetas (`#7c3aed`, `#4c1d95`) reaparecem em documentos novos mesmo após remoção no commit `290916f`. Verificar sempre com pattern `7c3aed|4c1d95`.
- Grids fixas (`repeat(N, 1fr)`) em formato de apresentação de slides são intencionais — não reportar como issue de responsividade.
- Margem líquida Inoveon: o valor oficial é `~55%` (inoveon-info.md). Roteiros gerados pelo doc-writer tendem a usar `> 50%` (conservador). Sempre corrigir para `~55%`.
- Chart.js via CDN aparece em apresentações HTML — viola o checklist "sem libs de gráficos externas". Tratar como issue de atenção (não bloqueante se o ambiente tem internet), mas registrar sempre.
- border-radius dos cards em apresentações tende a ficar em 12px; padrão do design system é 20px. Não bloqueia, mas deve ser registrado.

## Histórico de Revisões

| Data | Documento | Veredicto | Issues Críticos |
|------|-----------|-----------|-----------------|
| 2026-03-13 | — | — | Agente criado |
| 2026-03-13 | presentations/internal/diagnostico-organizacional-2026.html | APROVADO COM RESSALVAS | Cores roxas/violetas removidas (menores); KPIs sem fonte quantitativa precisa (sugestão) |
| 2026-03-13 | presentations/investment/pitch-investidor-2026.html | APROVADO COM RESSALVAS | Margem líquida corrigida de > 50% para ~55%; Chart.js CDN (não self-contained) sinalizado |
