# Pitch Investidor 2026 — Estrutura de Slides para Implementação HTML

**Produzido por:** doc-slides
**Data:** 2026-03-13
**Destino:** doc-designer — implementação HTML completa
**Fonte de conteúdo:** `pitch-investidor-2026.md`
**Total de slides:** 29
**Público:** Grupo Mirian — Conselho / Investidores

---

## DESIGN SYSTEM GLOBAL

| Token | Valor |
|-------|-------|
| Gradiente padrão | `linear-gradient(135deg, #12162B 0%, #011E4B 50%, #005BAA 100%)` |
| Fundo escuro base | `#12162B` |
| Azul primário | `#005BAA` |
| Azul médio | `#011E4B` |
| Cor de sucesso/positivo | `#28a745` |
| Cor de alerta/tensão | `#ffc107` |
| Cor de risco/negativo | `#dc3545` (usar com parcimônia — apenas slides 3, 19) |
| Texto primário | `#FFFFFF` |
| Texto secundário | `rgba(255,255,255,0.65)` |
| Acento de citação | `#64B5F6` (azul claro) |
| Tipografia | Inter (Google Fonts) — pesos 300, 400, 600, 700, 800 |
| Ícones | Material Icons |
| Border radius padrão | `12px` |
| Card background | `rgba(255,255,255,0.06)` |
| Card border | `1px solid rgba(255,255,255,0.10)` |

### Navegação Global (presente em TODOS os slides)

- **Posição:** barra fixa na base da tela (altura 56px)
- **Fundo da nav:** `rgba(0,0,0,0.55)` com `backdrop-filter: blur(8px)`
- **Esquerda:** botão `← Anterior` (desabilitado no slide 1)
- **Centro:** dots de progresso clicáveis (29 dots) + contador `"N / 29"` abaixo dos dots
- **Direita:** botão `Próximo →` (desabilitado no slide 29)
- **Teclas de atalho:** seta esquerda / seta direita para navegação
- **Transição entre slides:** fade com `opacity` (300ms, `ease-in-out`)

---

## CONVENÇÕES DE LAYOUT

| Layout Type | Quando usar |
|-------------|-------------|
| `capa` | Slide 1 — sem conteúdo informacional, apenas identidade |
| `bullets-coluna` | Conteúdo textual simples com lista vertical |
| `dois-blocos` | Dois grupos de conteúdo lado a lado (desktop) / empilhados (mobile) |
| `cards-grid-2x2` | Quatro cards em grade 2 colunas × 2 linhas |
| `cards-grid-4col` | Quatro cards em linha horizontal |
| `cards-grid-3col` | Três cards em linha horizontal |
| `cards-grid-2col` | Dois cards lado a lado |
| `timeline-horizontal` | Etapas sequenciais com setas de progressão |
| `metricas-hero` | Cards de métricas com número gigante em destaque |
| `grafico-barra` | Gráfico de barras verticais ou horizontais (Chart.js) |
| `grafico-linha` | Gráfico de linha dupla ou simples (Chart.js) |
| `grafico-pizza` | Gráfico de pizza/donut (Chart.js) |
| `tabela-dados` | Tabela estruturada com linhas e colunas |
| `diagrama-hub` | Hub central com conexões radiais (SVG ou CSS) |
| `cta-final` | Slide de encerramento com CTA e contatos |
| `dois-caminhos` | Duas colunas contrastando cenários opostos |
| `timeline-vertical` | Linha do tempo com marcos verticais |

---

## SLIDES — ESPECIFICAÇÃO EDITORIAL

---

### Slide 1 — CAPA

**Layout type:** `capa`
**Fundo:** `linear-gradient(135deg, #12162B 0%, #011E4B 55%, #005BAA 100%)` — gradiente completo
**Navegação:** dots visíveis mas botões Anterior/Próximo com visibilidade reduzida (sem destaque)

**Hierarquia visual (ordem de leitura):**
1. Logo Inoveon — centro superior (ou terço superior da tela)
2. Título principal: "i9ON Tecnologia" — Inter 800, 64–72px, branco, centrado
3. Subtítulo: "Construindo a próxima geração de tecnologia para postos de combustíveis" — Inter 300, 22–26px, `rgba(255,255,255,0.80)`, centrado, espaçamento generoso
4. Linha de apoio: "Pitch de Investimento — 2026" — Inter 400, 16px, `rgba(255,255,255,0.50)`, centrado, margem-top generosa

**Elemento de destaque:** Título "i9ON Tecnologia" — máximo peso e tamanho
**Elemento visual adicional:** Sutil partícula ou ruído de textura no gradiente (opcional — não sobrecarregar)
**Sem:** bullets, tabelas, ícones de conteúdo
**Altura:** 100vh (tela cheia)

---

### Slide 2 — O SETOR

**Layout type:** `bullets-coluna`
**Fundo:** `#12162B` com leve gradiente para `#011E4B` na base
**Largura de conteúdo:** máx 760px, centralizado

**Hierarquia visual (ordem de leitura):**
1. Título: "O setor de postos de combustíveis é um dos mais complexos do varejo brasileiro" — Inter 700, 36–40px, branco
2. Lista de bullets — Inter 400, 18px, `rgba(255,255,255,0.85)`, com ícone `circle` azul (`#005BAA`) à esquerda de cada item; espaçamento entre items: 20px
3. Bloco de citação destacado: "Nenhum outro segmento de varejo..." — tipografia 20px, Inter 400 itálico, cor `#64B5F6`, borda esquerda 3px `#005BAA`, padding 16px 24px, `background: rgba(0,91,170,0.12)`

**Elemento de destaque:** Citação em bloco — deve chamar a atenção como conclusão do slide
**Bullets (4 itens):**
- "Grande volume de transações diárias em cada posto"
- "Forte dependência de sistemas tecnológicos para operar"
- "Regras fiscais altamente específicas e em constante atualização"
- "Integração entre múltiplos processos simultâneos — abastecimento, caixa, estoque, fiscal"
**Ícone sugerido (Material Icons):** `local_gas_station` ou `business` no canto decorativo opcional

---

### Slide 3 — O PROBLEMA

**Layout type:** `dois-blocos`
**Fundo:** `#12162B` — tom ligeiramente mais frio para reforçar tensão
**Largura de conteúdo:** máx 860px, centralizado

**Hierarquia visual (ordem de leitura):**
1. Título: "A tecnologia que sustenta grande parte das operações não acompanhou a evolução do setor" — Inter 700, 34–38px, branco
2. **Bloco esquerdo — "Desafios Estruturais":** label em Inter 600 12px uppercase `#ffc107`; 4 bullets com ícone `warning` em `#ffc107` à esquerda; texto Inter 400 17px
3. **Bloco direito — "Consequência Direta":** label em Inter 600 12px uppercase `#dc3545`; 3 bullets com ícone `error_outline` em `#dc3545`; texto Inter 400 17px
4. Citação de impacto na base (largura total): "O setor evoluiu muito. A tecnologia que o sustenta, não." — Inter 600, 22px, branco, centralizado, `background: rgba(220,53,69,0.10)`, borda superior e inferior 1px `rgba(220,53,69,0.30)`, padding 20px

