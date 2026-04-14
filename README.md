# 👥 Análise de RH — IBM HR Analytics

# Dashboard:
![Dashboard Preview](https://github.com/diogovent/RH-da-IBM/blob/main/Dashboard.png)

# **📌 Índice**

 - Sobre o Projeto
 - Dataset
 - Tecnologias Utilizadas
 - Estrutura do Dashboard
 - Medidas DAX Criadas
 - Principais Insights
 - Recomendações
 - Como Aceder ao Dashboard

---

# **📋 Sobre o Projeto**

O objetivo deste projeto foi aplicar técnicas e conhecimentos de análise de dados sobre um conjunto de dados real 
de Recursos Humanos disponibilizado pela IBM, de forma a extrair insights acionáveis sobre a sua força de trabalho.

Este projeto abrange as seguintes áreas de análise:

 - Distribuição demográfica dos uncionários (idade, sexo e cargo)
 - Índice de Turnover e fatores associados
 - Satisfação no trabalho
 - Impacto das horas extra no bem-estar dos funcionários
 - Salário médio por função

---

# **🗂️ Dataset**

Fonte: Kaggle — IBM HR Analytics Attrition Dataset (https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset?resource=download&select=WA_Fn-UseC_-HR-Employee-Attrition.csv)

Disponibilizado por IBM

Nº de registos: 1.470 funcionários

Nº de colunas: 35 variáveis

---

# **🛠️ Tecnologias Utilizadas**

 - Power BI Desktop — construção do dashboard e modelo de dados
 - DAX (Data Analysis Expressions) — criação de medidas e colunas calculadas
 - Power Query — transformação e limpeza dos dados

---

# **📊 Estrutura do Dashboard**

| Bloco | Descrição |
|---|---|
| **KPIs Principais** | Total de Funcionários, salário médio e taxa de turnover |
| **Distribuição por Sexo** | Comparação entre género masculino e feminino |
| **Distribuição por Faixa Etária** | Agrupamento em faixas etárias criadas via DAX |
| **Distribuição por Cargo** | Funções com maior número de funcionários |
| **Satisfação no Trabalho** | Percentagem por nível (Baixa, Moderada, Alta, Muito Alta) |
| **Horas Extra** | Funcionários que realizam vs. que não realizam horas extra |

---

# **🧮 Medidas DAX Criadas e Coluna**

Abaixo estão as principais medidas e colunas calculadas desenvolvidas neste projeto:

Total de Funcionários:
```dax
   Total de Funcionários = COUNTROWS(Dados_RH)
````

Total por Sexo:
```dax
 - Total de Funcionários Masculinos = CALCULATE(COUNTROWS(Dados_RH), Dados_RH[Gender] = "Male")
 - Total de Funcionários Femeninos = CALCULATE(COUNTROWS(Dados_RH), Dados_RH[Gender] = "Female")
````

Percentagem por Sexo:
```dax
 - % de Funcionários Masculinos = DIVIDE([Total de Funcionários Masculinos],[Total de Funcionários])
 - % de Funcionários Femeninos = DIVIDE([Total de Funcionários Femeninos],[Total de Funcionários])
````

Anos Médios dentro da Empresa:
```dax
 - Experiência Média de Trabalho = AVERAGE(Dados_RH[TotalWorkingYears])
````

Salário Médio:
```dax
 - Salário Médio = AVERAGE(Dados_RH[MonthlyIncome])
````

Taxa de Turnover e %:
```dax
 - Total de Ex Funcionarios = CALCULATE(COUNTROWS(Dados_RH),Dados_RH[Attrition] = "Yes")
 - % de Ex Funcionários = DIVIDE([Total de Ex Funcionarios],[Total de Funcionários])
````

Horas Extra:
```dax
 - Hora Extra Sim = CALCULATE(COUNTROWS(Dados_RH),Dados_RH[OverTime] = "Yes")
 - Hora Extra Não = CALCULATE(COUNTROWS(Dados_RH),Dados_RH[OverTime] = "No")
````

Coluna Calculada — Faixa Etária:
```dax
 - Faixa Etaria = SWITCH(
    TRUE(),
    Dados_RH[Age] <= 17, "0-17",
    Dados_RH[Age] >= 18 && Dados_RH[Age] <= 25, "18-25",
    Dados_RH[Age] >= 26 && Dados_RH[Age] <= 35, "26-35",
    Dados_RH[Age] >= 36 && Dados_RH[Age] <= 45, "36-45",
    Dados_RH[Age] >= 46 && Dados_RH[Age] <= 55, "46-55",
    "56+"
)
````

---

# **📈 Principais Insights**

### 👥 Força de Trabalho

A IBM conta com **1.470 funcionários** ativos no dataset analisado.

A faixa etária predominante situa-se entre os **26 e os 45 anos**, representando o núcleo produtivo da empresa.
Existe uma predominância do género **masculino (≈60%)** face ao **feminino (≈40%)**.


### 💰 Remuneração

O salário médio mensal é de **$6.503**.

Os cargos com maior número de funcionários são **ales Executive** e **Research Scientist**, 
ambos historicamente associados a remunerações mais elevadas no setor tecnologia.


### 🚨 Pontos Críticos

O **Índice de Turnover é de 16,12%** — um valor acima do que é considerado saudável para o setor tecnológico (tipicamente entre 10-13%).

Quase **40% dos funcionários** reportam um nível de satisfação **"Baixo"** ou **"Moderado"**, o que é um sinal de alerta considerável.

**28,3% dos funcionários** realiza horas extra, o que pode estar a contribuir para um estado de burnout em equipas críticas.

---

# **💡 Recomendações**

Com base na análise efetuada, recomenda-se à IBM:

1. **Realizar um inquérito interno aprofundado** para identificar as causas-raiz da insatisfação, 
com especial enfoque nos departamentos com maior taxa de turnover.

2. **Rever a política de horas extra** — os 28,3% dos funcionários a fazer overtime é um valor que,
se não for monitorizado, pode acelerar o burnout e agravar o turnover.

 4. **Cruzar satisfação com cargo e antiguidade** para identificar se existe um padrão específico 
(ex: funcionários com 5-10 anos de experiência mais insatisfeitos — frequentemente o grupo mais valioso e difícil de substituir).

5. **Definir um plano de retenção** focado nas faixas etárias 26-45 anos, onde se concentra a maioria da força de trabalho.

---

# **🔗 Como Aceder ao Dashboard**

Podes interagir com o dashboard completo através do Power BI Service: https://app.powerbi.com/groups/me/reports/865a4e19-1e2d-4d82-b965-7991eb501a15/76202f17b6daa6a0a0a8?experience=power-bi

Ou então pode aceder pelo documento chamado "Projeto.pbix" que está neste repositório
