# UI Patterns — Design System i9ON (Documentos HTML Standalone)

> Documento de referência para criação de apresentações, relatórios e documentos HTML
> do projeto i9_docs (Inoveon/i9ON). Todos os outputs são arquivos HTML self-contained
> — sem frameworks JS, sem bundlers, sem dependências externas além de Google Fonts.
>
> Agente responsável: `doc-designer`

---

## Stack Obrigatória

| Item | Valor |
|------|-------|
| Linguagem | HTML5 + CSS3 + SVG puro |
| Fonte principal | Inter via Google Fonts (pesos: 300 400 500 600 700 800) |
| Ícones | Material Icons via Google Fonts |
| Ícones alt | Material Symbols Outlined (variante com fill/weight/grade) |
| Gráficos | SVG puro — sem Chart.js, D3.js, Highcharts ou similar |
| Frameworks JS | PROIBIDO — sem React, Vue, Alpine.js ou similar |
| CSS | Bloco `<style>` no `<head>` — nunca arquivo externo separado |
| Self-contained | Todo documento deve funcionar offline (exceto Google Fonts) |

---

## Tokens de Cor — Paleta i9ON

Declarar em `:root` em todo documento gerado. **Nunca hardcodar valores sem usar os tokens.**

```css
:root {
  /* Marca */
  --i9-dark:  #12162B;   /* Azul-escuro / quase-preto — fundo principal, textos */
  --i9-navy:  #011E4B;   /* Azul-marinho — gradientes intermediários */
  --i9-blue:  #005BAA;   /* Azul primário — ações, destaques, bordas ativas */
  --i9-light: #E7E7E7;   /* Cinza-azulado claro — divisores, backgrounds sutis */

  /* Neutros */
  --white:    #ffffff;
  --gray-100: #f1f3f5;   /* Background global da página */
  --gray-200: #E7E7E7;   /* Bordas padrão */
  --gray-300: #dee2e6;   /* Bordas de inputs */
  --gray-500: #adb5bd;   /* Placeholders, textos desabilitados */
  --gray-700: #495057;   /* Textos secundários */
  --gray-900: #12162B;   /* Textos principais (idêntico a --i9-dark) */

  /* Semânticos */
  --success: #28a745;    /* Variações positivas, confirmações */
  --warning: #ffc107;    /* Alertas, avisos */
  --error:   #dc3545;    /* Erros, variações negativas */
}
```

---

## Gradientes

```css
/* Gradiente principal — headers, slides de capa, seções de destaque */
background: linear-gradient(135deg, #12162B 0%, #011E4B 50%, #005BAA 100%);

/* Gradiente KPI card */
background: linear-gradient(135deg, #005BAA 0%, #011E4B 100%);

/* Gradiente barra horizontal de dado */
background: linear-gradient(90deg, #005BAA, #011E4B);

/* Gradiente área de gráfico SVG (fill sob linha) */
/* Usar via <linearGradient> com stop-opacity de 0.3 → 0 */
```

---

## Tipografia

### Imports obrigatórios (sempre no `<head>`)

```html
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
```

Quando precisar de variantes outlined/filled dos ícones:
```html
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@24,400,0,0" rel="stylesheet">
```

### Reset e corpo

```css
* { margin: 0; padding: 0; box-sizing: border-box; }
body {
  font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
  background: var(--gray-100);
  color: var(--gray-900);
  line-height: 1.6;
}
```

### Escala tipográfica

| Uso | Tamanho | Peso | Cor padrão |
|-----|---------|------|------------|
| H1 — título de página | 2.5rem | 800 | var(--white) sobre gradiente |
| H2 — título de seção | 2rem | 700 | var(--i9-dark) |
| H3 — subtítulo de seção | 1.8rem | 700 | var(--i9-dark) |
| Título de card | 1.2rem | 700 | var(--i9-dark) |
| Body padrão | 1rem | 400 | var(--gray-700) |
| Label de formulário | 0.95rem | 600 | var(--gray-900) |
| Caption / legenda | 0.85rem | 400 | var(--gray-700) |
| Badge / tag | 0.8rem | 600 | var(--i9-blue) |
| Código inline | 0.85rem | 400 | monospace, bg var(--gray-200) |