**Elemento de destaque:** Citação base — deve ser o encerramento visual mais impactante do slide
**Paleta de tensão:** usar `#ffc107` e `#dc3545` com moderação — apenas nos ícones e labels, não no texto corrido
**Layout mobile:** blocos empilhados verticalmente (Desafios acima, Consequências abaixo)

---

### Slide 4 — A OPORTUNIDADE

**Layout type:** `metricas-hero` com variação de dois cards grandes
**Fundo:** `linear-gradient(135deg, #011E4B 0%, #005BAA 100%)` — mais azul, tom otimista
**Largura de conteúdo:** máx 900px, centralizado

**Hierarquia visual (ordem de leitura):**
1. Título: "42 mil postos. Nenhuma plataforma dominante. A janela está aberta." — Inter 800, 36–42px, branco; os três fragmentos separados por ponto devem ter peso visual crescente
2. **Dois cards grandes lado a lado:**
   - Card 1: número "42.000" em Inter 800 72px branco; label "Postos em operação no Brasil" em Inter 300 16px `rgba(255,255,255,0.70)`
   - Card 2: palavra "Nenhuma" em Inter 800 48px `#ffc107`; label "Plataforma tecnológica dominante no setor" em Inter 300 16px `rgba(255,255,255,0.70)`
3. Bloco de texto centralizado: "Esse vácuo só pode ser preenchido por quem combina..." com os três ativos em **negrito** (`#64B5F6`)
4. Citação de fechamento: "A pergunta não é se a transformação acontecerá..." — Inter 400 itálico 18px, cor `#64B5F6`, borda esquerda

**Elemento de destaque:** "42.000" — número com maior hierarquia visual do slide, deve dominar o espaço
**Card background:** `rgba(255,255,255,0.10)`, border `rgba(255,255,255,0.15)`, radius 16px

---

### Slide 5 — ORIGEM DA INOVEON

**Layout type:** `cards-grid-2x2` com destaque numérico no topo
**Fundo:** `#12162B` com leve vinheta escura nas bordas
**Largura de conteúdo:** máx 880px, centralizado

**Hierarquia visual (ordem de leitura):**
1. Título: "A Inoveon nasceu dentro da realidade operacional dos postos — não fora dela" — Inter 700, 34px, branco
2. Destaque "10 anos" — Inter 800, 56px, `#005BAA`, centralizado, antes dos cards; label "de atuação direta no setor" em Inter 300 18px `rgba(255,255,255,0.65)` ao lado ou abaixo
3. **Grid 2×2 — quatro cards de pilar:**
   - Card "Regras Fiscais" — ícone `gavel`, título Inter 600 18px, descrição Inter 400 15px `rgba(255,255,255,0.75)`
   - Card "Processos Operacionais" — ícone `settings`, mesmo estilo
   - Card "Integrações" — ícone `device_hub`, mesmo estilo
   - Card "Necessidades Reais" — ícone `people`, mesmo estilo

**Elemento de destaque:** "10 anos" em tipografia de impacto antes dos cards
**Cards:** `background: rgba(255,255,255,0.06)`, border `rgba(255,255,255,0.10)`, padding 24px, radius 12px
**Ícones:** Material Icons, cor `#64B5F6`, tamanho 28px, alinhados ao topo esquerdo do card

---

### Slide 6 — EVOLUÇÃO DA EMPRESA

**Layout type:** `timeline-horizontal`
**Fundo:** `linear-gradient(135deg, #12162B 0%, #011E4B 100%)`
**Largura de conteúdo:** máx 960px, centralizado

**Hierarquia visual (ordem de leitura):**
1. Título: "Três fases. Uma decisão estratégica que mudou o rumo da empresa." — Inter 700, 34px, branco
2. **Timeline horizontal com três etapas conectadas por linha progressiva:**
   - **Fase 1 — Aprendizado do Mercado:** círculo numerado "1" em `#005BAA`; título Inter 700 18px; texto Inter 400 15px `rgba(255,255,255,0.75)`; ícone `school`
   - **Fase 2 — Diagnóstico do Problema:** círculo "2" em `#005BAA`; mesmo estilo; ícone `search`
   - **Fase 3 — Decisão Estratégica:** círculo "3" em `#28a745` (verde — ponto de inflexão); título em `#28a745`; card com borda verde; ícone `rocket_launch`
3. Citação de virada na base: "Esse foi o momento em que a i9ON deixou de ser apenas uma prestadora de serviços..." — Inter 400 itálico 18px, `#64B5F6`, borda esquerda azul

**Elemento de destaque:** Fase 3 — deve ter destaque visual máximo (borda verde, background levemente mais claro, sombra suave)
**Linha de progresso:** linha horizontal fina (2px, `rgba(255,255,255,0.25)`) conectando os três círculos
**Layout mobile:** empilhar as três fases verticalmente com linha vertical de conexão

---

### Slide 7 — PRIMEIRAS SOLUÇÕES PRÓPRIAS

**Layout type:** `cards-grid-2col`
**Fundo:** `#12162B`
**Largura de conteúdo:** máx 900px, centralizado

**Hierarquia visual (ordem de leitura):**
1. Título: "As primeiras soluções fora da caixa provaram que era possível inovar no setor" — Inter 700, 34px, branco
2. **Dois cards lado a lado (igual tamanho):**
   - **Card "Smart Feed":** badge "Smart Feed" em `#005BAA` (pill); ícone `smartphone` 32px; título Inter 700 20px; 4 bullets com ícone `check_circle` verde; descrição Inter 400 15px
   - **Card "Smart Count":** badge "Smart Count" em `#28a745` (pill); ícone `inventory_2` 32px; título Inter 700 20px; 3 bullets com ícone `check_circle` verde; descrição Inter 400 15px
3. Citação no rodapé: "Essas soluções mostraram que era possível inovar no setor..." — Inter 400 itálico 17px, `#64B5F6`, centralizado

**Elemento de destaque:** os dois cards com nomes em badges de cor — Smart Feed e Smart Count
**Cards:** background `rgba(255,255,255,0.06)`, border `rgba(255,255,255,0.10)`, padding 28px 24px, radius 14px
**Layout mobile:** empilhados verticalmente

---

### Slide 8 — A VIRADA TECNOLÓGICA

**Layout type:** `cards-grid-2x2`
**Fundo:** `linear-gradient(160deg, #011E4B 0%, #12162B 100%)`
**Largura de conteúdo:** máx 900px, centralizado

