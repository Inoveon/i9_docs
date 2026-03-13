# Análise de Concentração de Clientes - i9ON Tecnologia

## 1. Resumo dos Contratos Ativos

| Métrica | Valor |
|---------|-------|
| **Total de Contratos Ativos** | 80 |
| **Receita Mensal Recorrente (MRR)** | R$ 202.016,57 |
| **Receita Anual Recorrente (ARR)** | R$ 2.424.198,84 |
| **Contratos Encerrados** | 22 |
| **Ticket Médio por Contrato** | R$ 2.525,21 |

---

## 2. Análise por Grupo de Clientes

### Grupo ALDO (Postos de Combustível)
| Cliente | Qtd Contratos | Valor Mensal |
|---------|---------------|--------------|
| ALDO RODOVIA DOS IMIGRANTES | 3 | R$ 5.368,29 |
| POSTO ALDO BARCARENA | 3 | R$ 5.368,29 |
| POSTO ALDO BARREIRAS | 3 | R$ 5.368,29 |
| POSTO ALDO CUBATAO | 3 | R$ 5.368,29 |
| POSTO ALDO CUIABA | 3 | R$ 5.368,29 |
| POSTO ALDO ITAITUBA KM 30 | 3 | R$ 5.368,29 |
| POSTO ALDO JATAI INDUSTRIAL | 3 | R$ 5.368,29 |
| POSTO ALDO LINHO | 3 | R$ 5.368,29 |
| POSTO ALDO MARINGA | 3 | R$ 5.368,29 |
| POSTO ALDO PARANAGUA I | 3 | R$ 5.368,29 |
| POSTO ALDO PORTO FRANCO | 3 | R$ 5.368,29 |
| POSTO ALDO PRIMAVERA | 3 | R$ 5.368,29 |
| POSTO ALDO RONDONOPOLIS | 3 | R$ 5.368,29 |
| POSTO ALDO SAO JOSE DOS PINHAIS | 3 | R$ 5.368,29 |
| POSTO ALDO SAO LUIS | 2 | R$ 4.591,54 |
| POSTO ALDO SORRISO | 3 | R$ 5.368,29 |
| POSTO MANGUEIRAS | 3 | R$ 5.368,29 |
| POSTO TREVO JATAI | 3 | R$ 5.368,29 |
| **SUBTOTAL GRUPO ALDO** | **53** | **R$ 95.483,47** |

### Grupo MIRIAN (Postos de Combustível)
| Cliente | Qtd Contratos | Valor Mensal |
|---------|---------------|--------------|
| MIRIAN 11 | 2 | R$ 3.706,60 |
| MIRIAN CANDEIAS | 2 | R$ 3.706,60 |
| MIRIAN ITAITUBA | 2 | R$ 3.706,60 |
| MIRIAN JARAGUARI | 2 | R$ 3.706,60 |
| MIRIAN MATUPA | 2 | R$ 3.706,60 |
| MIRIAN MIRITITUBA | 2 | R$ 3.706,60 |
| MIRIAN VARZEA GRANDE | 2 | R$ 3.706,60 |
| POSTO MIRIAN 10 | 2 | R$ 3.706,60 |
| POSTO MIRIAN BARCARENA | 2 | R$ 3.706,60 |
| **SUBTOTAL GRUPO MIRIAN** | **18** | **R$ 33.359,40** |

### AUTO POSTO IRMÃOS BATISTA
| Cliente | Qtd Contratos | Valor Mensal |
|---------|---------------|--------------|
| AUTO POSTO IRMÃOS BATISTA M1 | 2 | R$ 3.706,60 |
| AUTO POSTO IRMÃOS BATISTA M2 | 2 | R$ 3.706,60 |
| **SUBTOTAL IRMÃOS BATISTA** | **4** | **R$ 7.413,20** |

### GA SERVICE (Consultoria/Gestão)
| Cliente | Qtd Contratos | Valor Mensal |
|---------|---------------|--------------|
| GA SERVICE - contrato base | 1 | R$ 4.000,00 |
| GA SERVICE - contrato principal | 1 | R$ 42.064,00 |
| **SUBTOTAL GA SERVICE** | **2** | **R$ 46.064,00** |

### Outros Clientes
| Cliente | Qtd Contratos | Valor Mensal |
|---------|---------------|--------------|
| IB3 TI | 1 | R$ 14.340,00 |
| ASFRETE | 1 | R$ 2.987,50 |
| TRANSPORTADORA BATISTA | 1 | R$ 2.000,00 |
| **SUBTOTAL OUTROS** | **3** | **R$ 19.327,50** |

---

## 3. Concentração de Receita por Cliente/Grupo

| Grupo/Cliente | Receita Mensal | % do Total | Risco |
|---------------|----------------|------------|-------|
| **GA SERVICE** | R$ 46.064,00 | **22,8%** | ALTO |
| **Grupo ALDO** | R$ 95.483,47 | **47,3%** | CRÍTICO |
| **Grupo MIRIAN** | R$ 33.359,40 | **16,5%** | MÉDIO |
| Irmãos Batista | R$ 7.413,20 | 3,7% | Baixo |
| IB3 TI | R$ 14.340,00 | 7,1% | Médio |
| ASFRETE | R$ 2.987,50 | 1,5% | Baixo |
| Transportadora Batista | R$ 2.000,00 | 1,0% | Baixo |
| **TOTAL** | **R$ 202.016,57** | **100%** | |

---

## 4. ANÁLISE DE RISCO DE CONCENTRAÇÃO

### Visão Consolidada

