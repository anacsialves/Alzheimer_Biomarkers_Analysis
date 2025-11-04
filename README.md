# Alzheimer Biomarkers Analysis
Por Ana Carolina Sayumi Imahata Alves, João Roberto Bonardi Kniphoff da Cruz e Vitor Araújo Bairral

Este repositório foi criado para o projeto final da disciplina de Aprendizado de Máquina do curso de Bacharelado em Ciência e Tecnologia da Ilum Escola de Ciência. 
Para este trabalho, foi demandado que se obtivesse um dataset com pelo menos 1 target, 6 atributos e 200 exemplos. A partir deste dataset, deveríamos induzir modelos preditivos
a partir de modelos de aprendizado de máquina, comparando seus desempenhos. O dataset selecionado é o arquivo nomeado como Dataset_Alzheimers.csv. Este dataset contém medidas de quantidades de diferentes analitos presentes no Fluido Cerebroespinal de pacientes separados entre indivíduos com doença de Alzheimer (classificados como Impaired) e indivíduos de controle saudáveis (classificados como Control).
O dataset é resultado do estudo listado em nossas referências [1].

## Estrutura do Dataset:
Nosso conjunto de dados possui 333 linhas e 131 colunas, sendo duas colunas com dados categóricos e o restante, dados numéricos dos pacientes estudados. Dentre os dados categóricos, uma das colunas (Class) será nosso target e a outra (Genotype) fará parte do conjunto de features. Há também uma coluna que contém os índices das linhas, a qual não influenciará em nossos estudos.
Em resumo, temos um conjunto de dados com 1 target e 129 features a serem estudadas com diferentes modelos. 

## Estrutura do projeto:
Dada a estrutura do dataset, com um target categórico binário, temos em mãos um problema de classificação. Foram selecionados para teste os seguintes modelos de classificação: KNN-Classifier, NaiveBayes, RandomForest, LogisticRegression e Supported Vector Machine (SVM).

A seleção de dados de treino e teste e os devidos tratamentos de dados foram realizados separadamente e estão contidos no arquivo Tratamento_geral.ipynb. Este código divide o dataset em 4 arquivos CSV (Features para Treino.csv, Features para teste.csv, Target para treino.csv e Target para teste.csv) que serão usados pelos integrantes do grupo para alimentar os modelos a serem testados.

Cada integrante selecionou modelos de linguagem para testar. A seleção de atributos e otimização de hiperparâmetros foram de responsabilidade de cada um, uma vez que cada modelo tem sua particularidade.
Como nosso projeto objetiva a previsão da doença de pacientes, a métrica padrão utilizada para otimização de hiperparâmetros foi a métrica F1, que leva em conta a precisão e recall dos modelos, sendo a mais indicada para trabalhos deste tipo.

### Arquivos importantes:
$\cdot$ Dataset_Alzheimers.csv: é o dataset principal de nosso modelo.

$\cdot$ Features para treino.csv e Target para treino.csv: guardam as features e target que serão usadas para alimentar os modelos.

$\cdot$ Features para teste.csv e Target para teste.csv: guardam as features e target para teste e validação.

$\cdot$ Tratamento geral.ipynb: Executa o tratamento de dados eliminando colunas vazias, normalizando dados categóricos das features e realiza train-test split. Os arquivos listados nos dois itens anteriores são gerados pelo dataset. 

$\cdot$ baseline.ipynb: executa e testa um modelo baseline.

$\cdot$ Modelo_kNN.ipynb: executa e testa um Classificador k-NN.

$\cdot$ NaiveBayes.ipynb: executa e testa um modelo NaiveBayes.

$\cdot$ Regressão Logística.ipynb: Executa e testa um modelo de regressão logística. 

$\cdot$ Supported Vector Machine.ipynb: Executa e testa um modelo SVM.

$\cdot$ random_forest.ipynb: Executa e testa um modelo de floresta aleatória.