**Hierarquia visual (ordem de leitura):**
1. Título: "i9 Smart PDV e Ticket Eletrônico: tecnologia passou a ser parte central da operação" — Inter 700, 34px, branco
2. **Grid 2×2 — quatro cards de benefício:**
   - "Emissão na Pista" — ícone `receipt_long`, cor `#64B5F6`; título Inter 600 17px; descrição Inter 400 14px
   - "Redução de Erros" — ícone `check_circle`, cor `#28a745`
   - "Controle de Vendas" — ícone `bar_chart`, cor `#64B5F6`
   - "Estabilidade" — ícone `security`, cor `#28a745`
3. Mensagem central em bloco destacado (largura total): "Com o i9 Smart PDV, a tecnologia deixou de ser um suporte para a operação e se tornou parte estrutural dela." — Inter 500 18px, branco, `background: rgba(0,91,170,0.15)`, borda esquerda 3px `#005BAA`

**Elemento de destaque:** Os cards com ícones coloridos — identidade visual de produto
**Cards:** background `rgba(255,255,255,0.07)`, border `rgba(255,255,255,0.10)`, padding 24px, radius 12px
**Nota:** Se houver mockup/screenshot do produto disponível, substituir um dos cards por imagem enquadrada — decisão do doc-designer conforme ativos disponíveis

---

### Slide 9 — ECOSSISTEMA TECNOLÓGICO

**Layout type:** `diagrama-hub`
**Fundo:** `linear-gradient(135deg, #12162B 0%, #011E4B 100%)`
**Largura de conteúdo:** máx 900px, centralizado

**Hierarquia visual (ordem de leitura):**
1. Título: "Um ecossistema completo — oito soluções integradas em torno de um hub central" — Inter 700, 34px, branco
2. **Diagrama radial central:**
   - **Centro (hub):** card ou círculo maior com label "Hub Inoveon" + ícone `hub`; texto "Camada de integração" abaixo em Inter 300 13px; cor de fundo `#005BAA`; border 2px white
   - **8 satélites ao redor** em disposição radial (ou dois arcos — 4 à esquerda, 4 à direita):
     - i9 PDV Web — ícone `point_of_sale`
     - Smart View — ícone `dashboard`
     - Smart Ticket — ícone `confirmation_number`
     - Smart Count — ícone `inventory_2`
     - Smart Feed — ícone `campaign`
     - Smart Queue — ícone `queue`
     - Smart PDV — ícone `smartphone`
     - Integrações — ícone `sync_alt`
   - **Linhas de conexão** do hub para cada satélite: 1px `rgba(255,255,255,0.25)`, animação sutil de pulso (CSS keyframe opcional)
3. Cada satélite: card pequeno (120×80px), ícone + nome; cor de fundo `rgba(255,255,255,0.08)`, border `rgba(255,255,255,0.15)`

**Elemento de destaque:** Hub central — maior, com cor sólida `#005BAA`, deve atrair o olho primeiro
**Implementação:** SVG posicionado absolutamente ou CSS `position: absolute` com layout calculado; considerar alternativa em grid circular via CSS
**Nota:** Este é o slide mais complexo visualmente — priorizar clareza sobre sofisticação

---

### Slide 10 — MODELO DE ESCALA

**Layout type:** `timeline-horizontal`
**Fundo:** `#12162B`
**Largura de conteúdo:** máx 960px, centralizado

**Hierarquia visual (ordem de leitura):**
1. Título: "Cada novo cliente segue um ciclo validado — previsível, replicável, escalável" — Inter 700, 34px, branco
2. **Fluxo horizontal de quatro etapas com setas de progressão:**
   - **Etapa 1 — Aquisição Comercial:** badge "1–4 sem" em pill `#005BAA`; ícone `handshake`; título Inter 700 16px; descrição Inter 400 13px `rgba(255,255,255,0.75)`
   - **Etapa 2 — Onboarding e Integração:** badge "2–6 sem"; ícone `settings_suggest`; mesmo estilo
   - **Etapa 3 — Implantação Assistida:** badge "2–4 sem"; ícone `rocket_launch`; mesmo estilo
   - **Etapa 4 — Expansão e Upsell:** badge "Contínuo" em pill `#28a745`; ícone `autorenew`; cor do card com borda verde; seta de "loop" visual
3. Mensagem de fechamento em bloco: "Este ciclo foi validado com 80 contratos ativos. Está pronto para ser executado em escala." — Inter 600 18px, branco, `#28a745` em "80 contratos ativos"

**Elemento de destaque:** Etapa 4 com badge verde e ícone de loop — indica continuidade e recorrência
**Setas entre etapas:** ícone `arrow_forward`, cor `rgba(255,255,255,0.40)`
**Layout mobile:** empilhamento vertical com seta `arrow_downward` entre etapas

---

### Slide 11 — TRAÇÃO ATUAL

**Layout type:** `metricas-hero`
**Fundo:** `linear-gradient(135deg, #12162B 0%, #011E4B 100%)`
**Largura de conteúdo:** máx 960px, centralizado
**Prioridade:** MÁXIMA — slide crítico do pitch

**Hierarquia visual (ordem de leitura):**
1. Título: "A i9ON já superou a fase de validação" — Inter 700, 38–42px, branco; acima dos cards
2. **Grid de quatro métricas hero (2×2 ou linha de 4):**
   - **Card 1 — Contratos Ativos:** número "80" em Inter 800 72–80px, branco; label "Contratos Ativos" Inter 300 16px `rgba(255,255,255,0.65)` abaixo
   - **Card 2 — MRR:** número "R$ 202K" em Inter 800 56px, `#28a745`; label "Receita Mensal Recorrente"
   - **Card 3 — ARR:** número "R$ 2,4M" em Inter 800 56px, `#28a745`; label "Receita Anual Recorrente"
   - **Card 4 — Margem:** número "> 50%" em Inter 800 56px, `#64B5F6`; label "Margem Líquida"
3. Linha de apoio abaixo dos cards: "Modelo 100% recorrente (SaaS) | Ticket médio: R$ 2.525/contrato" — Inter 400 15px `rgba(255,255,255,0.55)`, centralizado
4. Citação de impacto: "Não estamos pedindo que você aposte no futuro. Estamos mostrando o que já construímos." — Inter 700 20px, branco, centralizado, sem bloco destacado — puro texto forte

**Elemento de destaque:** Os quatro números em tipografia máxima — devem dominar o slide
**Cards:** background `rgba(255,255,255,0.08)`, border `rgba(255,255,255,0.12)`, padding 32px 24px, radius 16px, `box-shadow: 0 4px 24px rgba(0,0,0,0.30)`
**Nota de fonte:** rodapé discreto "Fonte: dados internos Inoveon — 2026" em Inter 300 11px `rgba(255,255,255,0.35)`

---

### Slide 12 — POTENCIAL DE MERCADO