---

## Geometria

| Contexto | border-radius |
|----------|---------------|
| Pill — botões, badges grandes | 50px |
| Botão padrão | 50px |
| Input de formulário | 12px |
| Card pequeno / chip | 12px |
| Card médio — chart card | 16px |
| Card principal / seção | 20px |
| Container de página / header | 20px |

---

## Sombras

| Contexto | box-shadow |
|----------|------------|
| Card padrão | `0 4px 20px rgba(0,0,0,0.08)` |
| Card hover | `0 8px 30px rgba(0,91,170,0.15)` |
| Header principal | `0 8px 30px rgba(0,0,0,0.15)` |
| KPI card com gradiente | `0 8px 25px rgba(0,91,170,0.3)` |
| Botão primário | `0 6px 20px rgba(0,91,170,0.4)` |
| Input em foco | `0 0 0 3px rgba(0,91,170,0.1)` |

---

## Transições

```css
transition: all 0.3s;          /* padrão */
transition: all 0.3s ease;     /* inputs e formulários */
```

Hover de card: `transform: translateY(-5px);`
Hover de ícone: `transform: scale(1.1);`

---

## Layouts Grid Responsivos

```css
/* 2 colunas */
display: grid;
grid-template-columns: repeat(auto-fit, minmax(500px, 1fr));
gap: 30px;

/* 3 colunas */
display: grid;
grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
gap: 30px;

/* 4 colunas — KPI cards */
display: grid;
grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
gap: 20px;

/* Ícones / itens pequenos */
display: grid;
grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
gap: 20px;
```

---

## Componentes — Templates

### Header de Página

```html
<div style="background: linear-gradient(135deg, #12162B 0%, #011E4B 50%, #005BAA 100%); color: #fff; padding: 50px 30px; border-radius: 20px; margin-bottom: 30px; text-align: center; box-shadow: 0 8px 30px rgba(0,0,0,0.15);">
  <h1 style="font-size: 2.5rem; font-weight: 800; margin-bottom: 10px;">Título</h1>
  <p style="opacity: 0.9; font-size: 1.1rem;">Subtítulo ou descrição</p>
</div>
```

### Container Padrão

```html
<div style="max-width: 1400px; margin: 0 auto; padding: 30px 20px;">
  <!-- conteúdo -->
</div>
```

### Card / Seção Branca

```html
<div style="background: #fff; border-radius: 20px; padding: 40px; margin-bottom: 30px; box-shadow: 0 4px 20px rgba(0,0,0,0.08);">
  <!-- conteúdo -->
</div>
```

### Section Title com Ícone e Border

```html
<h2 style="font-size: 2rem; font-weight: 700; color: #12162B; margin-bottom: 30px; padding-bottom: 20px; border-bottom: 3px solid #005BAA; display: flex; align-items: center; gap: 15px;">
  <span class="material-icons" style="font-size: 2.2rem; color: #005BAA;">analytics</span>
  Título da Seção
</h2>
```

### KPI Card com Gradiente

```html
<div style="background: linear-gradient(135deg, #005BAA 0%, #011E4B 100%); border-radius: 20px; padding: 35px; color: #fff; text-align: center; box-shadow: 0 8px 25px rgba(0,91,170,0.3);">
  <div style="width: 70px; height: 70px; background: rgba(255,255,255,0.2); border-radius: 50%; display: flex; align-items: center; justify-content: center; margin: 0 auto 20px;">
    <span class="material-icons" style="font-size: 35px;">trending_up</span>
  </div>
  <div style="font-size: 3rem; font-weight: 800; margin-bottom: 5px;">127k</div>
  <div style="font-size: 1rem; opacity: 0.9;">Vendas Totais</div>
  <div style="font-size: 0.85rem; opacity: 0.75; margin-top: 8px;">
    <span style="color: #28a745;">▲ 12.5%</span> vs. mês anterior
  </div>
</div>
```

