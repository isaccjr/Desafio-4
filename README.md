# *Modelo de Regressão para Marketing*
![image](https://github.com/user-attachments/assets/440fe74a-ac89-49b1-80ac-3e0e29fd4b79)

Desafio 4 do curso da carreira Cientista de Dados da Escola DNC

Desafio: Construindo um modelo de Regressão para marketing
Habilidades: Regressão

## **Contexto - Introdução**

Uma empresa está investindo mensalmente em plataformas de publicidade online, como Youtube, Facebook e newspaper, para a prospecção de leads (pessoas interessadas em seus produtos). A fim de acompanhar o desempenho desses investimentos, a empresa registra todos os gastos com publicidade e todos os retornos de vendas gerados a partir desses investimentos.

Para **entender** melhor **a relação entre as variáveis** presentes nesses registros e **identificar os fatores que mais impactam** na geração de leads, a empresa solicitou a análise de um especialista em dados. **Além disso, a empresa busca criar um modelo de predição** de valores para estimar o retorno de vendas que pode ser gerado a partir de um determinado investimento em publicidade.

## Sobre os dados

A tabela contém informações dos investimentos feitos pelo youtube, facebook, newspaper e também a quantidade de cada.

## 🎯 Etapas de Desenvolvimento


### **Etapa 01) Análise Descritiva**

Esta etapa consiste em explorar os dados do dataset para **compreender melhor as variáveis e identificar problemas**. Para isso, foi utilizado a biblioteca **Pandas** para importar e manipular os dados e realizar cálculos estatísticos, além das bibliotecas de visualização. 

É importante investigar o tipo de dado em cada variável, os valores e a distribuição dos dados. Ao final, foi feito uma interpretação sólida dos dados para avançar para a próxima etapa.



### **Etapa 02) Análise Exploratória**

Nesta etapa iremos explorar mais a fundo os dados, **identificando relações entre as variáveis e descobrindo padrões relevantes.** Para isso, utilizei técnicas de visualização de dados e análises estatísticas, buscando possíveis correlações e identificando possíveis outliers ou desvios da normalidade.

![image](https://github.com/user-attachments/assets/f92a1c1b-7d2d-4cb5-b1c4-e1e18df7972d)

![image](https://github.com/user-attachments/assets/d3461cfa-eb73-43b1-9f9d-33774d1c1a81)

Pelos gráficos vemos um fenêmeno interessante, quanto maior o gasto em publicidade no Youtube 📺 maiores as vendas 📈 mostrando um correlação positiva já esperada entretanto quanto maior o gasto menos eficiente ele se mostra, mas o mesmo não acontece no Facebook o que pode sinalizar uma maior eficiência. O fenômeno pode ser explicado em como as duas redes sociais se diferem, não adianta aplicar muito mais recursos no Youtube, não vão entregar fora do nincho agora já o Facebook sim.

![image](https://github.com/user-attachments/assets/3b255a76-a2ca-4873-a255-a5f8b6dcc17c)

Analisando os gastos e a correlações com as vendas e a coluna calculada retorno, achamos que a agência deveria diminuir os gastos em publicidade em jornais e aumentar no canal Facebook já que a correlação com a primeira é de 25% e da segunda 60% e o Facebook ainda tem a vantagem de ser o unico dos três canais sem um correlação negativa com o retorno, logo aumentar o gasto nesse canal se prova a melhor opção se a Agência buscar maximizar o retorno em cada campanha.

### **Etapa 03) Modelagem**

Para esta etapa,  **construi um modelo** simples de **regressão** que permite a previsão solicitada pela empresa, com base nos dados disponíveis. Para isto, utilizei as bibliotecas sklearn e Xgboost, testei os modelos de Regressão Linear, SVR, RandomForestRegressor, GradientBoostingRegressor e o Regressor da biblioteca Xgboost o XGBRegressor 
O modelo escolhido foi o gradiente boosting da biblioteca Sklearn.

O modelo escolhido consegue um precisão de 96,63%. O que significa um erro de 1118 unidades monetárias. 