**Layout type:** `metricas-hero` com funil conceitual
**Fundo:** `linear-gradient(160deg, #011E4B 0%, #005BAA 100%)` — azul mais vivo, tom de oportunidade
**Largura de conteúdo:** máx 880px, centralizado

**Hierarquia visual (ordem de leitura):**
1. Título: "Capturar 5% do mercado significa R$ 5,2M de receita mensal" — Inter 800, 36–40px, branco; o valor "R$ 5,2M" deve ter destaque especial (cor `#28a745` ou tamanho levemente maior)
2. **Progressão visual de três números em cards decrescentes (funil visual ou cards em linha):**
   - "42.000 postos" — o universo total; Inter 800 52px, branco
   - "2.100 postos" — meta de 5%; Inter 800 44px, `#64B5F6`; label "Meta conservadora (5%)"
   - "R$ 5,2M / mês" — resultado; Inter 800 52px, `#28a745`; label "Potencial de receita mensal"
3. Texto de contexto: "Estamos em 80 contratos. A meta de 5% representa 2.100 contratos. O caminho está mapeado e o modelo de escala está validado." — Inter 400 16px `rgba(255,255,255,0.80)`, bloco centralizado max-width 640px

**Elemento de destaque:** "R$ 5,2M / mês" — o número final do funil, maior peso e cor verde
**Separadores entre os números:** seta para baixo `arrow_downward` ou linha de redução visual
**Layout alternativo:** se o funil ficar confuso em mobile, usar três cards em linha com tamanhos iguais

---

### Slide 13 — PROJEÇÃO DE CRESCIMENTO

**Layout type:** `grafico-barra`
**Fundo:** `#12162B`
**Largura de conteúdo:** máx 820px, centralizado

**Hierarquia visual (ordem de leitura):**
1. Título: "De 80 para 500 contratos em 3 anos — crescimento de 525%" — Inter 700, 34px, branco; "525%" em `#28a745`
2. **Gráfico de barras duplas (Chart.js):**
   - Eixo X: dois pontos — "Hoje" e "Em 3 anos"
   - Barras: "Contratos" (azul `#005BAA`) e "Receita Anual" (verde `#28a745`)
   - "Hoje": 80 contratos / R$ 2,4M
   - "Em 3 anos": 500 contratos / R$ 15M
   - Valores anotados diretamente sobre cada barra (Inter 700 14px, branco)
   - Linha de tendência suave conectando os dois pontos (opcional)
   - Grid horizontal sutil: `rgba(255,255,255,0.08)`
3. Mensagem de apoio abaixo do gráfico: "Esse crescimento não é projetado no vácuo. Está ancorado em um pipeline de clientes identificados e em um modelo de escala já validado." — Inter 400 16px `rgba(255,255,255,0.75)`, centralizado

**Elemento de destaque:** Barra de "Em 3 anos" claramente maior — contraste visual imediato
**Legenda do gráfico:** inline sob o gráfico, Inter 400 13px, dots de cor correspondente
**Nota técnica:** Gráfico deve ser responsivo e renderizar via Chart.js com dataset definido no HTML

---

### Slide 14 — CUSTO DE REPLICAR A i9ON

**Layout type:** `bullets-coluna` com destaque monetário central
**Fundo:** `linear-gradient(135deg, #12162B 0%, #011E4B 100%)`
**Largura de conteúdo:** máx 800px, centralizado

**Hierarquia visual (ordem de leitura):**
1. Título: "Replicar o que a i9ON construiu custaria entre R$ 3M e R$ 5M — e levaria anos" — Inter 700, 34px, branco; o intervalo de valor em `#ffc107`
2. Sub-header: "O que qualquer concorrente precisaria construir do zero:" — Inter 600 16px uppercase `rgba(255,255,255,0.55)`
3. **Lista de 4 bullets** com ícone `block` em `#dc3545` à esquerda: Inter 400 18px, espaçamento 18px entre itens
4. **Bloco de estimativa central em destaque máximo:**
   - Label: "Estimativa de reconstrução" — Inter 400 14px uppercase `rgba(255,255,255,0.50)`
   - Valor: "R$ 3M a R$ 5M" — Inter 800 52–60px, `#ffc107`, centralizado
   - Sub-label: "apenas em desenvolvimento tecnológico — sem contar tempo nem conhecimento acumulado" — Inter 300 15px `rgba(255,255,255,0.65)`
   - Background do bloco: `rgba(255,193,7,0.08)`, border 1px `rgba(255,193,7,0.25)`, radius 12px, padding 24px

**Elemento de destaque:** "R$ 3M a R$ 5M" — número em âmbar, tipografia máxima
**Tom visual:** assertivo e protetor — comunica barreira e segurança do investimento

---

### Slide 15 — BARREIRAS DE ENTRADA

**Layout type:** `cards-grid-2x2`
**Fundo:** `#12162B`
**Largura de conteúdo:** máx 880px, centralizado

**Hierarquia visual (ordem de leitura):**
1. Título: "Concorrer com a i9ON significa reconstruir anos de tecnologia e experiência" — Inter 700, 34px, branco
2. **Grid 2×2 — quatro cards de barreira:**
   - "Conhecimento do Setor" — ícone `psychology`, cor `#64B5F6`; "10 anos de imersão..." em Inter 400 14px
   - "Plataforma Validada" — ícone `verified`, cor `#28a745`; "Tecnologia testada em produção..." em Inter 400 14px
   - "Relacionamento" — ícone `handshake`, cor `#64B5F6`; "Clientes ativos, satisfeitos..." em Inter 400 14px
   - "Ecossistema Integrado" — ícone `hub`, cor `#28a745`; "8 soluções funcionando em conjunto..." em Inter 400 14px
3. Citação de fechamento: "Concorrer com a i9ON significa reconstruir anos de tecnologia e experiência. O mercado não espera." — bloco destacado `rgba(0,91,170,0.15)`, borda esquerda `#005BAA`, Inter 500 itálico 17px, `#64B5F6`

**Elemento de destaque:** Os ícones coloridos + títulos dos cards — o olho percorre os quatro blocos em sequência
**Cards:** background `rgba(255,255,255,0.06)`, border `rgba(255,255,255,0.09)`, padding 24px, radius 12px

---

### Slide 16 — CRESCIMENTO SEM INVESTIMENTO

**Layout type:** `dois-caminhos`
**Fundo:** `linear-gradient(135deg, #12162B 0%, #011E4B 100%)`
**Largura de conteúdo:** máx 960px, centralizado

**Hierarquia visual (ordem de leitura):**
1. Título: "A i9ON cresce com ou sem o aporte — o investimento define a velocidade" — Inter 700, 34px, branco
2. **Duas colunas contrastantes (50% / 50%):**
   - **Coluna esquerda — "Sem Investimento":** header pill `rgba(255,255,255,0.15)` + label Inter 600 14px uppercase; 4 bullets com ícone `trending_up` em `rgba(255,255,255,0.50)` (neutro); borda do bloco `rgba(255,255,255,0.10)`
   - **Coluna direita — "Com Investimento":** header pill `#005BAA` sólido + label Inter 600 14px uppercase; 4 bullets com ícone `rocket_launch` em `#28a745`; borda do bloco `rgba(0,91,170,0.40)`, background `rgba(0,91,170,0.10)` (levemente destacado)
