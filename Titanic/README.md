<h1 align="center"> DESAFIO DO TITANIC UTILIZANDO CLASSIFICAÇÃO </h1>
<br><br>
O objetivo deste projeto é criar um modelo de Machine Learning, utilizando técnicas de classificação, para prever se uma pessoa sobreviveu ou não ao trágico acidente
do Titanic. Os dados fornecidos levam em conta características como idade dos passageiros, sexo, classe da passagem, e é possível verificar que existiram padrões que 
determinaram quem sobreviveu ou não ao acidente.
<br><br><br>
<h1 align="center"> Construção do projeto </h1>
<br><br>
Os dados foram extraídos do Kaggle. Após uma análise prévia dos dados, foi feito o tratamento dos dados nulos, de acordo com cada atributo, e posteriormente foi
realizada a engenharia de atributos para converter as variáveis categóricas em numéricas e para normalizar as variáveis numéricas.<br>
Foram testados os modelos Naive Bayes Gaussiano, Regressão Logística, Árvore de decisão, Florestas Aleatórias e Gradient Boosting para prever os resultados, 
utilizando a métrica de acurácia, que seria a porcentagem total de acertos do modelo. O desempenho foi avaliado pelo método de validação cruzada, onde o 
conjunto de dados foi dividido em 3 subconjuntos, o modelo aprende em um subconjunto e faz os testes nos 2 restantes.<br>
O modelo que apresentou melhor resultado nos dados de teste foi o modelo de ensemble Gradient Boosting, e portanto foi o modelo utilizado para validar o 
conjunto de testes no Kaggle.<br>
<br><br><br>
<h1 align="center"> Conclusões </h1>
O modelo utilizado obteve uma acurácia de 76,794% no conjunto de testes avaliado pelo Kaggle.
