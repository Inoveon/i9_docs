# Prompt Gerador de Dados para Slides

## Instruções para a IA Geradora de Conteúdo

Você irá gerar dados estruturados para criação de slides de apresentação seguindo o formato abaixo. Os slides seguem o padrão visual Inoveon (cores: #12162B dark, #011E4B navy, #005BAA blue, #E7E7E7 light).

---

## Formato de Resposta Obrigatório

Por favor, retorne os dados em formato JSON seguindo EXATAMENTE esta estrutura:

```json
{
  "tipo_slide": "hero|conteudo|comparacao|timeline|cards|graficos|chamada",
  "titulo": "Título Principal do Slide",
  "subtitulo": "Subtítulo ou descrição breve (opcional)",
  "conteudo": {
    // Varia conforme o tipo de slide
  }
}
```

---

## Tipos de Slides Disponíveis

### 1. HERO (Slide de Abertura/Destaque)
Ideal para: Abertura da apresentação, destaque de conceito principal

```json
{
  "tipo_slide": "hero",
  "titulo": "Transformando a Gestão de Postos",
  "subtitulo": "Tecnologia e Inteligência para o Futuro",
  "icone": "rocket_launch",
  "destaque": "i9ON - Ecossistema Completo",
  "texto_apoio": "A solução mais completa do mercado para gestão inteligente de postos de combustível"
}
```

### 2. CONTEÚDO COM CARDS (Grid de Features/Benefícios)
Ideal para: Listar benefícios, features, diferenciais

```json
{
  "tipo_slide": "cards",
  "titulo": "Benefícios da Solução",
  "cards": [
    {
      "icone": "speed",
      "titulo": "Alta Performance",
      "descricao": "Processamento rápido e eficiente"
    },
    {
      "icone": "security",
      "titulo": "Segurança Total",
      "descricao": "Dados protegidos com criptografia"
    },
    {
      "icone": "cloud",
      "titulo": "100% Cloud",
      "descricao": "Acesse de qualquer lugar"
    }
  ]
}
```

### 3. COMPARAÇÃO (Antes vs Depois)
Ideal para: Mostrar melhorias, ROI, transformação

```json
{
  "tipo_slide": "comparacao",
  "titulo": "O Impacto da Transformação Digital",
  "antes": {
    "titulo": "ANTES",
    "itens": [
      "Processos manuais demorados",
      "Erros frequentes no controle",
      "Falta de visibilidade em tempo real"
    ]
  },
  "depois": {
    "titulo": "DEPOIS",
    "itens": [
      "Automação completa de processos",
      "Precisão de 99.9% no controle",
      "Dashboards em tempo real"
    ]
  },
  "resultado": {
    "metrica": "70%",
    "descricao": "Redução no tempo de operação"
  }
}
```

### 4. TIMELINE (Linha do Tempo)
Ideal para: Roadmap, jornada, fases do projeto

```json
{
  "tipo_slide": "timeline",
  "titulo": "Roadmap de Implementação",
  "etapas": [
    {
      "fase": "Fase 1",
      "titulo": "Descoberta",
      "descricao": "Análise de processos e necessidades",
      "duracao": "2 semanas"
    },
    {
      "fase": "Fase 2",
      "titulo": "Configuração",
      "descricao": "Setup inicial da plataforma",
      "duracao": "3 semanas"
    },
    {
      "fase": "Fase 3",
      "titulo": "Treinamento",
      "descricao": "Capacitação da equipe",
      "duracao": "1 semana"
    },
    {
      "fase": "Fase 4",
      "titulo": "Go Live",
      "descricao": "Lançamento e acompanhamento",
      "duracao": "2 semanas"
    }
  ]
}
```

### 5. GRÁFICOS/MÉTRICAS (Dados Numéricos)
Ideal para: Resultados, KPIs, estatísticas

```json
{
  "tipo_slide": "graficos",
  "titulo": "Resultados Comprovados",
  "metricas": [
    {
      "icone": "trending_up",
      "valor": "127%",
      "label": "Aumento em Vendas",
      "cor": "blue"
    },
    {
      "icone": "attach_money",
      "valor": "R$ 2.4M",
      "label": "Economia Anual",
      "cor": "green"
    },
    {
      "icone": "speed",
      "valor": "87%",
      "label": "Satisfação dos Clientes",
      "cor": "yellow"
    }
  ]
}
```

### 6. CHAMADA PARA AÇÃO (CTA Final)
Ideal para: Encerramento, próximos passos

```json
{
  "tipo_slide": "chamada",
  "titulo": "Pronto para Transformar seu Negócio?",
  "subtitulo": "Agende uma demonstração gratuita",
  "beneficios": [
    "Demo personalizada de 30 minutos",
    "Análise gratuita do seu cenário",
    "Proposta comercial sem compromisso"
  ],
  "cta": {
    "texto": "Agendar Demonstração",
    "icone": "calendar_today"
  },
  "contato": {
    "email": "contato@inoveon.com.br",
    "telefone": "(00) 0000-0000"
  }
}
```

### 7. LISTA COM ITENS (Checklist/Features)
Ideal para: O que está incluído, requisitos, checklist

```json
{
  "tipo_slide": "lista",
  "titulo": "O que está Incluído",
  "items": [
    {
      "icone": "check_circle",
      "texto": "Plataforma web completa",
      "destaque": true
    },
    {
      "icone": "check_circle",
      "texto": "Aplicativo mobile iOS e Android",
      "destaque": true
    },
    {
      "icone": "check_circle",
      "texto": "Integração com sistemas legados",
      "destaque": false
    },
    {
      "icone": "check_circle",
      "texto": "Suporte técnico 24/7",
      "destaque": true
    }
  ]
}
```

---

## Ícones Material Design Disponíveis

Use estes ícones nos campos `icone`:

**Negócios & Finanças:**
`business`, `payments`, `attach_money`, `trending_up`, `analytics`, `account_balance`

**Tecnologia:**
`cloud`, `code`, `phonelink`, `settings`, `api`, `integration_instructions`, `devices`

**Performance:**
`speed`, `bolt`, `flash_on`, `rocket_launch`, `trending_up`

**Segurança:**
`security`, `verified_user`, `lock`, `shield`, `admin_panel_settings`

**Pessoas:**
`groups`, `people`, `person`, `support_agent`, `engineering`

**Tempo:**
`schedule`, `timer`, `access_time`, `calendar_today`, `event`

**Status:**
`check_circle`, `verified`, `done_all`, `task_alt`, `celebration`

**Comunicação:**
`phone`, `email`, `chat`, `message`, `contact_support`

---

## Cores Disponíveis para Métricas

- `blue` - Azul Inoveon (#005BAA) - Padrão
- `green` - Verde sucesso (#28a745)
- `yellow` - Amarelo atenção (#ffc107)
- `red` - Vermelho alerta (#dc3545)
- `dark` - Escuro (#12162B)
- `navy` - Navy (#011E4B)

---

## Exemplo de Requisição

**Você diz para a IA:**
> "Crie um slide sobre os benefícios da automação de postos de combustível, destacando 4 principais vantagens"

**A IA deve responder:**
```json
{
  "tipo_slide": "cards",
  "titulo": "Por Que Automatizar Seu Posto?",
  "subtitulo": "4 benefícios que transformam o negócio",
  "cards": [
    {
      "icone": "speed",
      "titulo": "Agilidade nas Operações",
      "descricao": "Reduza em até 70% o tempo de processos manuais"
    },
    {
      "icone": "security",
      "titulo": "Controle Total",
      "descricao": "Rastreabilidade completa de todas as transações"
    },
    {
      "icone": "analytics",
      "titulo": "Decisões Baseadas em Dados",
      "descricao": "Relatórios em tempo real para gestão inteligente"
    },
    {
      "icone": "attach_money",
      "titulo": "Redução de Custos",
      "descricao": "Economize até 40% em custos operacionais"
    }
  ]
}
```

---

## Diretrizes de Conteúdo

1. **Títulos**: Máximo 60 caracteres, objetivo e impactante
2. **Descrições**: Entre 50-100 caracteres, claro e direto
3. **Números**: Use dados concretos quando possível (%, R$, tempo)
4. **Tom**: Profissional, mas acessível
5. **Foco**: Benefícios e resultados (não apenas features técnicas)

---

## Validação JSON

Antes de retornar, certifique-se que:
- ✅ O JSON está válido (sem vírgulas extras, aspas corretas)
- ✅ Todos os campos obrigatórios estão preenchidos
- ✅ Os ícones existem na lista de Material Design Icons
- ✅ As cores estão entre as disponíveis
- ✅ O tipo de slide é um dos 7 tipos listados

---

## Como Usar Este Prompt

1. Copie este documento completo
2. Cole para a IA geradora de conteúdo (ChatGPT, Claude, etc.)
3. Faça sua solicitação específica (ex: "Crie um slide sobre ROI da solução")
4. A IA retornará o JSON estruturado
5. Copie o JSON e passe para mim (Claude Code)
6. Eu crio o slide HTML automaticamente no arquivo `apresentacoes/investimento/index.html`

---

**Pronto para usar!** 🚀