3. Mensagem central abaixo (largura total): "A i9ON continuará crescendo. A diferença está na velocidade — e na capacidade de consolidar o mercado antes que a janela feche." — Inter 600 17px, branco, centralizado

**Elemento de destaque:** Coluna direita ("Com Investimento") — deve ter destaque visual claro, como se fosse o caminho escolhido
**Separador visual entre colunas:** linha vertical fina `rgba(255,255,255,0.15)` ou espaço generoso
**Layout mobile:** colunas empilhadas — "Com Investimento" acima ("Sem Investimento" abaixo ou oculto no mobile)

---

### Slide 17 — POR QUE O GRUPO MIRIAN

**Layout type:** `cards-grid-3col` com equação central
**Fundo:** `linear-gradient(135deg, #011E4B 0%, #005BAA 100%)` — azul, tom colaborativo
**Largura de conteúdo:** máx 920px, centralizado

**Hierarquia visual (ordem de leitura):**
1. Título: "O Grupo Mirian não é apenas um investidor financeiro — é o parceiro operacional ideal" — Inter 700, 34px, branco
2. **Três cards horizontais (benefícios):**
   - "Validação Tecnológica em Produção Real" — ícone `factory`; Inter 700 16px; descrição Inter 400 14px
   - "Desenvolvimento Orientado à Prática" — ícone `engineering`; mesmo estilo
   - "Aceleração da Inovação" — ícone `speed`; mesmo estilo
3. **Equação em destaque central:** "Tecnologia + Operação = Inovação Real" — Inter 800, 32–36px, branco; os três termos separados por `+` e `=` em `#64B5F6`; largura total, centralizado, bloco com background `rgba(255,255,255,0.08)` e padding generoso
4. Citação de fechamento: "Nenhum outro investidor oferece o que o Grupo Mirian oferece: acesso direto à operação que a plataforma serve." — Inter 400 itálico 16px, `rgba(255,255,255,0.80)`

**Elemento de destaque:** Equação "Tecnologia + Operação = Inovação Real" — o conceito central do slide
**Cards:** background `rgba(255,255,255,0.10)`, border `rgba(255,255,255,0.15)`, padding 22px, radius 12px

---

### Slide 18 — O QUE MUDA PARA O GRUPO MIRIAN

**Layout type:** `bullets-coluna` com numeração e frase de transformação
**Fundo:** `#12162B`
**Largura de conteúdo:** máx 780px, centralizado

**Hierarquia visual (ordem de leitura):**
1. Título: "Com a participação societária, o Grupo Mirian deixa de ser cliente e passa a ser dono da plataforma" — Inter 700, 34px, branco
2. **Três itens numerados em lista visual:**
   - Cada item: número em círculo `#005BAA` (Inter 700 20px), título Inter 700 18px, descrição Inter 400 16px `rgba(255,255,255,0.75)`
   - Item 1: ícone `connect_without_contact` — "Acesso Direto à equipe tecnológica da i9ON"
   - Item 2: ícone `rocket_launch` — "Evolução Rápida das soluções"
   - Item 3: ícone `shield` — "Menor Dependência de fornecedores externos"
3. **Bloco de transformação (base do slide — largura total):**
   - "Tecnologia deixa de ser custo. Passa a ser ativo estratégico do Grupo Mirian." — Inter 700 24px, branco, centralizado
   - Background `rgba(0,91,170,0.20)`, border superior e inferior 1px `#005BAA`, padding 24px
   - Ícone `trending_up` em `#28a745` à esquerda do texto (decorativo)

**Elemento de destaque:** Frase de transformação na base — deve parecer uma conclusão inevitável
**Espaçamento:** 24px entre cada item numerado

---

### Slide 19 — O CUSTO DE NÃO ENTRAR

**Layout type:** `bullets-coluna` com tensão visual
**Fundo:** `linear-gradient(135deg, #12162B 0%, #1a0a0a 100%)` — levemente mais frio/escuro para tensão
**Largura de conteúdo:** máx 780px, centralizado

**Hierarquia visual (ordem de leitura):**
1. Título: "Sem participação societária, o Grupo Mirian permanece apenas como cliente" — Inter 700, 34px, branco; "apenas como cliente" pode ter peso diferenciado (`rgba(255,255,255,0.70)` ou itálico)
2. **Sub-header:** "O que o Grupo Mirian perde ao não entrar:" — Inter 600 14px uppercase `rgba(255,255,255,0.50)`, margin-bottom 20px
3. **Lista de 4 bullets** com ícone `remove_circle_outline` em `#dc3545` à esquerda; Inter 400 17px, espaçamento 18px entre itens
4. **Bloco de urgência:**
   - "A oportunidade de participar da construção da plataforma pode ser única. O mercado não esperará." — Inter 600 18px, branco, borda esquerda 3px `#ffc107`, background `rgba(255,193,7,0.08)`, padding 16px 20px

**Elemento de destaque:** Bloco de urgência na base — deve gerar reflexão sem ser alarmista
**Tom de controle:** ícones de alerta em vermelho suave — não usar vermelho saturado; manter sobriedade executiva
**Ícone de tensão decorativo:** `hourglass_top` em `rgba(255,193,7,0.15)` no canto superior direito (decorativo, tamanho 80px)

---

### Slide 20 — ESTRUTURA DA PARCERIA

**Layout type:** `metricas-hero` com tabela limpa
**Fundo:** `linear-gradient(135deg, #12162B 0%, #011E4B 100%)`
**Largura de conteúdo:** máx 880px, centralizado
**Prioridade:** MÁXIMA — slide financeiro central

**Hierarquia visual (ordem de leitura):**
1. Título: "Valuation de R$ 6,5M — aporte de R$ 1,3M por 20% de participação" — Inter 700, 34px, branco
2. **Três cards em linha horizontal — os três números principais:**
   - Card 1: "R$ 6,5M" — Inter 800 56px, branco; label "Valuation Atual da i9ON" Inter 300 15px
   - Card 2: "20%" — Inter 800 64px, `#64B5F6`; label "Participação Proposta" Inter 300 15px
   - Card 3: "R$ 1,3M" — Inter 800 56px, `#28a745`; label "Aporte Necessário" Inter 300 15px
3. **Linha de separação sutil** (1px `rgba(255,255,255,0.10)`)
4. Linha de contexto: "Objetivo do aporte: Acelerar crescimento e consolidar mercado" — Inter 400 16px `rgba(255,255,255,0.65)`, centralizado, ícone `flag` à esquerda
5. Mensagem de apoio: "O valuation de R$ 6,5M reflete a realidade atual: R$ 2,4M de receita anual recorrente, margem acima de 50% e plataforma validada em produção." — Inter 400 15px `rgba(255,255,255,0.70)`, max-width 680px, centralizado

