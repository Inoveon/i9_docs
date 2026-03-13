# doc-designer — Design System i9ON

## Documentação Detalhada

- [ui-patterns.md](ui-patterns.md) — Referência completa: tokens, componentes, gráficos SVG, ícones, template base

---

## Paleta de Cores

| Token | Hex | Uso |
|-------|-----|-----|
| `--i9-dark` | `#12162B` | Fundo principal, textos escuros |
| `--i9-navy` | `#011E4B` | Gradientes intermediários |
| `--i9-blue` | `#005BAA` | Ação primária, destaques, bordas ativas |
| `--i9-light` | `#E7E7E7` | Divisores, backgrounds sutis |
| `--white` | `#ffffff` | Cards, fundos limpos |
| `--gray-100` | `#f1f3f5` | Background global da página |
| `--gray-200` | `#E7E7E7` | Bordas padrão |
| `--gray-300` | `#dee2e6` | Bordas inputs |
| `--gray-500` | `#adb5bd` | Placeholders |
| `--gray-700` | `#495057` | Textos secundários |
| `--gray-900` | `#12162B` | Textos principais |
| `--success` | `#28a745` | Variações positivas, confirmações |
| `--warning` | `#ffc107` | Alertas, avisos |
| `--error` | `#dc3545` | Erros, variações negativas |

## Tipografia

- **Fonte principal**: Inter (Google Fonts) — pesos: 300, 400, 500, 600, 700, 800
- **Ícones**: Material Icons (Google Fonts) — `<span class="material-icons">nome</span>`
- **Ícones alt**: Material Symbols Outlined (quando precisar de variações de estilo)

### Escala tipográfica
| Uso | Tamanho | Peso |
|-----|---------|------|
| H1 página | 2.5rem | 800 |
| H2 seção | 2rem | 700 |
| H3 card | 1.8rem | 700 |
| Card title | 1.2rem | 700 |
| Body | 1rem / 0.95rem | 400 |
| Label form | 0.95rem | 600 |
| Caption | 0.85rem | 400 |
| Badge | 0.8rem | 600 |

## Gradiente Padrão

```css
background: linear-gradient(135deg, #12162B 0%, #011E4B 50%, #005BAA 100%);
```

Variações:
- KPI card: `linear-gradient(135deg, #005BAA 0%, #011E4B 100%)`
- Hover icon: `linear-gradient(135deg, #005BAA 0%, #011E4B 100%)`

## Border Radius

| Contexto | Valor |
|----------|-------|
| Pill / badge | 50px |
| Botão | 50px |
| Input | 12px |
| Card pequeno | 12px |
| Card médio | 16px |
| Card/seção | 20px |
| Container | 20px |

## Sombras

| Contexto | Valor |
|----------|-------|
| Card padrão | `0 4px 20px rgba(0,0,0,0.08)` |
| Card hover | `0 8px 30px rgba(0,91,170,0.15)` |
| Header principal | `0 8px 30px rgba(0,0,0,0.15)` |
| KPI card | `0 8px 25px rgba(0,91,170,0.3)` |
| Botão azul | `0 6px 20px rgba(0,91,170,0.4)` |

## Transições

```css
transition: all 0.3s;
transition: all 0.3s ease;
```

Hover padrão de card: `transform: translateY(-5px);`

## CSS Reset Padrão

```css
* { margin: 0; padding: 0; box-sizing: border-box; }
body { font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif; background: #f1f3f5; color: #12162B; line-height: 1.6; }
```

## Componentes — Estrutura

### Header de Página
```html
<div class="header" style="background: linear-gradient(135deg, #12162B 0%, #011E4B 50%, #005BAA 100%); color: #fff; padding: 50px 30px; border-radius: 20px; margin-bottom: 30px; text-align: center; box-shadow: 0 8px 30px rgba(0,0,0,0.15);">
  <h1 style="font-size: 2.5rem; font-weight: 800; margin-bottom: 10px;">Título</h1>
  <p style="opacity: 0.9; font-size: 1.1rem;">Subtítulo</p>
</div>
```

### Card Padrão
```html
<div style="background: #fff; border-radius: 20px; padding: 30px; box-shadow: 0 4px 20px rgba(0,0,0,0.08); margin-bottom: 30px;">
  <!-- conteúdo -->
</div>
```

### KPI Card (gradiente)
```html
<div style="background: linear-gradient(135deg, #005BAA 0%, #011E4B 100%); border-radius: 20px; padding: 35px; color: #fff; text-align: center; box-shadow: 0 8px 25px rgba(0,91,170,0.3);">
  <div style="width: 70px; height: 70px; background: rgba(255,255,255,0.2); border-radius: 50%; display: flex; align-items: center; justify-content: center; margin: 0 auto 20px;">
    <span class="material-icons" style="font-size: 35px;">trending_up</span>
  </div>
  <div style="font-size: 3rem; font-weight: 800; margin-bottom: 5px;">127k</div>
  <div style="font-size: 1rem; opacity: 0.9;">Vendas Totais</div>
</div>
```

