# 1° Challenge de Dados -  Alura

Esse projeto segue a metodologia de atuar em uma empresa hipotetica para experênciar as atividades de um cientisda de dados utilizando, a empresa foi nomeada Alura Voz.

A Alura Voz, uma empresa hipotética de telecomunicações, me contratou para atuar como cientista de dados na equipe de vendas. Logo na minha primeira semana, a liderança deixou claro que era essencial realizar um estudo sobre o churn da empresa. Foi explicado que o churn representa a saída de clientes e que, quando isso acontece, a empresa não apenas perde consumidores, mas também sofre impactos negativos em sua receita.

Diante desse cenário, recebi a missão de buscar, em um prazo de quatro semanas, uma alternativa para minimizar a saída de clientes. Para isso, fui apresentado a um conjunto de dados da Alura Voz, contendo diversas informações sobre os clientes, incluindo se eles permaneceram ou não na empresa.

Antes de propor qualquer solução, compreendi que o primeiro passo era analisar cuidadosamente os dados disponíveis. Após uma breve reunião, decidi que minha primeira semana seria dedicada a entender a estrutura do banco de dados, identificar os tipos de informações contidas nele, verificar a existência de valores inconsistentes e corrigi-los, caso necessário.

## Limpeza dos dados - limpeza.ipynb

### Dados

Ao observar a Base de dados da Alura Voz, verificamos que essa é uma base disponibilizada via API em formato JSON com várias camandas de dados.

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



## Análise dos dados - analise.ipynb

Feito o reconhecimento e tratamento de dados, demos continuidade do nosso trabalho, agora, analisando os dados. Em conversa com o grupo, conluímos que precisamos fazer uma análise gráfica para entender quais as variáveis que são relacionadas com o churn para que a equipe de vendas tenha uma noção do cenário atual, e também para que nós possamos entender de uma forma mais clara e formar possíveis hipóteses do que está acontecendo com os clientes.

Planejamos assim, fazer uma **análise estatística** dos dados, verificar os **tipos de dados** que temos, gerar gráficos de **distribuição de dados binários ou categóricos**, plot de **Boxplots** para detecção de outliers e **matriz de correlação**. Assim, de cada análise e verificação conseguimos identificar a relação dos dados com nosso alvo, identificar valores incoerêntes e/ou desnecessários e támbem entender ainda mais os dados que temos.



## Modelos de Machine Learning - modelos.ipynb

Ao discutir e verificar todas as análises feitas na 2° semana, concluímos que uma boa opção para minimizar a evasão de clientes na Alura Voz é ter um modelo treinado que vai classificar clientes como potenciais pessoas a deixar a empresa e assim, a equipe de vendas pode agir antes que isso possa, de fato, ocorrer.

Com isso, iniciamos a preparação de dados para serem enviados aos modelos. Pelos estudos da semana 2, nós já tinhamos identificado entradas desinteressantes para o aprendizado, dados categóricos não numéricos que seriam impossíveis de serem reconhecidos por um modelo matemático, além de termos o nosso alvo com valores desbalanceados. Esses dados logo foram tratados para se ajustarem ao modelo.

Os modelos de classificação que definimos serem interessantes para solucionar nosso problema foram o **SVC**, **Decision Tree** e **Random Forest**. No entanto, não entramos em um consenso de qual modelo seria o melhor para o caso. Por isso, decidimos criar os 3 modelos e treiná-los, para que na nossa última semana pudessemos avaliar qual o mais interessante de ser utilizado.

## Optimização - optimizacao.ipynb