**Elemento de destaque:** Os três números em tipografia máxima — dominam o slide
**Cards dos números:** background `rgba(255,255,255,0.08)`, border `rgba(255,255,255,0.12)`, padding 32px 28px, radius 14px

---

### Slide 21 — GOVERNANÇA DA PARCERIA

**Layout type:** `dois-blocos`
**Fundo:** `#12162B`
**Largura de conteúdo:** máx 880px, centralizado

**Hierarquia visual (ordem de leitura):**
1. Título: "Gestão operacional na i9ON. Decisões estratégicas em conjunto." — Inter 700, 34px, branco
2. **Dois blocos lado a lado:**
   - **Bloco esquerdo — "Gestão i9ON":** header com ícone `business_center` + label Inter 700 16px; bullet: "Gestão operacional e técnica permanece integralmente na i9ON"; bullet: "Criação de conselho estratégico para decisões relevantes"; cor de borda `#005BAA`
   - **Bloco direito — "Conselho Estratégico":** header com ícone `groups` + label Inter 700 16px; 4 bullets de cobertura do conselho; cor de borda `rgba(255,255,255,0.25)`
3. Mensagem de confiança na base: "Transparência e alinhamento são a base da parceria. O investidor tem visibilidade total — sem interferência operacional desnecessária." — Inter 400 itálico 16px, `#64B5F6`, bloco centralizado

**Elemento de destaque:** Bloco esquerdo com borda azul — indica protagonismo da gestão i9ON
**Blocos:** background `rgba(255,255,255,0.06)`, border lateral 3px (borda esquerda colorida), padding 24px, radius 12px
**Ícone decorativo:** `balance` em `rgba(255,255,255,0.05)` como marca d'água no fundo (decorativo)

---

### Slide 22 — DESTINAÇÃO DO INVESTIMENTO

**Layout type:** `grafico-pizza` com legenda lateral
**Fundo:** `#12162B` (ou `#FFFFFF` para maior contraste do gráfico — decisão do designer)
**Largura de conteúdo:** máx 900px, centralizado
**Nota:** Este é o único slide onde fundo claro pode ser considerado — avaliar com o gráfico renderizado

**Hierarquia visual (ordem de leitura):**
1. Título: "R$ 1,3M alocados com precisão — cada real com destino definido" — Inter 700, 34px; (branco se fundo escuro / `#12162B` se fundo claro)
2. **Gráfico de donut (Chart.js) — metade esquerda da tela:**
   - Segmento 1: Expansão Comercial 35% — cor `#005BAA`
   - Segmento 2: Implantação e Sucesso 25% — cor `#28a745`
   - Segmento 3: Infraestrutura 15% — cor `#64B5F6`
   - Segmento 4: Evolução da Plataforma 15% — cor `#ffc107`
   - Segmento 5: Marketing 10% — cor `#6c757d`
   - Centro do donut: "R$ 1,3M" Inter 700 24px + "Total Alocado" Inter 300 13px
3. **Legenda lateral (metade direita) — 5 linhas:**
   - Cada linha: dot de cor + porcentagem Inter 700 18px + valor em reais Inter 600 16px + label Inter 400 14px
   - Ordenado de maior para menor

**Elemento de destaque:** "Expansão Comercial 35%" — maior fatia, cor azul primário
**Dataset Chart.js:** definir explicitamente os 5 segmentos com cores e valores
**Total na base:** "Total: R$ 1.300.000" — Inter 400 14px `rgba(0,0,0,0.50)` se fundo claro / `rgba(255,255,255,0.45)` se escuro

---

### Slide 23 — EXPANSÃO DA EQUIPE

**Layout type:** `cards-grid-2col` com contexto de equipe atual
**Fundo:** `linear-gradient(135deg, #12162B 0%, #011E4B 100%)`
**Largura de conteúdo:** máx 880px, centralizado

**Hierarquia visual (ordem de leitura):**
1. Título: "A equipe cresce nas duas frentes que o mercado exige: tecnologia e operações" — Inter 700, 34px, branco
2. **Dois cards principais (contratações previstas):**
   - **Card "Tecnologia":** ícone `code` em `#64B5F6`, 32px; título Inter 700 20px; bullets: Devs Full Stack, Especialistas Protheus, UX/UI — ícone `add_circle` verde à esquerda
   - **Card "Operações":** ícone `support_agent` em `#64B5F6`, 32px; título Inter 700 20px; bullets: Suporte N1, Suporte N2, Suporte N3 — mesmo estilo
3. **Bloco "Equipe Atual"** (menor, abaixo dos cards, centralizado):
   - Label "Equipe Atual" — Inter 600 13px uppercase `rgba(255,255,255,0.45)`
   - "3 sócios fundadores + 5 colaboradores" — Inter 400 15px `rgba(255,255,255,0.65)`
   - Ícones `person` pequenos (8 ícones) como visualização simbólica
4. Mensagem de crescimento: "A equipe atual sustentou 80 contratos e R$ 2,4M de receita anual. Com o aporte, a capacidade de absorção cresce na mesma proporção que a carteira." — Inter 400 15px `rgba(255,255,255,0.70)`, centralizado

**Elemento de destaque:** Os dois cards de contratações com ícones coloridos
**Cards:** background `rgba(255,255,255,0.07)`, border `rgba(255,255,255,0.10)`, padding 28px, radius 14px

---

### Slide 24 — RETORNO POTENCIAL DO INVESTIMENTO

**Layout type:** `cards-grid-3col` com código de cores por cenário
**Fundo:** `#12162B`
**Largura de conteúdo:** máx 960px, centralizado
**Prioridade:** MÁXIMA — slide de retorno, crítico para o investidor

**Hierarquia visual (ordem de leitura):**
1. Título: "Três cenários. Retorno mínimo de 85% sobre o aporte em 3 anos." — Inter 700, 36px, branco; "85%" em `#28a745`
2. **Três cards verticais lado a lado — um por cenário:**
   - **Card Conservador** (fundo `rgba(100,181,246,0.12)`, borda `#64B5F6`):
     - Badge "Conservador" Inter 600 12px
     - Valuation: "R$ 12M" Inter 800 42px, branco
     - Participação 20%: "R$ 2,4M" Inter 700 24px, `#64B5F6`
     - Retorno: "+85%" Inter 800 36px, `#64B5F6`
   - **Card Moderado** (fundo `rgba(0,91,170,0.18)`, borda `#005BAA`):
     - Badge "Moderado" Inter 600 12px
     - "R$ 15M" Inter 800 42px
     - "R$ 3,0M" Inter 700 24px, `#005BAA`
     - "+131%" Inter 800 36px, `#005BAA`
   - **Card Otimista** (fundo `rgba(40,167,69,0.15)`, borda `#28a745`, com `box-shadow` verde suave):
     - Badge "Otimista" Inter 600 12px
     - "R$ 20M" Inter 800 42px
     - "R$ 4,0M" Inter 700 24px, `#28a745`
     - "+208%" Inter 800 36px, `#28a745`