### Mini-Chart Card (sparkline inline)

```html
<div style="background: linear-gradient(135deg, #005BAA 0%, #011E4B 100%); border-radius: 16px; padding: 25px; color: #fff;">
  <div style="display: flex; justify-content: space-between; align-items: start;">
    <div>
      <div style="font-size: 0.85rem; opacity: 0.9; margin-bottom: 5px;">Métrica</div>
      <div style="font-size: 2rem; font-weight: 800;">R$ 127k</div>
      <div style="font-size: 0.85rem; opacity: 0.8; margin-top: 5px;">
        <span style="color: #28a745;">▲ 12.5%</span> vs. mês anterior
      </div>
    </div>
    <svg viewBox="0 0 80 40" style="width: 80px; height: 40px;">
      <path d="M 0,30 L 20,25 L 40,20 L 60,10 L 80,5"
            stroke="rgba(255,255,255,0.8)" stroke-width="2" fill="none" stroke-linecap="round"/>
      <path d="M 0,30 L 20,25 L 40,20 L 60,10 L 80,5 L 80,40 L 0,40 Z"
            fill="rgba(255,255,255,0.2)"/>
    </svg>
  </div>
</div>
```

### Chart Card (container para gráfico)

```html
<div style="background: #fff; border: 2px solid #E7E7E7; border-radius: 16px; padding: 30px; transition: all 0.3s;">
  <h3 style="font-size: 1.2rem; font-weight: 700; color: #12162B; margin-bottom: 20px; display: flex; align-items: center; gap: 10px;">
    <span class="material-icons" style="color: #005BAA;">bar_chart</span>
    Título do Gráfico
  </h3>
  <!-- SVG do gráfico aqui -->
</div>
```

### Badge / Tag

```html
<!-- Azul padrão -->
<span style="background: rgba(0,91,170,0.1); color: #005BAA; padding: 8px 20px; border-radius: 20px; font-size: 0.85rem; font-weight: 600;">Label</span>

<!-- Sucesso -->
<span style="background: rgba(40,167,69,0.1); color: #28a745; padding: 6px 14px; border-radius: 20px; font-size: 0.8rem; font-weight: 600;">Ativo</span>

<!-- Alerta -->
<span style="background: rgba(255,193,7,0.15); color: #856404; padding: 6px 14px; border-radius: 20px; font-size: 0.8rem; font-weight: 600;">Pendente</span>

<!-- Erro -->
<span style="background: rgba(220,53,69,0.1); color: #dc3545; padding: 6px 14px; border-radius: 20px; font-size: 0.8rem; font-weight: 600;">Inativo</span>
```

### Step Numerado

```html
<div style="background: #f1f3f5; border-left: 4px solid #005BAA; padding: 20px; margin-bottom: 15px; border-radius: 8px;">
  <span style="display: inline-block; width: 30px; height: 30px; background: #005BAA; color: #fff; border-radius: 50%; text-align: center; line-height: 30px; font-weight: 700; margin-right: 10px; font-size: 0.9rem;">1</span>
  <strong>Título do passo</strong>
  <p style="margin-top: 10px; color: #495057;">Descrição do passo.</p>
</div>
```

### Alert Box

```html
<!-- Info / dica -->
<div style="background: #fff3cd; border-left: 4px solid #ffc107; padding: 20px; border-radius: 8px; margin: 20px 0;">
  <div style="display: flex; align-items: center; gap: 10px; margin-bottom: 10px;">
    <span class="material-icons" style="color: #ffc107;">lightbulb</span>
    <strong style="color: #856404; font-size: 1rem;">Atenção</strong>
  </div>
  <p style="color: #856404; line-height: 1.6;">Conteúdo do alerta.</p>
</div>

<!-- Sucesso -->
<div style="background: rgba(40,167,69,0.08); border-left: 4px solid #28a745; padding: 20px; border-radius: 8px;">
  <div style="display: flex; align-items: center; gap: 10px;">
    <span class="material-icons" style="color: #28a745;">check_circle</span>
    <strong style="color: #155724;">Mensagem de sucesso</strong>
  </div>
</div>
```

