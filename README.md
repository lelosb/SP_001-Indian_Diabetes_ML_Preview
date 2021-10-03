Neste projeto temos uma base de dados de pacientes com suas características e a ocorrência ou não de diabetes. O objetivo é utilizar essa base de dados como material de estudos para treino de modelos de machine learning. Utilizaremos as características fornecidas para prever a ocorrência de diabetes em um paciente dadas as suas características.
Os dados foram retirados do site: https://www.kaggle.com/uciml/pima-indians-diabetes-database?select=diabetes.csv
Não foram encontrados valores NaN, entretanto foi observado que existiam alguns atributos que estavam preenchidos com 0, o que não fazia sentido. Insulina, Pressão arterial e outros atributos não fazem sentido tererm valores zerados. Decidiu-se por preencher esses valores com o valor médio do atributo utilizando a classe SimpleImputer do scikit learn

Foi utilizado para separação dos dados de teste e treino o pacote train_test_split
O primeiro modelo utilizado foi o GNB, Gaussian Naive Bayes