### Card com Mini-Chart SVG
```html
<div style="background: linear-gradient(135deg, #005BAA 0%, #011E4B 100%); border-radius: 16px; padding: 25px; color: #fff;">
  <div style="display: flex; justify-content: space-between; align-items: start; margin-bottom: 15px;">
    <div>
      <div style="font-size: 0.85rem; opacity: 0.9; margin-bottom: 5px;">Métrica</div>
      <div style="font-size: 2rem; font-weight: 800;">R$ 127k</div>
      <div style="font-size: 0.85rem; opacity: 0.8; margin-top: 5px;"><span style="color: #28a745;">▲ 12.5%</span> vs. mês anterior</div>
    </div>
    <svg viewBox="0 0 80 40" style="width: 80px; height: 40px;">
      <path d="M 0,30 L 20,25 L 40,20 L 60,10 L 80,5" stroke="rgba(255,255,255,0.8)" stroke-width="2" fill="none" stroke-linecap="round"/>
      <path d="M 0,30 L 20,25 L 40,20 L 60,10 L 80,5 L 80,40 L 0,40 Z" fill="rgba(255,255,255,0.2)"/>
    </svg>
  </div>
</div>
```

### Section Title com ícone
```html
<h2 style="font-size: 2rem; font-weight: 700; color: #12162B; margin-bottom: 30px; padding-bottom: 20px; border-bottom: 3px solid #005BAA; display: flex; align-items: center; gap: 15px;">
  <span class="material-icons" style="font-size: 2.2rem; color: #005BAA;">analytics</span>
  Título da Seção
</h2>
```

### Badge / Tag
```html
<span style="background: rgba(0,91,170,0.1); color: #005BAA; padding: 8px 20px; border-radius: 20px; font-size: 0.85rem; font-weight: 600;">Label</span>
```

### Step (passo numerado)
```html
<div style="background: #f1f3f5; border-left: 4px solid #005BAA; padding: 20px; margin-bottom: 15px; border-radius: 8px;">
  <span style="display: inline-block; width: 30px; height: 30px; background: #005BAA; color: #fff; border-radius: 50%; text-align: center; line-height: 30px; font-weight: 700; margin-right: 10px;">1</span>
  <strong>Título do passo</strong>
</div>
```

### Alert / Warning Box
```html
<div style="background: #fff3cd; border-left: 4px solid #ffc107; padding: 20px; border-radius: 8px;">
  <h4 style="display: flex; align-items: center; gap: 10px; margin-bottom: 15px;">
    <span class="material-icons" style="color: #ffc107;">lightbulb</span>
    <span style="font-size: 1.1rem; font-weight: 700; color: #856404;">Atenção</span>
  </h4>
  <p style="color: #856404;">Conteúdo do alerta.</p>
</div>
```

## Layouts Grid

```css
/* 2 colunas responsivas */
display: grid; grid-template-columns: repeat(auto-fit, minmax(500px, 1fr)); gap: 30px;

/* 3 colunas responsivas */
display: grid; grid-template-columns: repeat(auto-fit, minmax(350px, 1fr)); gap: 30px;

/* 4 colunas responsivas */
display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px;
```

## Gráficos SVG Puros

### Barra horizontal
```html
<div style="margin-bottom: 15px;">
  <div style="display: flex; justify-content: space-between; margin-bottom: 5px;">
    <span style="font-size: 0.9rem; color: #495057;">Label</span>
    <span style="font-size: 0.9rem; font-weight: 700; color: #12162B;">75%</span>
  </div>
  <div style="background: #E7E7E7; border-radius: 4px; height: 8px;">
    <div style="background: linear-gradient(90deg, #005BAA, #011E4B); width: 75%; height: 8px; border-radius: 4px;"></div>
  </div>
</div>
```

### Linha SVG (sparkline)
```html
<svg viewBox="0 0 300 100" style="width: 100%; height: 100px;">
  <defs>
    <linearGradient id="grad" x1="0%" y1="0%" x2="0%" y2="100%">
      <stop offset="0%" style="stop-color:#005BAA;stop-opacity:0.3"/>
      <stop offset="100%" style="stop-color:#005BAA;stop-opacity:0"/>
    </linearGradient>
  </defs>
  <path d="M 0,80 L 60,60 L 120,40 L 180,55 L 240,20 L 300,10" stroke="#005BAA" stroke-width="2.5" fill="none" stroke-linecap="round" stroke-linejoin="round"/>
  <path d="M 0,80 L 60,60 L 120,40 L 180,55 L 240,20 L 300,10 L 300,100 L 0,100 Z" fill="url(#grad)"/>
</svg>
```

