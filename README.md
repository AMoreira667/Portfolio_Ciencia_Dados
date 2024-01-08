## Projeto 01 - Avaliação Riso de Credito

#### Uma instituição financeira acompanha periodicamente o indicador de inadimplência dos produtos financeiros e tem verificado o aumento expressivo desta taxa para o produto empréstimo, no último ano. Por mais que não pagamento gere um valor de “empréstimo” que possa gerar receita futura (devido a taxa de juros) para a instituição, parte do dinheiro pode não ser recuperada. Portanto, traçar estratégias de relacionamento, crédito e cobrança são necessários para controlar a taxa de inadimplência. Assim, a área de Empréstimos, solicitou a construção de um modelo preditivo para o produto com o objetivo de identificar o perfil dos clientes PF inadimplentes. Como a quantidade de clientes é grande e o custo de comunicação é limitado, o modelo auxiliará a instituição financeira a trabalhar de forma otimizada com seus clientes. O modelo deve ter boas taxas de acurárica, especificidade e sensibilidade (mínimo 70%).

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

### Base de Dados

#### Considerando dados históricos provenientes de um banco, referentes a 5.000 clientes que solicitaram empréstimos financeiros. A base contém informações como idade, tempo de residência no endereço atual, renda etc., além da variável resposta Classif, que indica se cada clientes foi um bom pagador (1) ou um mau pagador (0). Deseja-se avaliar o potencial dessas variáveis para predizer se novos clientes serão bons ou maus pagadores. 

### Dicionário de Dados

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/b5f92e35-6fff-4c41-8eeb-5eeaa4de2467.png" width="700px" />
</div>

## Análise Exploratória de Dados (RStudio) 

#### A análise exploratória de dados (AED) é o uso de ferramentas para examinar determinado conjunto de dados antes mesmo da aplicação de qualquer técnica estatística para tirar conclusões sobre eles. É uma maneira de obter um entendimento prévio sobre os dados disponíveis para um estudo e das variáveis que eles envolvem. <br>
#### Depois que os dados são coletados e armazenados em um banco de dados, a análise descritiva é o primeiro passo dentro do AED. Nessa etapa, os pesquisadores se familiarizam e organizam esses dados de forma sintetizada para saber que tipo de informações podem ser tiradas deles.
#### Dito de outra forma, antes de realizar uma análise exploratória de dados, temos que preparar esses dados para que se tornem analisáveis. Há um conjunto de tarefas envolvido nesse processo:

#### ✓ Identificar quais são as variáveis envolvidas e como elas se relacionam;

#### ✓ Identificar os chamados outliers, casos de exceção que não seguem uma tendência muito diferente da maior parte da amostra analisada;

#### ✓ Verificar se há dados ausentes;

#### ✓ Fazer algumas suposições preliminares sobre as tendências que esses dados demonstram, como normalidade e linearidade.

#### Esse é o processo que acontece nos bastidores de um sistema voltado para Business Intelligence (BI), que é a análise de dados críticos para ajudar os gestores de uma empresa a tomarem as melhores decisões. 

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/03489886-6784-4813-b73d-1422257f51b8.png" width="350px" />
</div>

### Análise Exploratória de Dados (RStudio) - Pacotes e Biblioteca

### Mapear diretorio onde esta salvo a base de dados