### Botão Primário

```html
<button style="background: linear-gradient(135deg, #005BAA 0%, #011E4B 100%); color: #fff; border: none; padding: 14px 30px; border-radius: 50px; font-family: 'Inter', sans-serif; font-size: 1rem; font-weight: 600; cursor: pointer; box-shadow: 0 6px 20px rgba(0,91,170,0.4); transition: all 0.3s; display: inline-flex; align-items: center; gap: 8px;">
  <span class="material-icons" style="font-size: 1.1rem;">save</span>
  Salvar
</button>
```

### Botão Outline

```html
<button style="background: transparent; color: #005BAA; border: 2px solid #005BAA; padding: 12px 28px; border-radius: 50px; font-family: 'Inter', sans-serif; font-size: 1rem; font-weight: 600; cursor: pointer; transition: all 0.3s;">
  Cancelar
</button>
```

### Input de Formulário

```html
<div style="margin-bottom: 20px;">
  <label style="display: block; font-weight: 600; color: #12162B; margin-bottom: 8px; font-size: 0.95rem;">
    Label <span style="color: #dc3545;">*</span>
  </label>
  <input type="text" placeholder="Placeholder"
         style="width: 100%; padding: 12px 16px; border: 2px solid #dee2e6; border-radius: 12px; font-family: 'Inter', sans-serif; font-size: 0.95rem; color: #12162B; transition: all 0.3s; background: #fff; outline: none;">
</div>
```

---

## Gráficos SVG Puros

### Barra de Progresso Horizontal

```html
<div style="margin-bottom: 15px;">
  <div style="display: flex; justify-content: space-between; margin-bottom: 6px;">
    <span style="font-size: 0.9rem; color: #495057; font-weight: 500;">Categoria</span>
    <span style="font-size: 0.9rem; font-weight: 700; color: #12162B;">75%</span>
  </div>
  <div style="background: #E7E7E7; border-radius: 4px; height: 8px; overflow: hidden;">
    <div style="background: linear-gradient(90deg, #005BAA, #011E4B); width: 75%; height: 8px; border-radius: 4px;"></div>
  </div>
</div>
```

### Gráfico de Linha SVG (sparkline / área)

```html
<svg viewBox="0 0 300 100" style="width: 100%; height: 100px;" preserveAspectRatio="none">
  <defs>
    <linearGradient id="areaGrad" x1="0%" y1="0%" x2="0%" y2="100%">
      <stop offset="0%" style="stop-color:#005BAA; stop-opacity:0.3"/>
      <stop offset="100%" style="stop-color:#005BAA; stop-opacity:0"/>
    </linearGradient>
  </defs>
  <!-- Área preenchida -->
  <path d="M 0,80 L 60,60 L 120,40 L 180,55 L 240,20 L 300,10 L 300,100 L 0,100 Z"
        fill="url(#areaGrad)"/>
  <!-- Linha -->
  <path d="M 0,80 L 60,60 L 120,40 L 180,55 L 240,20 L 300,10"
        stroke="#005BAA" stroke-width="2.5" fill="none"
        stroke-linecap="round" stroke-linejoin="round"/>
  <!-- Pontos -->
  <circle cx="300" cy="10" r="4" fill="#005BAA"/>
</svg>
```

### Gráfico de Pizza SVG (via stroke-dasharray)

> Circunferência do círculo com r=80: `2 × π × 80 ≈ 502.6`
> Fatia de X%: `502.6 × (X/100)`

