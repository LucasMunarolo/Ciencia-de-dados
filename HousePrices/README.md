<h1 align="center"> PREVISÃO DE PREÇOS DE CASAS UTILIZANDO REGRESSÃO </h1>
<br><br>
O objetivo deste projeto é criar um modelo de Machine Learning, utilizando técnicas de regressão, para prever preços de casas localizadas nos Estados Unidos. 
O conjunto de dados contém diversas características dos imóveis e o preço de venda dos mesmos. O modelo utiliza estes dados para realizar a previsão dos
preços de vendas.
<br><br><br>
<h1 align="center"> Construção do projeto </h1>
<br><br>
Os dados foram extraídos do Kaggle, e já vieram separados em conjuntos de treinamento e teste. Foi feito o tratamento dos dados nulos, e conversão dos valores 
categóricos para valores numéricos, utilizando Label Encoding e One Hot Encoding. Para tentar obter um modelo mais genéricos, criei dois dataframes separados, 
um sem normalizar os dados numéricos e sem retirar os outliers da variável alvo, e o outro com os dados numéricos normalizados e retirando os outliers dos preços 
de venda.<br>
Os modelos de Machine Learning utilizados foram Linear Regression, Elastic Net (regressão linear utilizando regularizações Lasso e Ridge mescladas), 
Random Forest Regressor (um modelo de ensemble que utiliza combinações com diversas árvores de decisão) e a Support Vector Machine Regressor.<br>
As métricas para avaliar os modelos foram Mean Square Error, Root Mean Square Error, R² Score e Mean Absolute Error. Ao fazer os testes no dataframe que continha 
outliers na variável alvo, o Mean Absolute Error foi uma métrica melhor para se analisar, já que não é tão influenciada pelos outliers. Isso se comprova pelo 
fato de que o Root Mean Square Error teve valores bem altos, e o Mean Absolute Error teve valores menores. No dataframe onde foram retirados os outliers, 
o Root Mean Square Error já teve valores menores.<br>
<br><br><br>
<h1 align="center"> Conclusões </h1>
Nos dados de treinamento, o Random Forest Regressor foi o modelo que teve melhor desempenho. Nos dados de teste, apesar de nenhum modelo ter obtido um desempenho 
favorável, a Support Vector Machine e o Random Forest Regressor tiveram uma melhor performance.<br>
Devido ao baixo desempenho, tentei utilizar PCA para reduzir a dimensionalidade dos dataframes e tentar obter melhores resultados, porém esta estratégia não 
teve efeito. Uma outra possibilidade para tentar generalizar melhor seria tentar conseguir melhores hiperparâmetros para os modelos utilizando GridSearch ou RandomSearch.