### Pizza SVG
```html
<svg viewBox="0 0 200 200" style="width: 200px; height: 200px;">
  <!-- Fatia 1: 60% — #005BAA -->
  <circle cx="100" cy="100" r="80" fill="none" stroke="#005BAA" stroke-width="40" stroke-dasharray="301.6 502.6" stroke-dashoffset="0" transform="rotate(-90 100 100)"/>
  <!-- Fatia 2: 25% — #011E4B -->
  <circle cx="100" cy="100" r="80" fill="none" stroke="#011E4B" stroke-width="40" stroke-dasharray="125.7 502.6" stroke-dashoffset="-301.6" transform="rotate(-90 100 100)"/>
  <!-- Fatia 3: 15% — #adb5bd -->
  <circle cx="100" cy="100" r="80" fill="none" stroke="#adb5bd" stroke-width="40" stroke-dasharray="75.4 502.6" stroke-dashoffset="-427.3" transform="rotate(-90 100 100)"/>
  <circle cx="100" cy="100" r="60" fill="white"/>
  <text x="100" y="95" text-anchor="middle" font-size="18" font-weight="800" fill="#12162B">60%</text>
  <text x="100" y="115" text-anchor="middle" font-size="12" fill="#495057">Principal</text>
</svg>
```

## Ícones Material Icons — Categorias Principais

| Categoria | Exemplos de ícones |
|-----------|-------------------|
| Negócios | business, domain, store, account_balance, work, corporate_fare |
| Crescimento/Analytics | trending_up, show_chart, analytics, bar_chart, pie_chart, timeline |
| Validação | verified, check_circle, task_alt, done_all, fact_check |
| Tecnologia | computer, code, api, developer_mode, cloud, memory |
| Documentos | description, article, folder, file_copy, assignment, picture_as_pdf |
| Pessoas | person, people, group, account_circle, manage_accounts |
| E-commerce | shopping_cart, payments, credit_card, point_of_sale, monetization_on |
| Tempo | schedule, calendar_today, event, date_range, history |
| Segurança | security, lock, shield, verified_user, fingerprint |
| Comunicação | email, message, chat, forum, send |
| Navegação | arrow_forward, chevron_right, navigate_next, expand_more |
| Ações | add, edit, delete, save, download, upload, refresh, share |
| Notificações | notifications, warning, error, info, campaign |
| Interface | menu, dashboard, grid_view, widgets, apps |

Uso: `<span class="material-icons" style="font-size: 2rem; color: #005BAA;">nome_icone</span>`

## Formulários

### Input padrão
```html
<div style="margin-bottom: 20px;">
  <label style="display: block; font-weight: 600; color: #12162B; margin-bottom: 8px; font-size: 0.95rem;">Label</label>
  <input type="text" placeholder="Placeholder" style="width: 100%; padding: 12px 16px; border: 2px solid #dee2e6; border-radius: 12px; font-family: 'Inter', sans-serif; font-size: 0.95rem; color: #12162B; transition: all 0.3s ease; background: #fff; outline: none;">
</div>
```

### Botão primário
```html
<button style="background: linear-gradient(135deg, #005BAA 0%, #011E4B 100%); color: #fff; border: none; padding: 14px 30px; border-radius: 50px; font-family: 'Inter', sans-serif; font-size: 1rem; font-weight: 600; cursor: pointer; box-shadow: 0 6px 20px rgba(0,91,170,0.4); transition: all 0.3s; display: inline-flex; align-items: center; gap: 8px;">
  <span class="material-icons">save</span> Salvar
</button>
```

### Botão outline
```html
<button style="background: transparent; color: #005BAA; border: 2px solid #005BAA; padding: 12px 28px; border-radius: 50px; font-family: 'Inter', sans-serif; font-size: 1rem; font-weight: 600; cursor: pointer; transition: all 0.3s;">
  Cancelar
</button>
```

## Template Base HTML

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
      --white: #ffffff; --gray-100: #f1f3f5; --gray-200: #E7E7E7;
      --gray-300: #dee2e6; --gray-700: #495057; --gray-900: #12162B;
      --success: #28a745; --warning: #ffc107; --error: #dc3545;
    }
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { font-family: 'Inter', sans-serif; background: var(--gray-100); color: var(--gray-900); line-height: 1.6; }
    .container { max-width: 1400px; margin: 0 auto; padding: 30px 20px; }
    .section { background: var(--white); border-radius: 20px; padding: 40px; margin-bottom: 30px; box-shadow: 0 4px 20px rgba(0,0,0,0.08); }
  </style>
</head>
<body>
  <!-- Header -->
  <div style="background: linear-gradient(135deg, #12162B 0%, #011E4B 50%, #005BAA 100%); color: #fff; padding: 50px 30px; text-align: center; box-shadow: 0 8px 30px rgba(0,0,0,0.15);">
    <h1 style="font-size: 2.5rem; font-weight: 800; margin-bottom: 10px;">Título do Documento</h1>
    <p style="opacity: 0.9; font-size: 1.1rem;">Subtítulo ou descrição</p>
  </div>

  <div class="container">
    <!-- Conteúdo aqui -->
  </div>
</body>
</html>
```