3. Mensagem de ancoragem abaixo: "No cenário conservador, o valuation dobra em relação ao atual de R$ 6,5M. O crescimento necessário para isso é inferior à metade do que a projeção de mercado indica." — Inter 400 15px `rgba(255,255,255,0.70)`, max-width 700px, centralizado

**Elemento de destaque:** Os três valores de retorno em porcentagem — "+85%", "+131%", "+208%" — devem ser os maiores elementos visuais de cada card
**Card Otimista:** deve ter sombra sutil verde para indicar o melhor cenário possível

---

### Slide 25 — PROJEÇÃO DE VALORIZAÇÃO

**Layout type:** `grafico-linha`
**Fundo:** `linear-gradient(135deg, #12162B 0%, #011E4B 100%)`
**Largura de conteúdo:** máx 880px, centralizado

**Hierarquia visual (ordem de leitura):**
1. Título: "ARR cresce de R$ 2,4M para R$ 15M em 3 anos — valuation segue na mesma direção" — Inter 700, 34px, branco; "R$ 15M" em `#28a745`
2. **Gráfico de linha dupla (Chart.js):**
   - Eixo X: 3 pontos — "Hoje", "Em 2 anos", "Em 3 anos"
   - **Linha 1 — ARR:** cor branco `#FFFFFF`, pontos circulares; valores: 2.4 / 8 / 15 (em M)
   - **Linha 2 — Valuation:** cor `#64B5F6`, pontos circulares; valores: 6.5 / 13.5 / 20+ (em M)
   - Valores anotados diretamente sobre cada ponto (Inter 700 13px)
   - Grid horizontal: `rgba(255,255,255,0.08)`; sem grid vertical
   - Eixo Y: oculto ou com labels mínimas
   - Área sob cada linha: fill semitransparente (10–15% de opacidade)
3. Legenda inline abaixo do gráfico: dot branco "Receita Anual Recorrente" | dot azul "Valuation Estimado"
4. Nota metodológica: "Valuation estimado com base em múltiplo de receita recorrente, padrão de mercado para SaaS em crescimento acelerado." — Inter 300 13px `rgba(255,255,255,0.45)`, italico

**Elemento de destaque:** Os pontos finais das duas linhas ("R$ 15M" e "R$ 20M+") — devem ter círculos maiores e labels em destaque
**Animação Chart.js:** entrada progressiva das linhas da esquerda para a direita (padrão Chart.js)

---

### Slide 26 — PIPELINE DE CLIENTES

**Layout type:** `tabela-dados` com barras de progresso visual
**Fundo:** `#12162B`
**Largura de conteúdo:** máx 920px, centralizado

**Hierarquia visual (ordem de leitura):**
1. Título: "R$ 16,5M de receita anual em potencial — 551 postos mapeados no pipeline" — Inter 700, 34px, branco; "R$ 16,5M" em `#28a745`
2. **Tabela com 8 grupos + linha de total:**
   - Colunas: Grupo | Postos | Receita Mensal | Barra visual
   - Cada linha: Inter 400 15px; barra proporcional ao número de postos (max: Rede Sim com 181 = 100%)
   - Barra: div com background `rgba(0,91,170,0.40)`, preenchimento proporcional em `#005BAA`, altura 6px, radius 3px
   - **Linha de total** (última): Inter 700 16px, branco; fundo `rgba(40,167,69,0.15)`, borda superior 1px `#28a745`; "551" e "R$ 1,37M/mês" em `#28a745`
3. **Bloco de destaque acima ou abaixo da tabela:**
   - "R$ 16,5M / ano" — Inter 800 48px, `#28a745`, centralizado; label "Receita anual potencial do pipeline"
4. Contexto abaixo: "Esses não são leads frios. São grupos com quem a i9ON já tem relacionamento ou está em processo ativo de aproximação." — Inter 400 15px `rgba(255,255,255,0.70)`

**Elemento de destaque:** Número "R$ 16,5M / ano" e linha de total da tabela
**Tabela styling:** fundo `rgba(255,255,255,0.04)`, linhas alternadas (zebragem sutil `rgba(255,255,255,0.03)`), border-bottom por linha `rgba(255,255,255,0.08)`

---

### Slide 27 — JORNADA DO RETORNO FINANCEIRO

**Layout type:** `timeline-vertical` com indicadores resumo
**Fundo:** `linear-gradient(135deg, #12162B 0%, #011E4B 100%)`
**Largura de conteúdo:** máx 960px, centralizado
**Prioridade:** MÁXIMA — slide de retorno detalhado

**Hierarquia visual (ordem de leitura):**
1. Título: "Payback em 24 meses. ROI de 214% em 36 meses." — Inter 800, 36–40px, branco; "214%" em `#28a745`
2. **Linha do tempo horizontal com 6 marcos (pode ser horizontal em desktop, vertical em mobile):**
   - Cada marco: círculo colorido + label de mês + evento + valor acumulado
   - **Fase vermelha (investimento):** Mês 0–8 e Mês 8–12 — círculos `#dc3545`, valores negativos em `#dc3545`
   - **Fase amarela (recuperação):** Mês 18 — círculo `#ffc107`, "-R$ 600K" em `#ffc107`
   - **Marco de payback:** Mês 24 — círculo maior `#28a745` com borda dupla, label "PAYBACK" em badge verde, "R$ 0" em branco
   - **Fase verde (lucro):** Mês 30 e Mês 36 — círculos `#28a745`, valores positivos em `#28a745`
   - Linha de conexão: fina, cor gradiente de vermelho para verde conforme progride
3. **Grid de indicadores resumo (5 cards compactos abaixo da timeline):**
   - Payback: "24 meses" Inter 700 22px
   - Receita Total: "R$ 3,77M" Inter 700 22px
   - Lucro Projetado: "R$ 2,57M" Inter 700 22px
   - **ROI: "214%" Inter 800 32px, `#28a745`** — card com borda verde e destaque máximo
   - MRR final: "R$ 209K" Inter 700 22px

**Elemento de destaque:** Marco de Payback no Mês 24 e o card "ROI 214%" — os dois pontos focais do slide
**Nota de layout:** Este é o slide mais denso — priorizar clareza absoluta; se necessário, reduzir tamanho de fonte para garantir leitura

---

### Slide 28 — VISÃO DE 10 ANOS