```html
<svg viewBox="0 0 200 200" style="width: 180px; height: 180px;">
  <!-- Fatia 1: 60% = 301.6 -->
  <circle cx="100" cy="100" r="80" fill="none" stroke="#005BAA" stroke-width="40"
          stroke-dasharray="301.6 502.6" stroke-dashoffset="0"
          transform="rotate(-90 100 100)"/>
  <!-- Fatia 2: 25% = 125.7 -->
  <circle cx="100" cy="100" r="80" fill="none" stroke="#011E4B" stroke-width="40"
          stroke-dasharray="125.7 502.6" stroke-dashoffset="-301.6"
          transform="rotate(-90 100 100)"/>
  <!-- Fatia 3: 15% = 75.4 -->
  <circle cx="100" cy="100" r="80" fill="none" stroke="#adb5bd" stroke-width="40"
          stroke-dasharray="75.4 502.6" stroke-dashoffset="-427.3"
          transform="rotate(-90 100 100)"/>
  <!-- Centro vazio (donut) -->
  <circle cx="100" cy="100" r="60" fill="white"/>
  <text x="100" y="95" text-anchor="middle" font-size="18" font-weight="800" fill="#12162B">60%</text>
  <text x="100" y="115" text-anchor="middle" font-size="12" fill="#495057">Principal</text>
</svg>
```

### Gráfico de Barras Verticais SVG

```html
<svg viewBox="0 0 400 200" style="width: 100%; height: 200px;">
  <!-- Eixo Y -->
  <line x1="40" y1="10" x2="40" y2="170" stroke="#dee2e6" stroke-width="1"/>
  <!-- Eixo X -->
  <line x1="40" y1="170" x2="390" y2="170" stroke="#dee2e6" stroke-width="1"/>
  <!-- Barras (ajustar x, y, height conforme dados) -->
  <rect x="60"  y="70"  width="40" height="100" rx="4" fill="#005BAA" opacity="0.9"/>
  <rect x="130" y="40"  width="40" height="130" rx="4" fill="#005BAA" opacity="0.9"/>
  <rect x="200" y="90"  width="40" height="80"  rx="4" fill="#005BAA" opacity="0.9"/>
  <rect x="270" y="20"  width="40" height="150" rx="4" fill="#005BAA" opacity="0.9"/>
  <rect x="340" y="55"  width="40" height="115" rx="4" fill="#005BAA" opacity="0.9"/>
  <!-- Labels -->
  <text x="80"  y="188" text-anchor="middle" font-size="11" fill="#495057">Jan</text>
  <text x="150" y="188" text-anchor="middle" font-size="11" fill="#495057">Fev</text>
  <text x="220" y="188" text-anchor="middle" font-size="11" fill="#495057">Mar</text>
  <text x="290" y="188" text-anchor="middle" font-size="11" fill="#495057">Abr</text>
  <text x="360" y="188" text-anchor="middle" font-size="11" fill="#495057">Mai</text>
</svg>
```

---

## Ícones Material Icons — Referência Rápida por Categoria

Uso: `<span class="material-icons" style="font-size: 2rem; color: #005BAA;">nome_icone</span>`

| Categoria | Ícones principais |
|-----------|-------------------|
| Negócios | `business` `domain` `store` `account_balance` `work` `corporate_fare` `storefront` |
| Analytics | `trending_up` `trending_down` `show_chart` `analytics` `bar_chart` `pie_chart` `timeline` `insights` |
| Validação | `verified` `check_circle` `task_alt` `done_all` `fact_check` `assignment_turned_in` |
| Tecnologia | `computer` `code` `api` `developer_mode` `cloud` `memory` `integration_instructions` |
| Documentos | `description` `article` `folder` `file_copy` `assignment` `picture_as_pdf` `note` |
| Pessoas | `person` `people` `group` `account_circle` `manage_accounts` `engineering` `diversity_3` |
| Finanças | `payments` `credit_card` `point_of_sale` `monetization_on` `attach_money` `paid` `receipt` |
| Tempo | `schedule` `calendar_today` `event` `date_range` `history` `update` `hourglass_empty` |
| Segurança | `security` `lock` `shield` `verified_user` `fingerprint` `vpn_key` `admin_panel_settings` |
| Comunicação | `email` `message` `chat` `forum` `send` `contact_mail` `announcement` |
| Navegação | `arrow_forward` `chevron_right` `navigate_next` `expand_more` `arrow_upward` |
| Ações | `add` `edit` `delete` `save` `download` `upload` `refresh` `share` `search` |
| Notificações | `notifications` `warning` `error` `info` `campaign` `priority_high` |
| Interface | `menu` `dashboard` `grid_view` `widgets` `apps` `list` `table_chart` |
| Crescimento | `rocket_launch` `flag` `explore` `navigation` `alt_route` `signpost` |
| Cloud | `cloud` `cloud_upload` `cloud_done` `backup` `dns` `storage` |
| E-commerce | `shopping_cart` `shopping_bag` `local_mall` `sell` `redeem` `loyalty` |

