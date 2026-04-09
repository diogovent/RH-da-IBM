# RH-da-IBM


Neste ficheiro irei analisar o meu dashboard dos RH da IBM.

O objetivo deste projeto foi por em prática o que aprendi e conseguir analasir uma grande quantidade de dados, os dados que extrai foi do kaggle 
(https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset?resource=download&select=WA_Fn-UseC_-HR-Employee-Attrition.csv) 
em que foram disponibilizados pela própria IBM.

Dashboard:
![Dashboard Preview](https://github.com/diogovent/RH-da-IBM/blob/main/Dashboard.png)

Caso querias mexer no trabalho podes fazer acedendo a este link: https://app.powerbi.com/groups/me/reports/865a4e19-1e2d-4d82-b965-7991eb501a15/76202f17b6daa6a0a0a8?experience=power-bi

Cálculo das Medias e da Coluna:
Neste trabalho tive de criar algumas medidas, nomeadamente o número total de funcionários, 
os respetivos valores por sexo e a sua percentagem. Além disso, calculei o salário médio e o número de funcionários que fazem e que não fazem horas extra.
Tive também de criar uma nova coluna, correspondente à faixa etária dos funcionários.
Todas as medidas e a coluna foram criadas através de DAX, a linguagem de fórmulas disponibilizada pelo Power BI.

Análise dos Dados:
Em relação aos dados, podemos verificar que, no momento em que a IBM disponibilizou a informação, 
existiam cerca de 1470 funcionários, sendo que 60% eram do sexo masculino e os restantes 40% do sexo feminino.
Os dois maiores grupos na faixa etária são os de 26-35 anos e 36-45 anos. Também se pode observar que o salário médio dos trabalhadores ronda os 6.503 $.

Pelo dashboard, nota-se que a IBM apresenta uma boa retenção de colaboradores ao longo do tempo, 
o que é visível através de uma experiência média de cerca de 11 anos. Isto indica que, em média, 
os trabalhadores permanecem vários anos na empresa. Por outro lado, o índice de turnover é de 16,12%, 
o que significa que 16,12% dos funcionários decidiram sair da empresa.

No gráfico da satisfação no trabalho, verifica-se que 61,29% dos colaboradores estão satisfeitos com o seu trabalho, 
enquanto os restantes, que representam cerca de 40%, não estão satisfeitos. Este resultado deve ser visto como um ponto de atenção.

No gráfico da proporção de funcionários com horas extra, observa-se que cerca de 28,3% realizam horas extra. 
Este valor é relativamente baixo, o que pode ser interpretado de forma positiva, dependendo da política interna da empresa e da área em análise.

Por fim, os três cargos com maior número de trabalhadores são Sales Executive, Research Scientist e Laboratory Technician. 
Os dois primeiros, em empresas de grande dimensão e do setor em que a IBM atua, tendem frequentemente a estar associados 
a salários mais elevados, o que pode ajudar a explicar o valor do salário médio observado.
