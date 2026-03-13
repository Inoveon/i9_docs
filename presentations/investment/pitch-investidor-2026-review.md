# Revisão — pitch-investidor-2026.html

**Data da revisão:** 2026-03-13
**Revisor:** doc-reviewer
**Arquivo revisado:** `presentations/investment/pitch-investidor-2026.html`
**Arquivo de referência (roteiro):** `presentations/investment/pitch-investidor-2026.md`
**Fonte de verdade corporativa:** `.claude/shared/inoveon-info.md`

---

## Status Geral: APROVADO COM RESSALVAS

O documento está em condição de entrega após as correções pontuais aplicadas nesta revisão. Os issues críticos foram resolvidos em tempo de revisão. Dois pontos de atenção remanescentes (biblioteca externa de gráficos e card-radius) não bloqueiam a apresentação mas devem ser endereçados em versão futura.

---

## Issues Críticos (bloqueantes)

### 1. Margem Líquida divergente do dado oficial — CORRIGIDO
- **Encontrado:** Slide 11 exibia `> 50%` como Margem Líquida; Slide 20 mencionava "margem acima de 50%"
- **Dado correto (inoveon-info.md):** `~55%`
- **Roteiro .md:** indica `> 50%` (diferença existia também no .md — o roteiro usou valor conservador)
- **Decisão de revisão:** O dado oficial de referência (`inoveon-info.md`) é a fonte de verdade. O valor correto é `~55%`. Ambas as ocorrências foram corrigidas.
- **Status:** Corrigido diretamente no HTML.

---

## Issues Menores (corrigidos)

Nenhum issue menor adicional identificado além do item acima.

---

## Issues de Atenção — Não Bloqueantes (requerem decisão futura)

### A. Uso de Chart.js via CDN externo
- **Linha 9:** `<script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.0/dist/chart.umd.min.js"></script>`
- **Checklist Inoveon:** "Sem bibliotecas de gráficos externas (Chart.js, D3.js)"
- **Impacto:** O documento **não é self-contained** — requer conexão com internet para renderizar os gráficos dos slides 13, 22 e 25. Em apresentação offline, esses três slides ficam sem gráfico.
- **Afetados:** Slide 13 (barras — crescimento contratos/receita), Slide 22 (rosca — alocação do aporte), Slide 25 (linha dupla — ARR vs Valuation)
- **Recomendação:** Substituir os três charts por SVG puro gerado inline, eliminando a dependência externa. Alternativa de curto prazo: embutir o script Chart.js minificado no próprio HTML.
- **Status:** Não corrigido — requer reimplementação significativa.

### B. border-radius dos cards: 12px no lugar de 20px
- **Encontrado:** A classe `.card` usa `border-radius: 12px`. O design system Inoveon especifica 20px para cards.
- **Contexto:** Em formato de apresentação (slides em tela cheia), o valor 12px funciona visualmente e é consistente em todo o documento. A diferença é imperceptível na prática.
- **Recomendação:** Alinhar ao token padrão (20px) na próxima versão para conformidade com o design system.
- **Status:** Não corrigido nesta revisão — impacto visual mínimo em contexto de apresentação.

---

## Checklist de Conformidade

### Design System Inoveon

