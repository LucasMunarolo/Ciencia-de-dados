<h1 align="center"> PREVISÃO DE PREÇOS DE CASAS UTILIZANDO REGRESSÃO </h1>
<br><br>
O objetivo deste projeto é criar um modelo de Machine Learning, utilizando técnicas de regressão, para prever preços de casas localizadas na cidade de Ames, Iowa,
nos Estados Unidos. 
O conjunto de dados contém diversas características dos imóveis e o preço de venda dos mesmos. O modelo utiliza estes dados para realizar a previsão dos
preços de vendas.
<br><br><br>
<h1 align="center"> Construção do projeto </h1>
<br><br>
Os dados foram extraídos do Kaggle, e já vieram separados em conjuntos de treinamento e teste. Foi feito o tratamento dos dados nulos, e conversão dos valores 
categóricos para valores numéricos, utilizando Label Encoding e One Hot Encoding.<br> 
Por ser uma base de dados com muitos atributos, utilizei algumas técnicas de seleção de atributos para utilizar apenas os 30 mais importantes. Primeiramente,
utizei Variance Threshold para excluir os modelos em que uma mesma variável estava presente em 80% ou mais das amostras. Após a exclusão destas colunas, utilizei
SelectKBest para selecionar os 30 atributos com maior contribuição, utilizando o critério f_regression, que calcula a relação de cada variável independente com a
variável dependente em um modelo de regressão.<br>
Os modelos de Machine Learning utilizados foram Linear Regression, Lasso Regression, Ridge Regression, Elastic Net (regressão linear utilizando regularizações Lasso e 
Ridge mescladas), Support Vector Machine Regressor, e os modelos de ensemble Random Forest Regressor e Gradient Boosting Regressor.<br>
As métricas para avaliar os modelos foram Mean Square Error, Root Mean Square Error, R² Score e Mean Absolute Error. Para cada modelo, também utilizei a média
do resultado de Mean Squared Error e Root Mean Squared Error em uma validação cruzada utilizando 5 repartições da base de dados de treinamento.<br>
<br><br><br>
<h1 align="center"> Conclusões </h1>
O modelo que melhor generalizou nos dados desconhecidos, foi o Gradient Boosting Regressor. Tentei utilizar Random Seach para conseguir melhor hiperparâmetros para o
modelo, pensando em um resultado melhor, porém de acordo com a métrica de avaliação do Kaggle, o modelo com os hiperparâmetros padrões obteve melhor desempenho.<br>
O desafio do Kaggle é avaliado pela Root Mean Squared Error do log dos dados previstos em relação ao log dos preços de vendas reais e, através desta métrica, o 
modelo obteve um resultado de 0.14642.
