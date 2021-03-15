## Identificando o tipo de hospedagem no Airbnb com modelos de classificação

O objetivo desse projeto é identificar o tipo hospedagem publicada no site da empresa Airbnb, na cidade do Rio de Janeiro, Brasil, utilizando modelos de classificação. A base de dados utilzada pode ser encontrada na página de dados da empresa, clicando [aqui](http://insideairbnb.com/get-the-data.html).

Para modelagem, foram utilizados cinco técnicas de Machine Learning:
- Supervised Vector Machine (SVM)
- Árvore de Decisão
- Naive Bayes
- Random Forest
- XGBoost

Esse projeto está dividido em três partes:
- Parte 01: Ajuste em variáveis para fazerem parte dos modelos
- Parte 02: Utilizando algoritmo de feature selection para escolha de variáveis
- Parte 03: Rodando os modelos e comparando os resultados

A estratégia de modelagem foi baseada em testar diferentes modelos, com as features mais representativas, tanto as quantitativas quanto as qualitativas. Para executar a modelagem, os dados categóricos foram transformados em variáveis binárias, utilizando a função OneHotEncoder, do Sklearn e, após a base pronta com as variáveis, as mesmas foram normalizdas utilizando StandardScaler, também do Sklearn.

O melhor modelo encontrado, foi o <b>XGBoost, apresentando 97% de acurácia</b>, acima dos demais. Contudo, o motivo por sua escolha está na avaliação dos indicadores de precisão, recall e f1-score, apresentando os melhores valores para previsão de cada classe da variável resposta.