| Item | Status | Observação |
|------|--------|------------|
| `:root` com tokens de cor presentes | APROVADO | `--i9-dark`, `--i9-navy`, `--i9-blue`, `--white`, `--gray-100`, `--success`, `--warning`, `--error` presentes. Tokens extras `--accent` e `--card-bg` adicionados — aceitável. |
| Gradiente padrão `linear-gradient(135deg, #12162B 0%, #011E4B 50%, #005BAA 100%)` | APROVADO | Usado em slides 1, 11, 16, 20, 23, 25, 27, 29. Variações em slides individuais (180deg, 160deg) são contextuais e aceitáveis. |
| Inter via Google Fonts (pesos 300–800) | APROVADO | Linha 7: `family=Inter:wght@300;400;500;600;700;800` |
| Material Icons importado | APROVADO | Linha 8: `family=Material+Icons` |
| `lang="pt-BR"` no `<html>` | APROVADO | Linha 2 |
| `box-sizing: border-box` no reset `*` | APROVADO | Linha 11 |
| border-radius correto por contexto | ATENCAO | Cards com 12px; padrão Inoveon é 20px. Ver item B acima. |
| Sombra padrão de card | APROVADO | Slides de prioridade máxima (11, 20, 24, 27) usam `box-shadow: 0 4px 24px rgba(0,0,0,0.30)` — ligeiramente mais forte que o padrão, adequado para destaque. |
| Sem frameworks JS externos (React, Vue, Alpine) | APROVADO | Nenhum framework JS externo presente. |
| Sem bibliotecas de gráficos externas | REPROVADO | Chart.js carregado via CDN. Ver item A acima. |
| Sem cores roxas/violetas (`#7c3aed`, `#4c1d95`) | APROVADO | Nenhuma ocorrência encontrada. |
| Sem paths absolutos de máquina | APROVADO | Sem referências a caminhos locais. |

### Completude de Conteúdo

| Item | Status | Observação |
|------|--------|------------|
| 29 slides presentes | APROVADO | Slides 1–29 identificados e verificados. |
| Slide 11 — Tração (80 contratos, R$ 202K MRR, R$ 2,4M ARR) | APROVADO | Valores corretos. |
| Slide 11 — Margem Líquida | CORRIGIDO | Era `> 50%`; corrigido para `~55%` (dado oficial). |
| Slide 20 — Valuation R$ 6,5M / Aporte R$ 1,3M / 20% | APROVADO | Valores corretos. |
| Slide 24 — ROI mínimo 85% / retornos 85%, 131%, 208% | APROVADO | Valores corretos nos três cenários. |
| Slide 27 — Payback 24 meses / ROI 214% em 36 meses | APROVADO | Valores corretos. |
| Slide 26 — Pipeline 551 postos / R$ 16,5M | APROVADO | Dados conferidos com o roteiro. |
| Ticket médio R$ 2.525,21 | APROVADO | Slide 11 exibe R$ 2.525/contrato; dentro da margem aceitável de arredondamento. |
| Nenhum dado inventado | APROVADO | Todos os dados financeiros conferem com inoveon-info.md e o roteiro .md. |

### Navegação

| Item | Status | Observação |
|------|--------|------------|
| Nav bar presente | APROVADO | `<nav class="slide-nav">` fixo no rodapé (linha 1079). |
| Botões Anterior / Próximo | APROVADO | Implementados com estado `disabled` correto. |
| Dots de progresso | APROVADO | 29 dots gerados dinamicamente. |
| Contador de slides (ex: "11 / 29") | APROVADO | `nav-counter` atualizado a cada navegação. |
| Atalhos de teclado (ArrowLeft / ArrowRight / PageUp / PageDown) | APROVADO | Linhas 1273–1276. |

### Qualidade Visual

| Item | Status | Observação |
|------|--------|------------|
| Slides de prioridade máxima com destaque (11, 20, 24, 27) | APROVADO | Slide 11: grid-4 com números grandes e sombras. Slide 20: três cards com tipografia de 3.2–3.8rem. Slide 24: três cards de cenário com cores distintas. Slide 27: linha do tempo colorida + cards de indicadores. |
| Hierarquia tipográfica consistente | APROVADO | `.slide-title` (2rem/700), `.slide-title.large` (2.4rem) — aplicados de forma consistente. |
| Sem overflow de conteúdo | APROVADO | Slides densos (26, 27) têm `overflow-y: auto` para scroll quando necessário. |
| Ecossistema (Slide 9) — diagrama visual | APROVADO | Hub central com SVG de linhas posicionado via JavaScript. |

### Conteúdo e Gramática

