[![author](https://img.shields.io/badge/author-lincolnneves-red.svg)](https://www.linkedin.com/in/lincolntneves/?locale=en_US) [![](https://img.shields.io/badge/python-3.7+-blue.svg)](https://www.python.org/downloads/release/python-365/)
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

O melhor modelo encontrado, foi o <b>XGBoost, apresentando 97% de acurácia</b>, acima dos demais. Contudo, o motivo por sua escolha está na avaliação dos indicadores de precisão (88%), recall (84%) e f1-score (86%), apresentando os melhores valores para previsão de cada classe da variável resposta.

Como evidências, podemos ver a matriz de confusão, apresentando boa classificação para todas as classes presentes.


<b>Matriz de Cunfusão:</b>
Predito     0   1     2    3   All
Real                              
0        5654   2    69    5  5730
1           2  17     5    1    25
2         101   1  1929   22  2053
3           1   0     8  168   177
All      5758  20  2011  196  7985


