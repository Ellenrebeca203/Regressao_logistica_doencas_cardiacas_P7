# Regressao_logistica_doencas_cardiacas_P7
Projeto utilizando o modelo de classificação binária 'Regressão Logística' para prever dados da variável target 'cardio_disease'

## Objetivo do projeto
Fazer a previsão da variável target 'cardio_disease' que indica pacientes que possuem problemas cardíacos ou não, baseada em outras variáveis presentes no projeto.

## Dados do dataset
- age - idade dos pacientes
- gender - gênero (2 mulheres) (1 homens)
- height - altura dos pacientes
- weight - peso dos pacientes
- gluc - glicose
- smoke - fumante (1) não fumante (0)
- alco - consume alcool (1) não consome (0)
- active - realiza atividades fisicas (1) não realiza (0)
- cardio_disease - tem doença cardio (1) não tem (0) - Variável target

## Etapas do projeto
1. Carregamento e tratamento da base de dados:
   A base foi carregada e lida com a biblioteca do pandas, em seguida foi verificado os tipos de dados e se havia dados faltantes ou Outliers. Havia Outliers em algumas colunas que foram tratadas como 'weight' por aparentarem possíveis erros de digitação. 

2. Análise exploratória dos dados:
   Nesta etapa foram utilizados gráficos de barras e boxplot para analisar o comportamento das variáveis de maneira individual, e análise bivariada para observar o a relação delas entre si. Em seguinda foi plotada a Matriz de Correlação. 

3. Separação das bases em treino e teste 
   Foi feita a separação das bases de treino e teste através da biblioteca Sklearn, importando a classe train_test_split

4. Padronização
   Devido a natureza dos dados com escalas distantes, as features foram padronizadas com o StandardScaler.

5. Treinanento do Modelo de Regressão Logística
   Por se tratar de uma classificação binária, utilizou-se o modelo de Regressão Logística, que foi treinado com as variáveis independentes e a target.

6. Avaliação do Modelo
   Foram utilizadas as métricas de Acurácia, Recall, Precisão e F1 score para avaliar o desempenho do modelo.

## Resultado
Acurária: 0.64
AUC: 0.64

O modelo teve resultados baixos nas métricas de avaliação, isso pode se dar pela relação das variáveis entre si serem baixas. Foram testadas outras combinaçãoes de variáveis que não deram melhoria no modelo. Mas ele conseguiu generalizar bem para os novos dados de teste. 
