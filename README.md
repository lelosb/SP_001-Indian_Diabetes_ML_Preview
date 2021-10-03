# Objetivo
  
  O objetivo deste projeto é utilizar uma base de dados do Kaggle para estudar a aplicação e comparação de modelos de Machine Learning. 
  
# Introdução

  Neste projeto temos uma base de dados de pacientes com algumas características coletadas e a ocorrência ou não de diabetes. Os dados foram retirados do site: https://www.kaggle.com/uciml/pima-indians-diabetes-database?select=diabetes.csv

## Desenvolvimento

  A base de dados utilizados possui 768 registros com 9 atributos. Não foram encontrados valores NaN, entretanto, entretanto foi observado que existiam alguns atributos que estavam preenchidos com 0, o que não fazia sentido. Insulina, Pressão arterial e outros atributos não fazem sentido tererm valores zerados, provavelmente por algum motivo esses valores não forma medidos e foram preenchidos com zero ("hidden NaN values"). Após uma verificação das distribuições destes atributos, decidiu-se por preencher esses valores com o valor médio do atributo utilizando a classe **SimpleImputer** do Scikit Learn antes do treinamento do modelo. Por ser um dataset muito pequeno, decidiu-se por não excluir esses registros.   Para a separação dos dados foi utilizado o pacote **train_test_split**, utilizando a proporção de 70/30.
  
  O primeiro algoritmo utilizado foi o GNB, *Gaussian Naive Bayes*, que gerou uma acurácia de 0,736, em outras palavras, o modelo conseguiu prever a ocorrência ou não de diabetes em 73,6% dos casos. Em seguida foi utilizada o algoritmo de Random Forest, que gerou uma acurácia de *0,766*. O último algoritmo utilizado foi a regressão logística, que por sua vez conseguiu uma acurácia de *0,736*, convergindo apenas para valores acima de 200 iterações.
  
  Abaixo segue um resumo dos resultados:
  
  |Algoritmo | Acurácia|
  |--- |---|
  |Gaussian Naive Bayes | 0,736|
  |Random Forest | 0,766
  |Logistic Regression | 0,736|
  
 # Conclusões
 Foram comparados alguns algoritmos de Machine Learning e escolhido um para fazer a previsão. Foi obsevada uma variação importante com a mudança dos parâmetros dos algoritmos, em especial da Random Forest, que melhorou a acurácia de 0,73 para a,76 com o aumento do número de estimadores. 
 
 # Melhorias futuras
 Criar uma função que percorra automaticamente um range de estimadores para a Random Forest
 
 Criar uma função de iterações para a regressão logística