````
setwd("inserir directorio do arquivo"") # Ou Ctrl + Shift + H
````

### Pacotes necessários

````
install.packages("readxl")            # Para leitura de dados Excel
install.packages("Information")       # Para calculo IV 
install.packages("car")               # Para analise de regressao e diagnostico de modelos 
install.packages("cutpointr")         # Para calculo ponto de corte
install.packages("ROCR")              # Para calculo KS e AUC			
install.packages("dplyr")             # Para manipulacao e transformacao dados
install.packages("psych")             # Para analise psicometrica e estatisitca
install.packages("C50")               # Decision tree algoritmo C5.0
install.packages("gmodels")           # Matriz de contigencia
installed.packages()                  # Para verificar bibliotecas instaladas
install.packages("GGally")            # Correlograma
````
### Bibliotecas necessárias

````
library(readxl)				
library(Information)				
library(car)				
library(cutpointr)				
library(ROCR)
library(dplyr)
library(psych)
library(C50)
library(gmodels)
library(GGally)
````
### Retirar a notacao cientifica

````
options(scipen = 999) 				
````

### Leitura da base de dados

````
emprestimo <- read_excel("Regressao logistica.xlsx", sheet = "Emprestimo - Dados")							
````

### Analise exploratoria dos dados - Univariada

### Cabeçalho

````
head(emprestimo, 15) # Cabecalho contento as 15 primeiras linhas do dataframe
````

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/823031af-c0f6-4464-a681-3fcc89a72307.png" width="700px" />
</div>

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

### Analise exploratoria dos dados - Bivariada

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

### Analise exploratoria dos dados - Bivariada com Information Value (IV)

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

#### Como a base de dados já foi previamente tratada, vamos pular para a etapa de Modelagem.

## 4 - Modelagem (Modeling)

### Regressão logística (RStudio)

#### A modelagem estatística tradicional é uma abordagem que envolve o uso de métodos estatísticos clássicos para analisar dados e fazer inferências sobre populações ou processos subjacentes. Essa abordagem é frequentemente utilizada para entender as relações entre variáveis, realizar previsões e tomar decisões informadas com base em evidências quantitativas. 

#### A regressão logística múltipla é uma técnica estatística utilizada para modelar a relação entre uma variável binária (ou dicotômica) dependente e várias variáveis independentes, que podem ser tanto numéricas quanto categóricas. Essa técnica é uma extensão da regressão logística simples, que lida com apenas uma variável independente.

#### Na regressão logística múltipla, o objetivo é estimar os coeficientes das variáveis independentes de forma a entender como cada uma delas contribui para a probabilidade de um evento ocorrer. 

#### A principal diferença em relação à regressão linear é que a regressão logística modela a relação entre as variáveis independentes e a log-odds da probabilidade do evento acontecer. A log-odds é a transformação logarítmica das probabilidades e é uma forma conveniente de trabalhar com problemas de classificação binária.

````
# Modelagem estatistica tradicional - Regressao logisttica
regressao_log <- glm(Classif ~ Idade + 
                     Tempo_Experiencia + 
                     Tempo_Endereco + 
                     Renda + 
                     Debito_Renda +
                     Variacao_Debito, 
                     binomial(link = "logit"), 
                     data = emprestimo)
summary(regressao_log)
````
<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/05c2dade-d92b-4e9f-8cb8-8fcfc1b7f286.png" width="600px" />
</div>

#### No processo de construção do modelo deve-se retirar, a cada passo, a variável com menor significância estatística. Como estamos adotando 95% de confiança, deve-se retirar variáveis cujo p-valor seja maior do que 5%. Esse procedimento é conhecido como Stepwise.

#### A variável explicativa Tempo_Experiencia apresenta p-valor acima de 5%. Logo, não é um aspecto estatisticamente significativo para explicar a decisão de conceder empréstimo e pode ser retirado do modelo. 

````
# Modelagem estatistica tradicional - Retiradno a variavel Tempo_Experiencia
regressao_log <- glm(Classif ~ Idade + 
                     Tempo_Endereco + 
                     Renda + 
                     Debito_Renda +
                     Variacao_Debito, 
                     binomial(link = "logit"), 
                     data = emprestimo)
summary(regressao_log)
````
<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/addb3371-2df2-48f0-a0d3-c3570c3afd9e.png" width="600px" />
</div>

#### Analisando os p-valores obtidos pelo modelo, consegue-se estatisticamente sustentar são as variáveis Debito_Renda, Tempo_Endereco, Variacao_Debito e Renda são variáveis significativas, adotando um nível de confiança de 95%. Logo, são aspectos estatisticamente significativos para explicar a decisão de conceder empréstimo, e devem ser mantidos no modelo.

### Cálculo das estimativas

#### Tendo em vista que todas as variáveis são importantes, pode-se calcular a probabilidade final de uma pessoa ser inadimplente de forma consistente da seguinte forma:

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/1b3cdaf1-9637-41bc-a483-fa537417e59c.png" width="600px" />
</div>

#### Por exemplo, uma pessoa com 80 anos de Idade, com 17 anos de Tempo_Endereco, com Renda de 36,1 salários mínimos, com 4,25 de Debito_Renda e com 1,82 de Variacao_Debito, teriamos: 

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/d97a8075-09c7-4e46-81b6-949d48a67efa.png" width="600px" />
</div>

### Obtendo as probabilidades estimadas para cada cliente

````
# Obtendo a probabilidade estimada de para cada cliente					
emprestimo$Probabilidade <- predict(regressao_log, emprestimo, type = "response") # Criar coluna com as probabilidades estimadas 
````

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/c8011556-a8de-4799-9ed8-6feecbd75240.png" width="600px" />
</div>

### Estatística VIF - Verificando Multicolinearidade

#### Quando lidamos com uma regressão múltipla, ou seja, com 2 ou mais variáveis explicativas, algumas delas podem representar informações muito similares. Esse tipo de redundância, no contexto de análise de regressão, é denominado multicolinearidade. 

#### ✓ A multicolinearidade ocorre quando variáveis explicativas fortemente associadas entre si são consideradas no mesmo modelo de regressão, seja linear ou logística. 

#### ✓ A redundância de informação eleva potencialmente o nível de variabilidade dos parâmetros estimados (betas) associados às variáveis correlacionadas, distorcendo a sua interpretação. Isso torna o modelo instável e, muitas vezes, compromete a sua utilização para predições futuras.

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

## 5 - Avaliação (Evaluation) - Regressão logística

### Ponto de corte

#### Após a obtenção da probabilidade, é importante obter a tabela de classificação.

#### Para classificar cada cliente como um potencial inadimplente variável (Y = 1) ou como adimplente (Y = 0) utilizando o modelo, deve-se adotar um valor de probabilidade predita como sendo o ponto de corte. Pode-se considerar como referência o valor da proporção geral de observações com Y = 1, ou seja, de indivíduos que deixaram de realizar o pagamento de suas contas em dia. Ou seja, os indivíduos que tiverem probabilidade predita acima desta referência serão considerados como propensos a se tornarem inadimplentes. O time de negócios tem interesse que modelo classifique tanto os clientes que tem maiores probabilidades de serem inadimplentes como os de serem adimplentes. Desta forma o cientista de dados definiu uma métrica que maximizasse tanto os acertos quanto os erros, chegando à seguinte tabela de classificação:

````
# Ponto de corte otimo que minimiza a diferenca entre sensibilidade e especificidade								
ponto_corte_sen_esp <- cutpointr(emprestimo, Probabilidade, Classif,  method = minimize_metric, metric = abs_d_sens_spec,							
                                 pos_class = 1, direction = ">=")								
summary(ponto_corte_sen_esp) 	
````

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/6dd9aaf3-4fb6-4a8d-aa76-490f966fd3d9.png" width="700px" />
</div>

````
# Obtendo a probabilidade estimada de ser um bom pagador para cada cliente 					
emprestimo$Predito <- as.factor(ifelse(emprestimo$Probabilidade >= 0.7535, 1, 0))
````

### Análise de desempenho - Matriz de contigencia para classificação

````
# Obtendo tabela com medidas de desempenho
tabela <- table(emprestimo$Classif, emprestimo$Predito)				
(acuracia       <- (tabela[1,1] + tabela[2,2]) / sum(tabela))				
(especificidade <- tabela[1,1] / (tabela[1,1] + tabela[1,2]))				
(sensibilidade  <- tabela[2,2] / (tabela[2,1] + tabela[2,2]))				
tabela
````

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/e9a9c22d-45fb-4cdf-a256-3bdb833e8342.png" width="600px" />
</div>

#### Análise: 
#### A Acurácia de 71,6% significa que, em geral, a cada 100 clientes, o modelo identifica corretamente se haverá ou não inadimplência para 72 deles. Já a Sensibilidade indica que cerca de 72% dos clientes que pagam suas dívidas em dias são corretamente classificados pelo modelo. A Especificidade indica que 72% dos clientes que não pagam suas dívidas em dia são corretamente classificados pelo modelo. 

#### De acordo com os índices de Acurácia, Sensibilidade e Especificidade, podemos afirmar que o modelo apresenta um ótimo desempenho, além de estar devidamente balanceado.

### Análise de desempenho - KS

#### A estatística de Kolmogorov-Smirnov (KS) reflete a máxima separação entre as curvas de frequências acumuladas de 2 grupos distintos de observações, no nosso caso, baseadas na variável resposta binária (Y). O valor do KS varia entre 0 (nenhuma separação) e 1 (separação completa).

````
# Obtendo o KS do modelo final
ks <- max(attr(perf, 'y.values')[[1]] - attr(perf, 'x.values')[[1]])
print(ks)
````

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/8c696451-29d3-4a13-b4b0-269a6b1b68f3.png" width="600px" />
</div>

#### Análise:
#### De acordo com o índice KS podemos afirmar que o modelo apresenta um desempenho muito bom.

### Análise de desempenho - AUC

#### O valor da área abaixo da curva ROC, abreviado como AUC, é um indicador da qualidade de classificação do modelo, associado a diferentes pontos de corte possíveis. Nesse sentido, é uma medida mais abrangente que o KS, que considera o distanciamento entre sensibilidade e especificidade para um único ponto de corte.

#### Quando o modelo possui alto poder de discriminância de 0’s e 1’s, existem pontos de corte que propiciam altos níveis de sensibilidade e de especificidade, concomitantemente. Isso leva a uma curva ROC com concavidade mais acentuada.

````
# Obtendo o AUC e curva ROC do modelo final
pred <- prediction(emprestimo$Probabilidade, emprestimo$Classif)					
perf <- performance(pred, "tpr", "fpr")					
auc <- performance(pred, "auc")					
auc <- auc@y.values[[1]]					
print(auc)
````

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/75c713c1-460e-45d9-b225-08e4503c0d3a.png" width="600px" />
</div>

#### Análise:
#### De acordo com o índice AUC (0,79) podemos afirmar que o modelo apresenta um bom desempenho.

## 4 - Modelagem (Modeling)

### Modelagem com IA - Decision tree com algoritimo C5.0 (RStudio)

#### O algoritmo C5.0 constrói a árvore de decisão através da divisão da amostra de treinamento com base no teste que resulta na maior razão de ganho. Cada subconjunto obtido da primeira divisão é novamente divido pela aplicação de um novo teste e este processo é repetido até que nenhuma outra divisão seja possível. Por fim, a simplificação da árvore com a poda dos nós que não contribuem para a tarefa de classificação é realizada através da poda pessimista embutida no C5.0.

#### C5.0 pode produzir dois tipos de modelos. Uma árvore de decisão é uma descrição direta das divisões encontradas pelo algoritmo. Cada nó terminal (ou "folha") descreve um subconjunto específico dos dados de treinamento, e cada caso nos dados de treinamento pertence exatamente a um nó terminal na árvore. Em outras palavras, exatamente uma predição é possível para qualquer registro de dados específico apresentado para uma árvore de decisão.

#### Os modelos C5.0 são bastante robustos na presença de problemas como dados omissos e grandes números de campos de entrada. Eles geralmente não requerem longos tempos de treinamento para estimar. Além disso, os modelos C5.0 tendem a ser mais fáceis de entender do que alguns outros tipos de modelo, já que as regras derivadas do modelo possuem uma interpretação muito clara. O C5.0 também oferece o método de reforço poderoso para aumentar a precisão da classificação.

````
# Usando sample para construir os dados de treino e de teste
set.seed(123)
train_sample <- sample(5000, 4000) # 80% para treino e 20% para teste
````

#### Dividindo a amostra para receber dados de treino e teste.
#### Obs:  Não exite um consenso sobre a proporção da divisão entre dados de treino e teste, algumas literaturas reconendam 80/20, 70/30 etc. Essa decisão fica a critério do Cientista de Dados de acordo com cada projeto.

````
# Divisao dos dataframes
emprestimo_train <- emprestimo[train_sample, ]
emprestimo_test  <- emprestimo[-train_sample, ]
````

#### Nesse etapa estamos seguimentando o dataframe em "emprestimo_train" para treino (80%) e em "emprestimo_test" para teste (20%).

````
# Verificando a proporção da variavel resposta 
prop.table(table(emprestimo_train$Classif))
prop.table(table(emprestimo_test$Classif))
````

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/d428cf4f-ae9b-44ff-8d59-2218c85b3a98.png" width="600px" />
</div>
