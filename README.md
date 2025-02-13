# 1° Challenge de Dados -  Alura

<center>
  <img src="https://i.imgur.com/jn7km8o.png">
</center>

A Alura Voz é uma empresa de telecomunicação que nos contratou para atuar como cientistas de dados na equipe de vendas. Logo na primeira semana, a liderança nos informa que é muito necessário realizar um estudo quanto ao Churn da empresa. É explicado que o churn indica se um cliente cancelou ou não o contrato com a empresa, e também que, nos casos de perda do cliente a empresa também perde faturamento, o que ocasiona prejuizos na receita final.

Desse modo, nossa liderança informa que temos 4 semanas para buscar uma alternativa que possa minimizar a saída de clientes e nos entrega um conjunto de dados da Alura Voz que contém diversas informações sobre os clientes e também informa se eles deixaram ou não a empresa.

Sabemos que, antes de pensar em qualquer alternaiva, é preciso entender as informações que recebemos e, após uma pequena reunião, concluímos que na primeira semana nós nos dedicaríamos a entender o banco de dados, descobrir os tipos de dados, verificar a existencia de valores incoerentos e corrigi-los caso seja necessário.

## Limpeza dos dados -  Arquivo limpeza.ipynb

### Dados

Ao observar a [Base de dados da Alura Voz](https://github.com/sthemonica/alura-voz/blob/main/Dados/Telco-Customer-Churn.json), verificamos que essa é uma base disponibilizada via API em formato JSON com várias camandas de dados.

Junnto a esses dados também foi disponibilizado o [dicionário dos dados](https://github.com/sthemonica/alura-voz/blob/main/dicionario.md) que nele contém todas as informações sobre as colunas do banco de dados.

Nela, além da informação se o cliente deixou ou não a empresa, também contém:

<b>Cliente:</b>
 
* `gender`: gênero (masculino e feminino)
* `SeniorCitizen`: informação sobre um cliente ter ou não idade igual ou maior que 65 anos
* `Partner`: se o cliente possui ou não um parceiro ou parceira
* `Dependents`: se o cliente possui ou não dependentes

<b>Serviço de telefonia</b>


 * `tenure`: meses de contrato do cliente
 * `PhoneService`: assinatura de serviço telefônico
 * `MultipleLines`: assisnatura de mais de uma linha de telefone
 

<b>Serviço de internet</b>


 * `InternetService`: assinatura de um provedor internet
 * `OnlineSecurity`: assinatura adicional de segurança online
 * `OnlineBackup`: assinatura adicional de backup online
 * `DeviceProtection`: assinatura adicional de proteção no dispositivo
 * `TechSupport`: assinatura adicional de suporte técnico, menos tempo de espera
 * `StreamingTV`: assinatura de TV a cabo
 * `StreamingMovies`: assinatura de streaming de filmes


<b>Contrato</b>


 * `Contract`: tipo de contrato
 * `PaperlessBilling`: se o cliente prefere receber online a fatura
 * `PaymentMethod`: forma de pagamento
 * `Charges.Monthly`: total de todos os serviços do cliente por mês
 * `Charges.Total`: total gasto pelo cliente

Tendo essas informações entendemos nossos dados e, assim, podemos realizar uma análise mais técnica, buscando entender JSON, os dados e realizar o tratamento deles.

Todo o desenvolvimento feito na nossa 1° semana pode ser observado no [notebook semana 1](https://github.com/sthemonica/alura-voz/blob/main/1-Limpeza%20dos%20dados/limpeza.ipynb).

## Análise dos dados

Feito o reconhecimento e tratamento de dados, demos continuidade do nosso trabalho, agora, analisando os dados. Em conversa com o grupo, conluímos que precisamos fazer uma análise gráfica para entender quais as variáveis que são relacionadas com o churn para que a equipe de vendas tenha uma noção do cenário atual, e também para que nós possamos entender de uma forma mais clara e formar possíveis hipóteses do que está acontecendo com os clientes.

Planejamos assim, fazer uma **análise estatística** dos dados, verificar os **tipos de dados** que temos, gerar gráficos de **distribuição de dados binários ou categóricos**, plot de **Boxplots** para detecção de outliers e **matriz de correlação**. Assim, de cada análise e verificação conseguimos identificar a relação dos dados com nosso alvo, identificar valores incoerêntes e/ou desnecessários e támbem entender ainda mais os dados que temos.

Todo o desenvolvimento e análise feita na nossa 2° semana pode ser observado no [notebook semana 2](https://github.com/sthemonica/alura-voz/blob/main/2-%20An%C3%A1lise%20dos%20dados/analise.ipynb).

## Modelos de Machine Learning

Ao discutir e verificar todas as análises feitas na 2° semana, concluímos que uma boa opção para minimizar a evasão de clientes na Alura Voz é ter um modelo treinado que vai classificar clientes como potenciais pessoas a deixar a empresa e assim, a equipe de vendas pode agir antes que isso possa, de fato, ocorrer.

Com isso, iniciamos a preparação de dados para serem enviados aos modelos. Pelos estudos da semana 2, nós já tinhamos identificado entradas desinteressantes para o aprendizado, dados categóricos não numéricos que seriam impossíveis de serem reconhecidos por um modelo matemático, além de termos o nosso alvo com valores desbalanceados. Esses dados logo foram tratados para se ajustarem ao modelo.

Os modelos de classificação que definimos serem interessantes para solucionar nosso problema foram o **SVC**, **Decision Tree** e **Random Forest**. No entanto, não entramos em um consenso de qual modelo seria o melhor para o caso. Por isso, decidimos criar os 3 modelos e treiná-los, para que na nossa última semana pudessemos avaliar qual o mais interessante de ser utilizado.

Todo o desenvolvimento e análise feita na nossa 3° semana pode ser observado no [notebook semana 3 dos modelos](https://github.com/sthemonica/alura-voz/blob/main/3-Modelos%20de%20ML/modelos.ipynb) e [notebook semana 3 para melhoria do melhor modelo](https://github.com/sthemonica/alura-voz/blob/main/4-Melhorando%20o%20modelo/otimizacao.ipynb).