**Layout type:** `bullets-coluna` com fundo inspiracional
**Fundo:** `linear-gradient(135deg, #12162B 0%, #011E4B 50%, #005BAA 100%)` com overlay de imagem conceitual (opcional — mapa do Brasil ou horizonte, tratado com `opacity: 0.08`)
**Largura de conteúdo:** máx 780px, centralizado

**Hierarquia visual (ordem de leitura):**
1. Título: "Não queremos apenas crescer. Queremos modernizar todo o setor de postos do Brasil." — Inter 800, 38–42px, branco, centralizado; este é o título mais emocional da apresentação — tratamento especial de linha e espaçamento
2. Sub-header: "Os três objetivos de longo prazo:" — Inter 600 14px uppercase `rgba(255,255,255,0.50)`
3. **Três itens numerados (não bullets — números grandes):**
   - Número "01", "02", "03" em Inter 800 36px `rgba(0,91,170,0.50)` à esquerda (decorativo)
   - Texto dos objetivos Inter 500 18px branco à direita; espaçamento 28px entre itens
4. Sub-header 2: "Onde estaremos em 10 anos:" — Inter 600 14px uppercase `rgba(255,255,255,0.50)`
5. Três bullets mais curtos com ícone `check` em `#28a745`; Inter 400 16px
6. Citação de visão: "Não queremos apenas crescer como empresa. Queremos ajudar a modernizar todo o setor de postos de combustíveis do Brasil." — Inter 300 itálico 20px, `rgba(255,255,255,0.85)`, centralizado, padding-top generoso

**Elemento de destaque:** O título — deve ser o maior e mais impactante desta parte da apresentação
**Tom:** este é o slide mais inspiracional — tipografia leve (Inter 300) na citação final, espaços generosos, sem poluição visual
**Não usar:** ícones de alerta, vermelho ou amarelo neste slide — apenas branco, azul e verde

---

### Slide 29 — ENCERRAMENTO / CTA

**Layout type:** `cta-final`
**Fundo:** `linear-gradient(135deg, #12162B 0%, #011E4B 55%, #005BAA 100%)` — gradiente completo (espelha a capa)
**Largura de conteúdo:** máx 860px, centralizado

**Hierarquia visual (ordem de leitura):**
1. Logo Inoveon — topo centralizado (menor que na capa — função de ancoragem)
2. Título: "A próxima etapa é a confirmação do aporte" — Inter 700, 36–40px, branco, centralizado
3. **Quatro passos em layout horizontal (ou 2×2 no mobile):**
   - Cada passo: número em círculo `#005BAA` Inter 700 20px; ícone representativo; título Inter 600 16px; sem descrição longa
   - Passo 1 — "Confirmação do interesse" — ícone `thumb_up`
   - Passo 2 — "Formalização dos termos" — ícone `description`
   - Passo 3 — "Assinatura do contrato" — ícone `draw`
   - Passo 4 — "Início da execução" — ícone `rocket_launch`
   - Setas `arrow_forward` entre passos (ocultas no mobile)
4. **Dois cards de contato lado a lado:**
   - Card "Lee Chardes — CEO": ícone `person`; nome Inter 700 17px; cargo Inter 400 14px `rgba(255,255,255,0.65)`; email Inter 400 15px `#64B5F6` (link clicável)
   - Card "Rodrigo Felippe — CFO/COO": mesmo estilo
5. Link de website: "inoveon.com.br" — Inter 400 16px, `#64B5F6`, com ícone `open_in_new`, clicável
6. Citação final: "Obrigado pela atenção. A janela está aberta. A decisão é agora." — Inter 700 22px, branco, centralizado, padding-top 24px

**Elemento de destaque:** Citação final — a última coisa que o investidor lê
**Navegação:** botão "Próximo" desabilitado (este é o último slide); botão "Anterior" visível
**Cards de contato:** background `rgba(255,255,255,0.08)`, border `rgba(255,255,255,0.15)`, padding 20px 24px, radius 12px

---

## MATRIZ DE PRIORIDADE VISUAL

| Prioridade | Slides | Justificativa |
|------------|--------|---------------|
| MÁXIMA | 1, 11, 20, 24, 27, 29 | Capa, tração, financeiro, retorno, ROI, CTA |
| ALTA | 4, 9, 13, 25, 26 | Oportunidade, ecossistema, crescimento, valorização, pipeline |
| PADRÃO | 2, 5, 6, 7, 8, 10, 12, 14, 15, 17, 22, 23, 28 | Contexto, produto, modelo, mercado, equipe, visão |
| CONTEXTUAL | 3, 16, 18, 19, 21 | Problema, contraste, benefícios, urgência, governança |

---

## MAPEAMENTO DE LAYOUTS

| Layout Type | Slides que usam |
|-------------|-----------------|
| `capa` | 1 |
| `bullets-coluna` | 2, 14, 18, 19, 28 |
| `dois-blocos` | 3, 21 |
| `metricas-hero` | 4, 11, 12, 20 |
| `cards-grid-2x2` | 5, 8, 15 |
| `cards-grid-4col` | — |
| `cards-grid-3col` | 17, 24 |
| `cards-grid-2col` | 7, 23 |
| `timeline-horizontal` | 6, 10 |
| `timeline-vertical` | 27 |
| `diagrama-hub` | 9 |
| `grafico-barra` | 13 |
| `grafico-linha` | 25 |
| `grafico-pizza` | 22 |
| `tabela-dados` | 26 |
| `dois-caminhos` | 16 |
| `cta-final` | 29 |

---

## DEPENDÊNCIAS TÉCNICAS

| Biblioteca | Versão | Uso |
|------------|--------|-----|
| Inter (Google Fonts) | — | Tipografia global |
| Material Icons | — | Ícones em todos os slides |
| Chart.js | 4.x CDN | Slides 13, 22, 25 |
| Chart.js — chartjs-plugin-datalabels | 2.x CDN | Labels sobre gráficos |

---

## INSTRUÇÃO FINAL PARA O DOC-DESIGNER

1. Implementar como Single-Page Application (SPA) com 29 slides em divs ocultas, exibidas via JavaScript
2. Cada slide ocupa `100vw × 100vh` — sem scroll interno (excepcionalmente slide 26 pode ter scroll se a tabela não couber)
3. Navegação via teclado (setas) obrigatória além dos botões
4. Responsividade mínima: funcionar em telas 1024px+ (desktop e laptop); adaptações mobile são bonus
5. Todos os gráficos Chart.js devem ter `responsive: true` e `maintainAspectRatio: false` dentro de containers com altura definida
6. Slides de prioridade máxima (1, 11, 20, 24, 27, 29) devem ser implementados primeiro e revisados antes dos demais
7. Fonte de conteúdo authoritative: `pitch-investidor-2026.md` — não adicionar nem remover conteúdo
8. Não usar animações pesadas — transição `opacity` simples é suficiente; evitar `transform` complexos que possam travar
9. Cores e tokens definidos neste documento são lei — não inventar variações não documentadas