```
GRUPO ALDO + MIRIAN = 63,8% da receita
       ↓
    ALERTA CRÍTICO DE CONCENTRAÇÃO
```

| Indicador | Valor | Status |
|-----------|-------|--------|
| Top 1 Cliente (GA Service) | 22,8% | ⚠️ Alto |
| Top 2 Grupos (Aldo + Mirian) | 63,8% | 🔴 Crítico |
| Top 3 (+ GA Service) | 86,6% | 🔴 Muito Crítico |
| Clientes independentes | 13,4% | Diversificado |

### O que isso significa?

**CENÁRIO DE RISCO:**
- Se o Grupo ALDO sair → perda de **47,3%** da receita (R$ 95k/mês)
- Se o Grupo MIRIAN sair → perda de **16,5%** da receita (R$ 33k/mês)
- Se GA SERVICE sair → perda de **22,8%** da receita (R$ 46k/mês)

**Se ALDO + MIRIAN saírem juntos:**
- Receita mensal cai de R$ 202k para R$ 73k
- **Perda de 64% do faturamento**

---

## 5. IMPACTO NO VALUATION

### Valuation Original (sem análise de concentração)
| Método | Valor |
|--------|-------|
| Múltiplo 5x Lucro | R$ 6.846.140 |
| Valuation sugerido | R$ 6.000.000 - R$ 7.000.000 |

### Ajuste por Risco de Concentração

**Desconto por concentração de clientes:**
- Concentração > 50% em poucos grupos = **desconto de 15-25%**
- Benchmark: Empresas com base diversificada valem mais

| Cenário | Desconto | Valuation Ajustado |
|---------|----------|-------------------|
| Conservador | -25% | R$ 4.500.000 - R$ 5.250.000 |
| Moderado | -15% | R$ 5.100.000 - R$ 5.950.000 |
| **Com investidor sendo cliente** | **0%** | **R$ 6.000.000 - R$ 7.000.000** |

### Por que o desconto pode ser ZERO?

**Se o investidor for do Grupo ALDO ou MIRIAN:**
- A concentração vira **VANTAGEM**, não risco
- Cliente-sócio = receita garantida por contrato
- Alinhamento total de interesses
- Lock-in natural do maior cliente

---

## 6. PONTOS POSITIVOS DESCOBERTOS

### Receita 100% Recorrente
| Tipo | Valor | % |
|------|-------|---|
| Contratos mensais (recorrente) | R$ 202.016,57 | **100%** |
| Projetos pontuais | R$ 0 | 0% |

**EXCELENTE!** Receita 100% recorrente vale **2-3x mais** no valuation.

### Contratos por Tempo Indeterminado
- Todos os 80 contratos são **indeterminados**
- Previsibilidade alta
- Sem risco de não-renovação em data específica

### Diversificação Geográfica (dentro dos grupos)
O Grupo ALDO tem postos em:
- São Paulo (Cubatão, Rod. dos Imigrantes)
- Paraná (Paranaguá, São José dos Pinhais, Maringá)
- Mato Grosso (Cuiabá, Primavera, Rondonópolis, Sorriso)
- Goiás (Jataí)
- Pará (Itaituba, Barcarena)
- Maranhão (Porto Franco, São Luís)
- Bahia (Barreiras)

### Estrutura de Contratos
Padrão por posto (3 contratos):
1. **Contrato base i9 PDV** = ~R$ 3.157 ou R$ 2.929/mês
2. **Módulo adicional** = ~R$ 776/mês
3. **Serviço complementar** = ~R$ 1.434/mês

**Total por posto:** ~R$ 5.300/mês

---

## 7. RECOMENDAÇÕES ESTRATÉGICAS

### Para Negociação com Investidor

**Se o investidor for do Grupo ALDO:**
1. A concentração de 47% é um **ATIVO**, não um risco
2. Ele garante a maior parte da receita como sócio
3. Pode expandir para mais postos do grupo
4. Pode indicar outros grupos de postos

**Argumentos para manter valuation alto:**
- Receita 100% recorrente (raro no setor)
- Contratos indeterminados (estabilidade)
- Cliente conhece e confia no produto
- Potencial de expansão dentro do grupo

### Para Diversificação Futura

| Ação | Prazo | Meta |
|------|-------|------|
| Conquistar 5 novos clientes independentes | 12 meses | Reduzir concentração para < 50% |
| Lançar produto para outros segmentos | 18 meses | Diversificar base |
| Marketing para postos fora dos grupos | 6 meses | Pipeline de novos clientes |

---

## 8. CONCLUSÃO

### Diagnóstico
A i9ON tem uma **estrutura de receita excelente** (100% recorrente, contratos indeterminados), mas com **alta concentração** em dois grupos de clientes (ALDO e MIRIAN = 64% da receita).

### Impacto no Investimento

| Cenário | Valuation | Observação |
|---------|-----------|------------|
| Investidor externo | R$ 4.500.000 - R$ 5.500.000 | Desconto por concentração |
| Investidor é cliente (ALDO/MIRIAN) | R$ 6.000.000 - R$ 7.000.000 | Concentração vira vantagem |
| Investidor + contrato de 5 anos | R$ 6.500.000 - R$ 7.500.000 | Premium por garantia |

### Recomendação Final

**Para este investidor específico (cliente e parte significativa da receita):**

O modelo **Smart Money** com participação de **18-20%** continua sendo ideal, mas agora com argumento adicional:

> "Você representa parte significativa da nossa receita. Como sócio, você garante a continuidade dessa relação E participa do lucro que você ajuda a gerar."

---

*Análise elaborada em Dezembro/2024 com base nos contratos ativos fornecidos.*
