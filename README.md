# RH-da-IBM


Neste ficheiro irei analisar o meu dashboard dos RH da IBM.

O objetivo deste projeto foi por em prática o que aprendi e conseguir analasir uma grande quantidade de dados, os dados que extrai foi do kaggle 
(https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset?resource=download&select=WA_Fn-UseC_-HR-Employee-Attrition.csv) 
em que foram disponibilizados pela própria IBM.

Dashboard:
![Dashboard Preview](https://github.com/diogovent/RH-da-IBM/blob/main/Dashboard.png)

Caso pretenda mexer no trabalho, poderá fazê-lo através do seguinte link: https://app.powerbi.com/groups/me/reports/865a4e19-1e2d-4d82-b965-7991eb501a15/76202f17b6daa6a0a0a8?experience=power-bi

Cálculo das Médias e da Coluna:

Neste trabalho tive de criar algumas medidas, nomeadamente o número total de funcionários, 
os respetivos valores por sexo e a sua percentagem. Além disso, calculei o salário médio e o número de funcionários que fazem e que não fazem horas extra.

Tive também de criar uma nova coluna, correspondente à faixa etária dos funcionários.
Todas as medidas e a coluna foram criadas através de DAX, a linguagem de fórmulas disponibilizada pelo Power BI.

Análise dos Dados:

A força de trabalho da IBM é composta por 1470 funcionários, com uma concentração maioritária nas faixas dos 26 aos 45 anos. 
Observamos que existe certa predominancia do sexo masculino (60%) face ao sexo feminino (40%).

O salário médio é de 6.503$, sendo que as funções com um maior número de funcionários são os Sales Executive e Research Scientist,
que historicamente são posições de alto valor acrescentado e remuneração competitiva no setor tecnológico o que pode justificar o valor do salário médio.
Um dos pontos críticos e alerta é a Experiência Média de 11 anos por mais que indique uma base de conhecimento e lealdade à empresa, 
o Índice de Turnover de 16,12% é um ponto de atenção. Este valor, quando cruzado com o gráfico de Satisfação 
revela um cenário preocupante que quse 40% dos funcionário reportam uma satisfação "Baixa" ou "Moderada".

Vendo esta correlação é importante ver se esta insatisfação está relacionada a cargos especificos ou 
está relacionado ao Hora Extra (28,3%), que embora pareçam controladas podem estar a gerar um burnout em equipas críticas.

Recomendação:

É importante a empresa fazer uma análise interna e perceber o porquê do nivel de satisfação dos funcionários estar baixo e ver as possiveis alternativas que podem ser feitas para poderem aumentar a satisfação.