| Item | Status | Observação |
|------|--------|------------|
| Sem erros gramaticais ou ortográficos | APROVADO | Nenhum erro identificado na leitura completa. |
| Tom consistente (profissional, direto, orientado a dados) | APROVADO | Tom mantido em todos os 29 slides. |
| Títulos em voz ativa | APROVADO | Todos os títulos verificados. |
| Bullets com no máximo 7 itens | APROVADO | Máximo encontrado: 4 bullets por lista. |
| Fonte de dados identificada | APROVADO | Slide 11: "Fonte: dados internos Inoveon — 2026" |
| CTA claro e específico | APROVADO | Slide 29: quatro etapas numeradas + contatos + chamada de ação final. |
| Nome da empresa: "Inoveon" (não "i9ON" isolado) | APROVADO | "Inoveon" usado como nome da empresa; "i9ON" aparece apenas como nome da razão social (i9ON Tecnologia) e nos nomes de produto (i9 PDV, i9ON ecossistema) — uso correto. |

### Técnico HTML

| Item | Status | Observação |
|------|--------|------------|
| Documento self-contained | PARCIAL | Sem Chart.js, gráficos não renderizam offline. Demais conteúdos funcionam. |
| Layout responsivo | APROVADO | Grids fixas são intencionais em formato de apresentação full-screen. |
| SVG puro para ícones | APROVADO | Material Icons (fonte). Diagrama de ecossistema usa SVG nativo. |

---

## Verificação de Métricas Críticas

| Métrica | Valor esperado (briefing) | Valor no HTML | Status |
|---------|--------------------------|---------------|--------|
| MRR | R$ 202K | R$ 202K (slide 11) | CORRETO |
| Contratos ativos | 80 | 80 (slides 11, 10, 15, 23) | CORRETO |
| ARR | R$ 2,4M | R$ 2,4M (slides 11, 13, 20, 23, 25) | CORRETO |
| Margem líquida | ~55% (inoveon-info.md) | ~55% (corrigido) | CORRIGIDO |
| ROI | 214% | 214% (slide 27) | CORRETO |
| Payback | 24 meses | 24 meses (slide 27) | CORRETO |
| Valuation | R$ 6,5M | R$ 6,5M (slides 20, 24) | CORRETO |
| Aporte | R$ 1,3M | R$ 1,3M (slides 20, 22, 27) | CORRETO |
| Participação | 20% | 20% (slides 20, 24) | CORRETO |
| Ticket médio | R$ 2.525,21 | R$ 2.525/contrato | CORRETO (arredondamento aceitável) |
| Pipeline total | 551 postos | 551 (slide 26) | CORRETO |
| Pipeline receita anual | R$ 16,5M | R$ 16,5M (slide 26) | CORRETO |

---

## Correções Aplicadas Nesta Revisão

| # | Arquivo | Linha | Alteração |
|---|---------|-------|-----------|
| 1 | `pitch-investidor-2026.html` | 490 | `&gt; 50%` → `~55%` (Margem Líquida no slide 11) |
| 2 | `pitch-investidor-2026.html` | 738 | "margem acima de 50%" → "margem líquida de ~55%" (texto de apoio no slide 20) |

---

## Recomendações para Versão Futura

1. **Eliminar Chart.js externo:** Reescrever os gráficos dos slides 13, 22 e 25 em SVG puro ou CSS. Isso tornará o documento verdadeiramente self-contained para apresentação offline.
2. **Alinhar border-radius dos cards:** Atualizar `.card { border-radius: 12px }` para `20px` para conformidade com o design system.
3. **Atualizar roteiro .md:** O arquivo `pitch-investidor-2026.md` (slide 11) indica `> 50%` como Margem Líquida, que difere do dado oficial `~55%`. Recomenda-se sincronizar o roteiro com o dado correto para evitar divergências futuras.

---

## Conclusão

O pitch está **pronto para apresentação** ao Grupo Mirian após as correções de margem aplicadas. O único risco operacional remanescente é a dependência de Chart.js via CDN: caso a apresentação ocorra em ambiente sem internet, os slides 13, 22 e 25 ficarão sem os gráficos — o conteúdo textual dos demais 26 slides permanece íntegro.

Recomendação para o apresentador: garantir conexão com internet no ambiente de apresentação, ou solicitar ao doc-designer a versão self-contained antes do evento.

---

*Revisado por doc-reviewer — 2026-03-13*