---

## Template Base HTML Completo

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Título — Inoveon</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
  <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
  <style>
    :root {
      --i9-dark: #12162B; --i9-navy: #011E4B; --i9-blue: #005BAA;
      --i9-light: #E7E7E7; --white: #ffffff;
      --gray-100: #f1f3f5; --gray-200: #E7E7E7; --gray-300: #dee2e6;
      --gray-500: #adb5bd; --gray-700: #495057; --gray-900: #12162B;
      --success: #28a745; --warning: #ffc107; --error: #dc3545;
    }
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
      background: var(--gray-100);
      color: var(--gray-900);
      line-height: 1.6;
    }
    .container { max-width: 1400px; margin: 0 auto; padding: 30px 20px; }
    .section {
      background: var(--white);
      border-radius: 20px;
      padding: 40px;
      margin-bottom: 30px;
      box-shadow: 0 4px 20px rgba(0,0,0,0.08);
    }
  </style>
</head>
<body>

  <!-- HEADER -->
  <div style="background: linear-gradient(135deg, #12162B 0%, #011E4B 50%, #005BAA 100%); color: #fff; padding: 50px 30px; text-align: center; box-shadow: 0 8px 30px rgba(0,0,0,0.15); margin-bottom: 0;">
    <h1 style="font-size: 2.5rem; font-weight: 800; margin-bottom: 10px;">Título do Documento</h1>
    <p style="opacity: 0.9; font-size: 1.1rem;">Subtítulo ou descrição</p>
  </div>

  <div class="container">

    <!-- SEÇÃO 1 -->
    <div class="section">
      <h2 style="font-size: 2rem; font-weight: 700; color: var(--i9-dark); margin-bottom: 30px; padding-bottom: 20px; border-bottom: 3px solid var(--i9-blue); display: flex; align-items: center; gap: 15px;">
        <span class="material-icons" style="font-size: 2.2rem; color: var(--i9-blue);">analytics</span>
        Seção
      </h2>
      <!-- conteúdo -->
    </div>

  </div>
</body>
</html>
```

---

## NUNCA FAZER

- Usar frameworks JS externos: React, Vue, Alpine.js, Svelte
- Usar bibliotecas de gráficos: Chart.js, D3.js, Highcharts, ApexCharts
- Criar arquivo CSS separado — tudo self-contained no `<style>`
- Usar cores hardcoded fora dos tokens definidos em `:root`
- Omitir `lang="pt-BR"` no `<html>`
- Omitir `box-sizing: border-box` no reset `*`
- Omitir as fontes Google Fonts no `<head>`
- Criar layouts sem responsividade (`grid auto-fit` é obrigatório)
- Usar `rounded-full` em badges — usar `border-radius: 20px` (pílula média)
- Usar `fetch()` ou JavaScript para dados — documentos são estáticos
- Remover a seção de tokens `:root` — todo documento deve tê-la

---

## Histórico de Padrões

| Data | Padrão | Motivo |
|------|--------|--------|
| 2026-03-13 | Paleta i9ON com 13 tokens CSS | Identidade visual consistente cross-documento |
| 2026-03-13 | SVG puro para todos os gráficos | Zero dependências externas, portabilidade total |
| 2026-03-13 | Inter 300–800 via Google Fonts | Tipografia Inoveon padrão |
| 2026-03-13 | Material Icons via Google Fonts | 696 ícones categorizados, integração simples |
| 2026-03-13 | CSS self-contained no `<style>` | Documentos funcionam como arquivo único |
| 2026-03-13 | Grid `repeat(auto-fit, minmax)` | Responsividade sem media queries complexas |
