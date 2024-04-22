## Avaliação Riso de Credito

#### Uma instituição financeira acompanha periodicamente o indicador de inadimplência dos produtos financeiros e tem verificado o aumento expressivo desta taxa para o produto empréstimo, no último ano. Por mais que não pagamento gere um valor de “empréstimo” que possa gerar receita futura (devido a taxa de juros) para a instituição, parte do dinheiro pode não ser recuperada. Portanto, traçar estratégias de relacionamento, crédito e cobrança são necessários para controlar a taxa de inadimplência. Assim, a área de Empréstimos, solicitou a construção de um modelo preditivo para o produto com o objetivo de identificar o perfil dos clientes PF inadimplentes. Como a quantidade de clientes é grande e o custo de comunicação é limitado, o modelo auxiliará a instituição financeira a trabalhar de forma otimizada com seus clientes. O modelo deve ter boas taxas de acurárica, sensibilidade e especificidade (mínimo de 70%).
## Criterio utilizado para constução do projeto: Cross Industry Standard Process for Data Mining (CRISP-DM)

#### CRISP-DM é a abreviação de Cross Industry Standard Process for Data Mining, que pode ser traduzido como Processo Padrão Inter-Indústrias para Mineração de Dados. Desempenha um papel crucial no cenário empresarial moderno, permitindo que as organizações tomem decisões embasadas e obtenham insights valiosos. Nesse contexto, a metodologia CRISP-DM tem se destacado como uma estrutura robusta para abordar projetos de ciência de dados.

## Etapas da CRIPS-DM

#### 1 - Compreensão do Negócio (Business Understanding) Antes de iniciar um projeto de ciência de dados, é essencial compreender o contexto e os objetivos do negócio. Nesta fase, definimos claramente as metas do projeto e as alinhamos aos objetivos estratégicos da organização;

#### 2 - Compreensão dos Dados (Data Understanding) Coletar dados relevantes é fundamental para o sucesso do projeto. Nessa fase, exploramos e nos familiarizamos com os dados disponíveis, identificamos lacunas e problemas potenciais, e avaliamos a qualidade e a adequação dos dados para o projeto;

#### 3 - Preparação dos Dados (Data Preparation) Os dados brutos raramente estão prontos para a análise. Nesta fase, realizamos a limpeza dos dados, tratamos valores ausentes ou inconsistentes e integramos diferentes fontes de dados. O objetivo é criar um conjunto de dados preparado para as etapas subsequentes;

#### 4 - Modelagem (Modeling) A fase de modelagem envolve a aplicação de técnicas e algoritmos de modelagem de dados aos dados preparados. Selecionamos as técnicas mais adequadas, como regressão, classificação ou agrupamento, e ajustamos e avaliamos os modelos para garantir sua precisão e eficácia;

#### 5 - Avaliação (Evaluation) A avaliação dos modelos desenvolvidos é crucial para medir sua qualidade e desempenho. Nesta fase, utilizamos métodos como validação cruzada e métricas de desempenho para avaliar o quão bem os modelos se saem em dados não vistos. Com base nessa avaliação, podemos ajustar e aprimorar os modelos, se necessário;

#### 6 - Implantação (Deployment) A fase final da metodologia CRISP-DM é a implantação do modelo em um ambiente de produção. Integramos o modelo aos sistemas existentes, monitoramos seu desempenho contínuo e garantimos a adoção pela equipe de negócios.

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/e2cd3dbc-6a95-47d5-87df-130bd0b409d8.png" width="700px" height="300px" />
</div>

## Inciando o projeto

## 1 - Compreensão do Negócio (Business Understanding)

#### O objetivo do trabalho é predizer e avaliar o risco de empréstimo de clientes PF (Pessoa Física) de uma instituição financeira. A predição será realizada utilizando dados históricos transacionais e modelos estatísticos e algoritmos de Inteligência Artificial, que selecionarão as características mais relevantes que explicam a justificativa de empréstimo ou não empréstimo. Desta forma, a empresa poderá traçar estratégias financeiras, desenvolver réguas de empréstimos e ações preventivas para minimizar de forma proativa sua taxa de inadimplência de empréstimos.

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/eddb0d7d-28df-4acf-93fd-c3280934083b.png" width="700px" />
</div>

## 2 - Compreensão dos Dados (Data Understanding)

### Base de dados

#### Considerando dados históricos provenientes de um banco, referentes a 5.000 clientes que solicitaram empréstimos financeiros. A base contém informações como idade, tempo de residência no endereço atual, renda etc., além da variável resposta Classif, que indica se cada clientes foi um bom pagador (1) ou um mau pagador (0). Deseja-se avaliar o potencial dessas variáveis para predizer se novos clientes serão bons ou maus pagadores. 

### Dicionário de dados

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/b5f92e35-6fff-4c41-8eeb-5eeaa4de2467.png" width="700px" />
</div>

### Análise exploratória de dados (AED) 

#### A análise exploratória de dados (AED) é o uso de ferramentas para examinar determinado conjunto de dados antes mesmo da aplicação de qualquer técnica estatística para tirar conclusões sobre eles. É uma maneira de obter um entendimento prévio sobre os dados disponíveis para um estudo e das variáveis que eles envolvem. <br>
#### Depois que os dados são coletados e armazenados em um banco de dados, a análise descritiva é o primeiro passo dentro do AED. Nessa etapa, os pesquisadores se familiarizam e organizam esses dados de forma sintetizada para saber que tipo de informações podem ser tiradas deles.
#### Dito de outra forma, antes de realizar uma análise exploratória de dados, temos que preparar esses dados para que se tornem analisáveis. Há um conjunto de tarefas envolvido nesse processo:

#### Identificar quais são as variáveis envolvidas e como elas se relacionam;

#### Identificar os chamados outliers, casos de exceção que não seguem uma tendência muito diferente da maior parte da amostra analisada;

#### Verificar se há dados ausentes;

#### Fazer algumas suposições preliminares sobre as tendências que esses dados demonstram, como normalidade e linearidade.

#### Esse é o processo que acontece nos bastidores de um sistema voltado para Business Intelligence (BI), que é a análise de dados críticos para ajudar os gestores de uma empresa a tomarem as melhores decisões. 

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/03489886-6784-4813-b73d-1422257f51b8.png" width="350px" />
</div>

## Pacotes e Biblioteca

### Mapear diretorio onde esta salvo a base de dados

````
setwd("inserir directorio do arquivo"") # Ou Ctrl + Shift + H
````

### Pacotes necessários

````
install.packages("readxl")             # Para leitura de dados Excel
install.packages("Information")        # Para calculo IV
install.packages("car")                # Para analise de regressao e diagnostico de modelos 
install.packages("cutpointr")          # Para calculo ponto de corte		
install.packages("dplyr")              # Para manipulacao e transformacao dados
install.packages("psych")              # Para analise psicometrica e estatisitca
install.packages("C50")                # Decision Tree com algoritmo C50
install.packages("gmodels")            # Para matriz de contigencia (C50)
install.packages("GGally")             # Correlograma
install.packages("caret")              # Para treino de classificacao e regressao
install.packages("e1071")              # Para matriz de contigencia
install.packages("pROC")               # Para plotar curva ROC
````
### Bibliotecas necessárias

````
library(readxl)				
library(Information)				
library(car)				
library(cutpointr)				
library(dplyr)
library(psych)
library(C50)
library(gmodels)
library(GGally)
library(caret)
library(e1071)
library(pROC)
library(ggplot2)
````
### Retirar a notação científica

````
options(scipen = 999) 				
````

### Leitura da base de dados

````
emprestimo <- read_excel("Regressao logistica.xlsx", sheet = "Emprestimo - Dados")							
````

### Cabeçalho (Head)

````
head(emprestimo, 15) # Cabecalho contento as 15 primeiras linhas do dataframe
````

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/73db7a4d-a3e8-47c4-8b44-b4d6de0d1c69.png" width="700px" />
</div>

### Calda (Tail)

````
tail(emprestimo, 15) # Calda contento as 15 ultimas linhas do dataframe
````

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/d42a2af9-f020-4871-b9a0-2b0c3832ca37.png" width="700px" />
</div>

### Medidas resumo

````
summary(emprestimo[,-1]) # Medidas de posicao 
````
<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/e3645e0e-edf2-42fe-82c5-75a93bbdcd3e.png" width="700px" />
</div>

````
describe(emprestimo[,-1]) # Medidas de dispersao
````
<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/a1a6cdc2-37e5-4f55-b81e-3a476583eae7.png" width="700px" />
</div>
````
par(mfrow = c(2, 3)) # Inserir 2 graficos na mesma tela	
boxplot(Idade ~ Classif, data = emprestimo, col = "darkturquoise", main = "Boxplot Idade") # Idade x Classif					
boxplot(Tempo_Experiencia ~ Classif, data = emprestimo, col = "darkturquoise", main = "Boxplot Tempo_Experiencia") # Tempo_Experiencia x Classif
boxplot(Tempo_Endereco ~ Classif, data = emprestimo, col = "darkturquoise", main = "Boxplot Tempo_Endereco") # Tempo_Endereco x Classif
boxplot(Renda ~ Classif, data = emprestimo, col = "darkturquoise", main = "Boxplot Renda") # Renda x Classif
boxplot(Debito_Renda ~ Classif, data = emprestimo, col = "darkturquoise", main = "Boxplot Debito_Renda") # Debito_Renda x Classif
boxplot(Variacao_Debito ~ Classif, data = emprestimo, col = "darkturquoise", main = "Boxplot Variacao_Debito") # Variacao_Debito x Classif
````

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/31158540-b491-4f10-af10-d06fa72d2f88.png" width="700px" />
</div>

#### Análise:
#### Analisando os dados dos boxplot das variáveis demograficas (explicativa) x variável resposta Classif, pode-se observar que a variável Debito_Renda apresenta uma relação com variável Classif devido a disparidade entre os “0” e “1”, o que pode ser idicativo de algum poder preditivo. 

### Análise exploratória de dados - Bivariada com information value (IV)

#### O Valor da Informação, ou Information Value (IV), é um indicador que mensura a força da relação entre duas variáveis, sejam elas numéricas ou categóricas. No contexto da regressão logística, o IV é calculado entre as variáveis explicativas versus a variável resposta (binária) na fase de análise bivariada, sendo útil para realizar uma avaliação prévia de quais variáveis explicativas têm maior potencial de discriminação para a posterior construção de um modelo. Quanto maior o valor do IV, maior o grau de explicabilidade da variável explicativa sobre a resposta. Em grande parte das situações práticas, seu valor varia entre 0 a 0,5, ainda que possa assumir quaisquer valores positivos. 

````
IV <- create_infotables(data = emprestimo[,c(2:8)], y = "Classif") # Information Value - library("information")
IV$Summary	
````
<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/955b1939-2fc1-4336-a5ae-f2c6d838b85e.png" width="700px" />
</div>

#### Análise:
#### Fazendo um segunda verificação com a técnica information value, a variável Debito_Renda parece ter maior grau de explicabilidade sobre a variável resposta, sugere-se que essa variável possa tem alguma relevância para distinguir os bons e maus pagadores. 

<ul>
  <li> Existe alguma correlação entre a idade dos clientes e sua classificação como bons ou maus pagadores? 
       Investigar se a idade está relacionada à probabilidade de ser um bom pagador. 
</ul>

### Boxplot e histograma - Idade

````
par(mfrow = c(1,2)) # Inserir 2 graficos na mesma tela
boxplot(emprestimo$Idade, col = "darkturquoise", main = "Boxplot Idade") # Bloxplot Idade
hist(emprestimo$Idade, main = "Histograma Idade", col = "darkturquoise", ylab = "Frequencia", xlab = "Idade") # Histograma Idade
````
<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/2931ea1b-94de-4b38-89af-8cc26b9a792f.png" width="600px" />
</div>

#### Análise: 
#### Analisando os dados do boxplot da variável Idade, pode-se observar poucos valores discrepantes (outliers), onde os dados indicam que, para uma base de 5.000 clientes 25% tem menos de 37 anos e idade média de 48 anos. Já analisando os dados do histograma, pode-se observar que a distribuição tende à “normal”, onde 65,56% dos clientes tem idades entre 28 e 55 anos aproximadamente, que são representas pelas maiores porções do gráfico.

### Boxplot e histograma - Tempo_Experiencia

````
par(mfrow = c(1,2))	# Inserir 2 graficos na mesma tela
boxplot(emprestimo$Tempo_Experiencia, col = "red", main = "Boxplot Tempo_Experiencia") # Boxplot Tempo_Experiencia
hist(emprestimo$Tempo_Experiencia, main = "Histograma Tempo_Experiencia", col = "red", ylab = "Frequencia", xlab = "Tempo_Experiencia") # Histograma Tempo_Experiencia
````

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/a4e1ab92-52d0-496d-9418-588fa840a42d.png" width="600px" />
</div>

#### Análise: 
#### Analisando os dados do boxplot da variável Tempo_Experiencia, pode-se observar a ausência valores descrepantes (outliers), onde os dados indicam que, para uma base de 5.000 clientes 75% tem menos de 22 de experiência e média de 14 anos. Já analisando os dados do histograma, pode-se observar que a distribuição é assimétrica à direita, onde 54,94% dos clientes tem tempo de experiência entre 0 e 13 anos aproximadamente, que são representas pelas maiores porções do gráfico.

### Boxplot e histograma - Tempo_Experiencia

````
par(mfrow = c(1,2))	
boxplot(emprestimo$Tempo_Endereco, col = "green", main = "Boxplot Tempo_Endereco") # Boxplot Tempo Endereco
hist(emprestimo$Tempo_Endereco, main = "Histograma Tempo_Endereco", col = "green", ylab = "Frequencia", xlab = "Tempo_Endereco") # Histograma Tempo_Endereco
````

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/2b0654ef-6481-4f64-8442-ec106bbd5ca6.png" width="600px" />
</div>

#### Análise: 
#### Analisando os dados do boxplot da variável Tempo_Endereco, pode-se observar poucos valores outliers (2,56%), onde os dados indicam que, para uma base de 5.000 clientes 25% tem menos de 3 de tempo endereço e média de 8,2 anos. Já analisando os dados do histograma, pode-se observar que a distribuição é assimétrica à direita, onde 67,76% dos clientes tem tempo de residência entre 0 e 10,2 anos aproximadamente, que são capturadas pelas maiores porções do gráfico.

### Boxplot e histograma - Renda

````
par(mfrow = c(1,2)) # Inserir 2 graficos na mesma tela
boxplot(emprestimo$Renda, col = "darkblue", main = "Boxplot Renda") # Boxplot Renda
hist(emprestimo$Renda, main = "Histograma Renda", col = "darkblue", ylab = "Frequencia", xlab = "Renda") # Histograma Renda
````

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/b4c5abae-c925-467e-a21e-7948430d68a0.png" width="600px" />
</div>

#### Análise: 
#### Analisando os dados do boxplot da variável Renda, pode-se observar poucos valores outliers (0,42%), onde os dados indicam que, para uma base de 5.000 clientes 75% ganham menos de 4,6 salários mínimos e média de 3,9. Já analisando os dados do histograma, pode-se observar que a distribuição é assimétrica à direita, onde 60,5% dos clientes tem rendas entre 1,8 e 4,6 salários aproximadamente, que é capturada pela maior porção do gráfico.
#### Extra: De acordo com a base de dados, apenas 0,42% da população tem renda entre 21,3 e 38 salários mínimos, que representa (ou tende a representar) a desigualdade de renda existente no País.

### Boxplot e histograma - Debito_Renda

````
par(mfrow = c(1,2)) # Inserir 2 graficos na mesma tela
boxplot(emprestimo$Debito_Renda, col = "yellow", main = "Boxplot Debito_Renda") # Boxplot Debito_Renda
hist(emprestimo$Debito_Renda, main = "Histograma Debito_Renda", col = "yellow", ylab = "Frequencia", xlab = "Debito_Renda") # Histograma Debito_Renda
````

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/b345178a-38a8-45ed-b721-1baaac77580b.png" width="600px" />
</div>

#### Análise: 
#### Analisando os dados do boxplot da variável Debito_Renda, pode-se observar poucos valores outliers (0,6%), onde os dados indicam que, para uma base de 5.000 clientes 25% tem débitos de 5 salários em relação a renda atual e média de 10. Já analisando os dados do histograma, pode-se observar que a distribuição é assimétrica à direita, onde 52,8% dos clientes tem débitos em relação a renda entre 0,08 e 12,9 aproximadamente, que são capturadas pelas maiores porções do gráfico.

### Boxplot e histograma - Variacao_Debito

````
par(mfrow = c(1,2)) # Inserir 2 graficos na mesma tela
boxplot(emprestimo$Variacao_Debito, col = "darkgrey", main = "Boxplot Variacao_Debito") # Boxplot Variacao_Debito
hist(emprestimo$Variacao_Debito, main = "Histograma Variacao_Debito", col = "darkgrey", ylab = "Frequencia", xlab = "Variacao_Debito") # Histograma Variacao_Debito
````

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/2e0896e1-3270-491c-ae63-9b702388453e.png" width="600px" />
</div>

#### Análise: 
#### Analisando os dados do boxplot da variável Variacao_Debito, pode-se observar valores outliers (11,9%), onde os dados indicam que, para uma base de 5.000 clientes 75% tem variações de 0,17 em relação a 6 meses atrás e média de -0,43. Já analisando os dados do histograma, pode-se observar que a distribuição é assimétrica à direita, onde 88,1% dos clientes tem variações de debito em relação a 6 meses atrás entre -1 e 1,57 aproximadamente, que são capturadas pelas maiores porções do gráfico.

### Analise exploratória dos dados - Bivariada

````
par(mfrow = c(2, 3)) # Inserir 2 graficos na mesma tela	
boxplot(Idade ~ Classif, data = emprestimo, col = "darkturquoise", main = "Boxplot Idade") # Idade x Classif					
boxplot(Tempo_Experiencia ~ Classif, data = emprestimo, col = "red", main = "Boxplot Tempo_Experiencia") # Tempo_Experiencia x Classif
boxplot(Tempo_Endereco ~ Classif, data = emprestimo, col = "green", main = "Boxplot Tempo_Endereco") # Tempo_Endereco x Classif
boxplot(Renda ~ Classif, data = emprestimo, col = "darkblue", main = "Boxplot Renda") # Renda x Classif
boxplot(Debito_Renda ~ Classif, data = emprestimo, col = "yellow", main = "Boxplot Debito_Renda") # Debito_Renda x Classif
boxplot(Variacao_Debito ~ Classif, data = emprestimo, col = "darkgrey", main = "Boxplot Variacao_Debito") # Variacao_Debito x Classif
````

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/dbe4180b-814f-4f71-9df7-33454f1c60ff.png" width="600px" />
</div>

#### Análise: 
#### Analisando os dados do boxplot da variável explicativa Debtio_Renda x variável resposta Classif, pode-se observar uma relação entre essas variáveis devido a disparidade entre os “0” e “1”.

### Analise exploratória dos dados - Bivariada com Information Value (IV)

#### O Valor da Informação, ou Information Value (IV), é um indicador que mensura a força da relação entre duas variáveis, sejam elas numéricas ou categóricas. No contexto da regressão logística, o IV é calculado entre as variáveis explicativas versus a variável resposta (binária) na fase de análise bivariada, sendo útil para realizar uma avaliação prévia de quais variáveis explicativas têm maior potencial de discriminação para a posterior construção de um modelo. Quanto maior o valor do IV, maior o grau de explicabilidade da variável explicativa sobre a resposta. Em grande parte das situações práticas, seu valor varia entre 0 a 0,5, ainda que possa assumir quaisquer valores positivos. 

````
IV <- create_infotables(data = emprestimo[,c(2:8)], y = "Classif") # Information Value - library("information")
IV$Summary	
````
<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/955b1939-2fc1-4336-a5ae-f2c6d838b85e.png" width="600px" />
</div>

#### Análise: 
#### Analisando os dados, a variável Debito_Renda parece ter maior grau de explicabilidade sobre a variável resposta.

### Analise exploratoria dos dados - Bivariada com Correlograma
````
# Analise exploratoria dos dados - Correlograma
ggpairs(emprestimo[,c(2:8)], title="Correlograma") # Correlograma - library(GGally) 				
````
<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/6d8d9b69-51f9-46f6-84d1-ec36c2108f14.png" width="600px" />
</div>

#### Análise: 
#### Analisando os dados correlograma, a variável Debito_Renda parece ter maior grau de explicabilidade (apesar do baixo nível de correlação -0,379) sobre a variável resposta. As demais variávies apresentam baixos níveis de correlação.

## 3 - Preparação dos Dados (Data Preparation)

### Pré-processamento 

#### É uma etapa crucial no desenvolvimento de modelos de machine learning, pois influencia diretamente na qualidade e no desempenho do modelo. Ele envolve uma série de técnicas e procedimentos aplicados aos dados brutos antes de serem alimentados ao algoritmo de machine learning. 

### Normalização e Padronização:

#### A normalização e padronização dos dados são técnicas comuns de pré-processamento que colocam todas as variáveis em uma escala comparável, evitando que alguma variável domine sobre as outras, o que é especialmente importante em algoritmos sensíveis à escala.

````
# Pre-Processamento - Transformando variável resposta "Classif" para factor
emprestimo$Classif <- as.factor(emprestimo$Classif)
````

````
# Pre-Processamento - Normalização das variáveis numéricas
dados_treino[, c("Idade", "Tempo_Experiencia", "Tempo_Endereco", "Renda", "Debito_Renda", "Variacao_Debito")] <- scale(dados_treino[, c("Idade", "Tempo_Experiencia", "Tempo_Endereco", "Renda", "Debito_Renda", "Variacao_Debito")])
dados_teste[, c("Idade", "Tempo_Experiencia", "Tempo_Endereco", "Renda", "Debito_Renda", "Variacao_Debito")] <- scale(dados_teste[, c("Idade", "Tempo_Experiencia", "Tempo_Endereco", "Renda", "Debito_Renda", "Variacao_Debito")])
````

## 4 - Modelagem (Modeling)

### Modelagem com Machine Learning - Regressão logística (RStudio)

#### A Regressão logística é um modelo de aprendizado de máquina que é comumente utilizado para problemas de classificação binária. Apesar do nome "regressão", esse modelo é usado para prever a probabilidade de um evento pertencer a uma das duas classes (por exemplo, sim ou não, 1 ou 0).

#### A Regressão logística é particularmente útil quando a variável de saída é categórica e binária. Ela estima a probabilidade de uma instância pertencer a uma classe específica com base em uma combinação linear de variáveis independentes. A função logística (também chamada de função sigmoid) é utilizada para transformar a saída linear em uma probabilidade entre 0 e 1.

### Divisão da base para treino e teste

#### A divisão de dados em conjuntos de treinamento e teste é uma prática comum em Machine Learning. O objetivo é avaliar a capacidade do modelo de generalizar para novos dados que não foram usados no treinamento. A ideia é treinar o modelo em um conjunto de dados de treinamento e avaliar seu desempenho em um conjunto de dados de teste. O conjunto de treinamento é usado para ajustar os parâmetros do modelo, enquanto o conjunto de teste é usado para avaliar o desempenho do modelo em dados não vistos. A divisão dos dados em conjuntos de treinamento e teste ajuda a evitar o overfitting, que ocorre quando o modelo se ajusta demais aos dados de treinamento e não generaliza bem para novos dados.

````
# Dividindo os dados em conjuntos de treinamento e teste (80% treinamento, 20% teste)
set.seed(123)  # Define uma semente para reproducibilidade
indices_treino <- createDataPartition(emprestimo$Classif, p = 0.8, list = FALSE)
dados_treino <- emprestimo[indices_treino, ]
dados_teste <- emprestimo[-indices_treino, ]
````

### Criando modelo de Regressão logística

````
# Modelagem com Machine Learning - Regressao logistica
regressao_log <- glm(Classif ~ Idade + 
                       Tempo_Experiencia + 
                       Tempo_Endereco + 
                       Renda + 
                       Debito_Renda +
                       Variacao_Debito, 
                       binomial(link = "logit"), 
                       data = dados_treino)
summary(regressao_log)
````

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/eaa28942-4d2b-4508-85a0-895f0df3623c.png" width="600px" />
</div>

### Selecionando as melhores variáveis

````
# Feature Selection - Selecionando as melhores variáveis
formula <- "Classif ~ Idade + Tempo_Experiencia + Tempo_Endereco + Renda + Debito_Renda + Variacao_Debito"
formula <- as.formula(formula)
control <- trainControl(method = "repeatedcv", number = 10, repeats = 2)
model <- train(formula, data = dados_treino, method = "glm", trControl = control)
importance <- varImp(model, scale = FALSE)
plot(importance)
````

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/bcfd6127-f1d8-4a24-842e-e4cf346f7dfe.png" width="600px" />
</div>

#### No processo de construção do modelo deve-se retirar, a cada passo, a variável com menor significância estatística. Como estamos adotando 95% de confiança, deve-se retirar variáveis cujo p-valor seja maior do que 5%. Esse procedimento é conhecido como Stepwise.

#### A variável explicativa Tempo_Experiencia apresenta p-valor acima de 5%. Logo, não é um aspecto estatisticamente significativo para explicar a decisão de conceder empréstimo e deve ser retirado para melhor ajuste do modelo. 

````
# Modelagem com Machine Learning - Regressao logisttica - Retirando variável Tempo_Experiencia 
regressao_log <- glm(Classif ~ Idade + 
                       Tempo_Endereco + 
                       Renda + 
                       Debito_Renda +
                       Variacao_Debito, 
                       binomial(link = "logit"), 
                       data = dados_treino)
summary(regressao_log)
````

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/972df4fc-78a9-4e26-a960-d9989133c0a6.png" width="600px" />
</div>

#### Análise:
#### Analisando os p-valores obtidos pelo modelo, consegue-se estatisticamente sustentar são as variáveis Debito_Renda, Tempo_Endereco, Variacao_Debito e Renda são variáveis significativas, adotando um nível de confiança de 95%. Logo, são aspectos estatisticamente significativos para explicar a decisão de conceder empréstimo, e devem ser mantidos no modelo.

### Cálculo das estimativas

#### Tendo em vista que todas as variáveis são importantes, pode-se calcular a probabilidade final de uma pessoa ser inadimplente de forma consistente da seguinte forma:

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/1b3cdaf1-9637-41bc-a483-fa537417e59c.png" width="600px" />
</div>

### Estatística VIF - Verificando Multicolinearidade

#### Quando lidamos com uma regressão múltipla, ou seja, com 2 ou mais variáveis explicativas, algumas delas podem representar informações muito similares. Esse tipo de redundância, no contexto de análise de regressão, é denominado multicolinearidade. 

#### A multicolinearidade ocorre quando variáveis explicativas fortemente associadas entre si são consideradas no mesmo modelo de regressão, seja linear ou logística. 

#### A redundância de informação eleva potencialmente o nível de variabilidade dos parâmetros estimados (betas) associados às variáveis correlacionadas, distorcendo a sua interpretação. Isso torna o modelo instável e, muitas vezes, compromete a sua utilização para predições futuras.

#### A estatística VIF (Variance Inflation Factor, ou Fator de Inflação da Variância) mensura o quanto a variância de cada coeficiente estimado do modelo está sendo inflacionada por conta de multicolinearidade. A partir de estudos anteriores, valores de VIF superiores a 4 já revelam sinais de multicolinearidade. 	

````
# Verificando multicolinearidade no modelo final - Variance Inflator Factor (Estatistica VIF)								
vif(regressao_log)
````

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/b2634bdc-4524-4746-aa95-7b5696da6244.png" width="700px" />
</div>

#### Análise: 
#### Interpretatando os dados se saída, não há evidencias claras de multicolinearidade no modelo, pois todos os valores foram menores que 4, podendo seguir com as próximas etapas.

### Fazendo previsões no conjunto de teste
````
previsoes <- predict(regressao_log, newdata = dados_teste, type = "response")
````

## 5 - Avaliação (Evaluation) - Regressão logística

### Ponto de corte

#### Após a obtenção da probabilidade, é importante obter a tabela de classificação.

#### Para classificar cada cliente como um potencial inadimplente variável (Y = 1) ou como adimplente (Y = 0) utilizando o modelo, deve-se adotar um valor de probabilidade predita como sendo o ponto de corte. Pode-se considerar como referência o valor da proporção geral de observações com Y = 1, ou seja, de indivíduos que deixaram de realizar o pagamento de suas contas em dia. Ou seja, os indivíduos que tiverem probabilidade predita acima desta referência serão considerados como propensos a se tornarem inadimplentes. O time de negócios tem interesse que modelo classifique tanto os clientes que tem maiores probabilidades de serem inadimplentes como os de serem adimplentes. Desta forma o cientista de dados definiu uma métrica que maximizasse tanto os acertos quanto os erros, chegando à seguinte tabela de classificação:

````
# Obtendo a probabilidade estimada de cancelamento para cada cliente					
emprestimo$Probabilidade <- predict(regressao_log, emprestimo, type = "response") # Criar coluna com as probabilidades no R					
#delete.response(termobj = emprestimo$Probabilidade) # Deletar coluna

# Ponto de corte otimo que minimiza a diferenca entre sensibilidade e especificidade								
ponto_corte_sen_esp <- cutpointr(emprestimo, Probabilidade, Classif,  method = minimize_metric, metric = abs_d_sens_spec,					
pos_class = 1, direction = ">=")								
summary(ponto_corte_sen_esp) 	
````

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/b84b0315-f189-4f26-b9c3-e2f724a21f68.png" width="700px" />
</div>

#### Ponto de corte de 0,7535 que minimiza as diferenças entre Sensibilidade e Especificidade. 

````
# Convertendo as probabilidades em classes (0 ou 1)
previsoes_classes <- as.factor(ifelse(previsoes >= 0.7535, 1, 0))
````

### Análise de desempenho - Matriz de contigência 

````
# Criar a matriz de confusão usando o pacote caret
matriz_confusao <- confusionMatrix(data = previsoes_classes, reference = dados_teste$Classif, positive = "1")
print(matriz_confusao)
````

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/08fa996c-5963-44cb-b51f-6e8efd6efffb.png" width="600px" />
</div>

#### Análise:
#### A Acurácia de 72% significa que, em geral, a cada 100 clientes, o modelo identifica corretamente se haverá ou não inadimplência para 72 deles. Já a Sensibilidade indica que cerca de 73% dos clientes que pagam suas dívidas em dias são corretamente classificados pelo modelo. A Especificidade indica que 72% dos clientes que não pagam suas dívidas em dia são corretamente classificados pelo modelo. 

#### De acordo com os índices de Acurácia, Sensibilidade e Especificidade, podemos afirmar que o modelo apresenta um ótimo desempenho, além de estar devidamente balanceado.

#### Neste modelo não foram implementadas técnicas de engenharia de recursos.

### Análise de desempenho - Curva ROC

#### O valor da área abaixo da curva ROC, abreviado como AUC, é um indicador da qualidade de classificação do modelo, associado a diferentes pontos de corte possíveis. Nesse sentido, é uma medida mais abrangente que o KS, que considera o distanciamento entre sensibilidade e especificidade para um único ponto de corte.

#### Quando o modelo possui alto poder de discriminância de 0’s e 1’s, existem pontos de corte que propiciam altos níveis de sensibilidade e de especificidade, concomitantemente. Isso leva a uma curva ROC com concavidade mais acentuada.

````
# Criando a objeto ROC
roc_objeto <- roc(dados_teste$Classif, previsoes)

# Plotando a curva ROC
plot(roc_objeto, main = "Curva ROC", col = "blue", lwd = 3)

# Adicionando uma legenda
legend("bottomright", legend = paste("AUC =", round(auc(roc_objeto), 2)), col = "blue", lwd = 2)
````

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/b06884f5-183c-4bbc-8f75-8c4f334c9fa8.png" width="600px" />
</div>

#### Análise:
#### De acordo com o índice AUC (0,80) podemos afirmar que o modelo apresenta um excelente desempenho, pois possui alto poder de discriminância de 0’s e 1’s com altos níveis de sensibilidade e de especificidade.

## 4 - Modelagem (Modeling)

### Modelagem com Machine Learning - Decision tree com algoritimo C5.0 (RStudio)

#### O algoritmo C5.0 constrói a árvore de decisão através da divisão da amostra de treinamento com base no teste que resulta na maior razão de ganho. Cada subconjunto obtido da primeira divisão é novamente divido pela aplicação de um novo teste e este processo é repetido até que nenhuma outra divisão seja possível. Por fim, a simplificação da árvore com a poda dos nós que não contribuem para a tarefa de classificação é realizada através da poda pessimista embutida no C5.0.

#### C5.0 pode produzir dois tipos de modelos. Uma árvore de decisão é uma descrição direta das divisões encontradas pelo algoritmo. Cada nó terminal (ou "folha") descreve um subconjunto específico dos dados de treinamento, e cada caso nos dados de treinamento pertence exatamente a um nó terminal na árvore. Em outras palavras, exatamente uma predição é possível para qualquer registro de dados específico apresentado para uma árvore de decisão.

#### Os modelos C5.0 são bastante robustos na presença de problemas como dados omissos e grandes números de campos de entrada. Eles geralmente não requerem longos tempos de treinamento para estimar. Além disso, os modelos C5.0 tendem a ser mais fáceis de entender do que alguns outros tipos de modelo, já que as regras derivadas do modelo possuem uma interpretação muito clara. O C5.0 também oferece o método de reforço poderoso para aumentar a precisão da classificação.

#### Divisão da base para treino e teste

````
# Usando sample para construir os dados de treino e de teste
set.seed(123)
train_sample <- sample(5000, 4000) # 80% para treino e 20% para teste
````

#### Obs:  Não exite um consenso sobre a proporção da divisão entre dados de treino e teste, algumas literaturas reconendam 80/20, 70/30 etc. Essa decisão fica a critério do Cientista de Dados de acordo com cada projeto.

````
# Divisao dos dataframes
emprestimo_train <- emprestimo[train_sample, ]
emprestimo_test  <- emprestimo[-train_sample, ]
````

#### Nesse etapa estamos seguimentando o dataframe em "emprestimo_train" para treino (80%) e em "emprestimo_test" para teste (20%).

#### Verificando a proporção da variável resposta

````
# Verificando a proporção da variavel resposta 
prop.table(table(emprestimo_train$Classif))
prop.table(table(emprestimo_test$Classif))
````

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/d428cf4f-ae9b-44ff-8d59-2218c85b3a98.png" width="500px" />
</div>

#### Transfromando a variável resposta "Classif" para factor

````
# Transformando a variavel resposta "Classif" para factor
emprestimo_train$Classif <- as.factor(emprestimo_train$Classif)
class(emprestimo_train$Classif) # Verificar a classe da variável
````

#### Obs: A transformação de uma variável em fator é uma prática importante para garantir que você esteja tratando corretamente variáveis categóricas e aproveitando ao máximo as funcionalidades estatísticas. Em certos casos, se uma variável categórica não for tratada como fator, os algoritmos podem interpretá-la como uma variável numérica, o que pode levar a interpretações equivocadas dos dados.

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/fe29409b-90bb-4ded-b3e4-d9cccac2bc15.png" width="500px" />
</div>

#### Criando e visualizando o modelo

````
# Criando e visualizando o modelo
emprestimo_model <- C5.0(emprestimo_train[2:7], emprestimo_train$Classif)
print(emprestimo_model)
summary(emprestimo_model)
````

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/fe7107d3-54cc-44fc-95e7-166ccc4c006c.png" width="500px" />
</div>

## 5 - Avaliação (Evaluation) - Decision tree com algoritimo C5.0

### Análise de desempenho 

````
# Avaliando a performance do modelo
emprestimo_pred <- predict(emprestimo_model, emprestimo_test)
print(emprestimo_pred)
summary(emprestimo_pred)
````

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/ca6ed24b-1c8b-4bca-a450-2c393d4da95a.png" width="500px" />
</div>

#### Análise:
#### Para a base de teste, o modelo classificou 88,2% para como inadimplente e 11,8% para adimplente.

### Análise de desempenho - Matriz de contigência para classificação

````
# Matriz de contigencia para comparar valores observados e valores previstos
CrossTable(emprestimo_test$Classif, 
           emprestimo_pred,
           prop.chisq = FALSE, 
           prop.c = FALSE, 
           prop.r = FALSE,
           dnn = c('Observado', 'Previsto'))
````

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/f82fbadc-d146-418f-85cd-d3e534860751.png" width="600px" />
</div>

#### Análise:
#### A Acurácia de 77,4% significa que, em geral, a cada 100 clientes, o modelo identifica corretamente se haverá ou não inadimplência para 77 deles. Já a Sensibilidade indica que cerca de 91% dos clientes que pagam suas dívidas em dias são corretamente classificados pelo modelo. Por outro lado, a Especificidade indica que cerca de 40,5% dos clientes que não pagam suas dívidas em dia são corretamente classificados pelo modelo. 

#### O modelo apresenta um ótimo desempenho de acordo com os índices de Acurácia e Sensibilidade, porém em Especificidade podemos observar que o modelo apresenta um desempenho abaixo do critério de aceitação. Nitidamente, os parâmetros estão desbalanceados, utilizaremos uma "Matriz de Custo" para equalizar esses parâmetros.

### Melhorando a performace do modelo - Aplicando a matriz de custo

#### A matriz de custo é uma ferramenta utilizada em problemas de classificação para avaliar o desempenho de um modelo preditivo, levando em consideração os custos associados aos diferentes tipos de erros que o modelo pode cometer. Em alguns casos, ela também pode ser utilizada como parte de estratégias de balanceamento em modelos preditivos.

#### Ao aplicar custos a cada uma dessas categorias, é possível ajustar a métrica de avaliação para refletir as implicações práticas de diferentes tipos de erros. Em casos de desbalanceamento de classes, a matriz de custo pode ser útil para equilibrar o impacto de falsos positivos e falsos negativos.

#### Por exemplo, se a classe positiva representa eventos raros, como fraudes em transações financeiras, o custo associado a um falso positivo (rotular erroneamente uma transação como fraude) pode ser muito alto. Nesse caso, você pode atribuir um custo maior para Falsos Positivos (FP) na matriz de custo.

````
# Criando uma matriz de dimensoes de custo
matrix_dimensions <- list(c("0", "1"), c("0", "1"))
names(matrix_dimensions) <- c("Previsto", "Observado")
print(matrix_dimensions)

# Construindo a matriz
error_cost <- matrix(c(0, 2.5, 0, 2.5), nrow = 2, dimnames = matrix_dimensions)
print(error_cost)

# Aplicando a matriz a arvore
emprestimo_cost <- C5.0(emprestimo_train[2:7], emprestimo_train$Classif, costs = error_cost)

# Avaliando a performance do modelo
emprestimo_cost_pred <- predict(emprestimo_cost, emprestimo_test)
summary(emprestimo_cost_pred)
````

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/c6c43668-44bd-4bbf-a307-0a7a2735f648.png" width="400px" />
</div>

#### Análise:
#### Para a base de teste, o modelo classificou 59% para como inadimplente e 41% para adimplente, houve uma melhora significativa no balanceamento das distribuições.

#### Antes da matriz de custo:
#### Inadimpltes: 88,2 | Adimpletes: 11,8%

#### Depois da matriz de custo:
#### Inadimplentes: 59% | Adimplentes: 41%

### Análise de desempenho - Matriz de contigência para classificação após matriz de custo

````
# Matriz de contigencia para comparar valores observados e valores previstos
CrossTable(emprestimo_test$Classif, 
           emprestimo_cost_pred,
           prop.chisq = FALSE, 
           prop.c = FALSE, 
           prop.r = FALSE,
           dnn = c('Observado', 'Previsto'))
````

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/33dd066e-293a-42bc-9f69-dcdaaf9aab93.png" width="600px" />
</div>

#### Análise:
#### A Acurácia de 70% significa que, em geral, a cada 100 clientes, o modelo identifica corretamente se haverá ou não inadimplência para 70 deles. Já a Sensibilidade indica que cerca de 70% dos clientes que pagam suas dívidas em dias são corretamente classificados pelo modelo. Por outro lado, a Especificidade indica que cerca de 70% dos clientes que não pagam suas dívidas em dia são corretamente classificados pelo modelo. 

#### De acordo com os índices de Acurácia, Sensibilidade e Especificidade, podemos afirmar que o modelo apresenta um ótimo desempenho, além de estar devidamente balanceado após a aplicação da matriz de custo.

## 6 - Implantação (Deployment)

#### O modelo não foi implantado (deployment) por ser computacionamente e financeiramente muito onerosos.

## Conclusão

#### Analisando os valores das métricas de avaliação de desempenho dos modelos, podemos afimar o que modelo de Regressão Logística apresentou melhores índicies comparado com a Árvore de Decisão, o que sugere que esse modelo deva ser adotado para realizar novas predições.

#### Regressão Logística
#### Acurácia = 72%
#### Sensibilidade = 73%
#### Especificidade = 72%

#### Árvore de Decisão C5.0
#### Acurácia = 70%
#### Sensibilidade = 70%
#### Especificidade = 70%


