## Projeto 01 - Avaliação Riso de Credito

#### Uma instituição financeira acompanha periodicamente o indicador de inadimplência dos produtos financeiros e tem verificado o aumento expressivo desta taxa para o produto empréstimo, no último ano. Por mais que não pagamento gere um valor de “empréstimo” que possa gerar receita futura (devido a taxa de juros) para a instituição, parte do dinheiro pode não ser recuperada. Portanto, traçar estratégias de relacionamento, crédito e cobrança são necessários para controlar a taxa de inadimplência. Assim, a área de Empréstimos, solicitou a construção de um modelo preditivo para o produto com o objetivo de identificar o perfil dos clientes PF inadimplentes. Como a quantidade de clientes é grande e o custo de comunicação é limitado, o modelo auxiliará a instituição financeira a trabalhar de forma otimizada com seus clientes.

#### Criterio utilizado para constução do projeto: Cross Industry Standard Process for Data Mining (CRISP-DM)

#### CRISP-DM é a abreviação de Cross Industry Standard Process for Data Mining, que pode ser traduzido como Processo Padrão Inter-Indústrias para Mineração de Dados. Desempenha um papel crucial no cenário empresarial moderno, permitindo que as organizações tomem decisões embasadas e obtenham insights valiosos. Nesse contexto, a metodologia CRISP-DM tem se destacado como uma estrutura robusta para abordar projetos de ciência de dados.

#### Etapas da CRIPS-DM

#### 1 - Compreensão do Negócio (Business Understanding) Antes de iniciar um projeto de análise de dados, é essencial compreender o contexto e os objetivos do negócio. Nesta fase, definimos claramente as metas do projeto e as alinhamos aos objetivos estratégicos da organização;

#### 2 - Compreensão dos Dados (Data Understanding) Coletar dados relevantes é fundamental para o sucesso do projeto. Nessa fase, exploramos e nos familiarizamos com os dados disponíveis, identificamos lacunas e problemas potenciais, e avaliamos a qualidade e a adequação dos dados para o projeto;

#### 3 - Preparação dos Dados (Data Preparation) Os dados brutos raramente estão prontos para a análise. Nesta fase, realizamos a limpeza dos dados, tratamos valores ausentes ou inconsistentes e integramos diferentes fontes de dados. O objetivo é criar um conjunto de dados preparado para as etapas subsequentes;

#### 4 - Modelagem (Modeling) A fase de modelagem envolve a aplicação de técnicas e algoritmos de modelagem de dados aos dados preparados. Selecionamos as técnicas mais adequadas, como regressão, classificação ou agrupamento, e ajustamos e avaliamos os modelos para garantir sua precisão e eficácia;

#### 5 - Avaliação (Evaluation) A avaliação dos modelos desenvolvidos é crucial para medir sua qualidade e desempenho. Nesta fase, utilizamos métodos como validação cruzada e métricas de desempenho para avaliar o quão bem os modelos se saem em dados não vistos. Com base nessa avaliação, podemos ajustar e aprimorar os modelos, se necessário;

#### 6 - Implantação (Deployment) A fase final da metodologia CRISP-DM é a implantação do modelo em um ambiente de produção. Integramos o modelo aos sistemas existentes, monitoramos seu desempenho contínuo e garantimos a adoção pela equipe de negócios.

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/e2cd3dbc-6a95-47d5-87df-130bd0b409d8.png" width="700px" />
</div>

#### Inciando o projeto

#### 1 - Compreensão do Negócio (Business Understanding)

#### O objetivo do trabalho é predizer e avaliar o risco de empréstimo de clientes PF (Pessoa Física) de uma instituição financeira. A predição será realizada utilizando dados históricos transacionais e modelos estatísticos e algoritmos de Inteligência Artificial, que selecionarão as características mais relevantes que explicam a justificativa de empréstimo ou não empréstimo. Desta forma, a empresa poderá traçar estratégias financeiras, desenvolver réguas de empréstimos e ações preventivas para minimizar de forma proativa sua taxa de inadimplência de empréstimos.

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/eddb0d7d-28df-4acf-93fd-c3280934083b.png" width="700px" />
</div>

#### 2 - Compreensão dos Dados (Data Understanding)

#### Base de Dados

#### Considerando dados históricos provenientes de um banco, referentes a 5.000 clientes que solicitaram empréstimos financeiros. A base contém informações como idade, tempo de residência no endereço atual, renda etc., além da variável resposta Classif, que indica se cada clientes foi um bom pagador (1) ou um mau pagador (0). Deseja-se avaliar o potencial dessas variáveis para predizer se novos clientes serão bons ou maus pagadores. 

#### Dicionário de Dados

<div align="center">
<img src="https://github.com/AMoreira667/Portfolio_Ciencia_Dados/assets/89550284/b5f92e35-6fff-4c41-8eeb-5eeaa4de2467.png" width="700px" />
</div>

#### Análise Exploratória de Dados (RStudio) 

#### A análise exploratória de dados (AED) é o uso de ferramentas para examinar determinado conjunto de dados antes mesmo da aplicação de qualquer técnica estatística para tirar conclusões sobre eles. É uma maneira de obter um entendimento prévio sobre os dados disponíveis para um estudo e das variáveis que eles envolvem.
#### Depois que os dados são coletados e armazenados em um banco de dados, a análise descritiva é o primeiro passo dentro do AED. Nessa etapa, os pesquisadores se familiarizam e organizam esses dados de forma sintetizada para saber que tipo de informações podem ser tiradas deles.
#### Dito de outra forma, antes de realizar uma análise exploratória de dados, temos que preparar esses dados para que se tornem analisáveis. Há um conjunto de tarefas envolvido nesse processo.
#### Identificar quais são as variáveis envolvidas e como elas se relacionam;
#### Identificar os chamados outliers, casos de exceção que não seguem uma tendência muito diferente da maior parte da amostra analisada;
#### Verificar se há dados ausentes;
#### Fazer algumas suposições preliminares sobre as tendências que esses dados demonstram, como normalidade e linearidade.
#### Esse é o processo que acontece nos bastidores de um sistema voltado para Business Intelligence (BI), que é a análise de dados críticos para ajudar os gestores de uma empresa a tomarem as melhores decisões. 

#### Análise Exploratória de Dados (RStudio) - Pacotes e Biblioteca

#### Mapear diretorio onde esta salva a base de dados

#### setwd("inserir directorio do arquivo"") #### Ou Ctrl + Shift + H

#### Pacotes necessarios
#### install.packages("readxl") *** Para leitura de dados Excel
install.packages("Information") # Para calculo IV
install.packages("car“) # Para analise de regressao e diagnostico de modelos 
install.packages("cutpoint") # Para calculo ponto de corte
install.packages("ROCR") # Para calculo KS e AUC
install.packages("ggplot2") # Para criacao de tabelas e graficos
install.packages("dplyr") # Pra manipulacao e transformacao dados


