<h1 align="center"> NAVE ESPACIAL TITANIC - DESAFIO KAGGLE </h1>
<br><br>
Similar ao desafio do Titanic no Kaggle, o Spaceship Titanic consiste em uma nave espacial que transporta aproximadamente 13000 passageiros, saindo do nosso sistema
solar e indo para três exoplanetas habitáveis que orbitam estrelas próximas. Ao se chocar com uma anomalia no espaço, alguns passageiros foram transportados para uma 
dimensão alternativa. O objetivo do desafio é prever quais passageiros foram transportados para esta dimensão alternativa, utilizando um modelo de Machine Learning de 
classificação.
<br><br><br>
<h1 align="center"> Construção do projeto </h1>
<br><br>
Os dados vieram separados em amostras de treino e de teste e foram extraídos do Kaggle. Os atributos são planeta natal, Id do passageiro, cabine, destino, idade, 
se o passageiro é VIP, gastos do passageiro em diversos luxos da nave espacial e nome do passageiro.<br>
No Id do passageiro, utilizei str.split do pandas para extrair o grupo do passageiro, o que foi informado no desafio que a maioria dos passageiros do mesmo grupo 
constituíam uma família, o que pode indicar alguns padrões. No caso da cabine, utilizei o mesmo comando para extrair o Deck, o lado da cabine e o número em si da cabine, 
como também informado pelo Kaggle.<br>
Após este procedimento, foi feita uma análise de cada atributo, e através desta análise foram substituídos os dados nulos. Posteriormente, fiz a padronização das colunas
numéricas, e converti as colunas categóricas em numéricas utilizando get_dummies do pandas.<br>
Na criação dos modelos de Machine Learning, utilizei para testes a Regrssão Logística, Naive Bayes, Árvore de decisão, e os modelos de ensemble Gradient Boosting, 
Florestas Aleatórias e Ada Boost. As métricas utilizadas para avaliar os modelos foram acurácia e matriz de confusão. Para validar o modelo em dados desconhecidos, 
utilizei o método de validação cruzada, criando 10 subconjuntos de treino e teste.
<br><br><br>
<h1 align="center"> Conclusões </h1>
O modelo que obteve melhores resultados nos dados de teste foi a Regressão Logística. Ao enviar as previsões dos dados de teste para avaliação do modelo pelo Kaggle, 
obtive um resultado de 78,746% de acurácia.
