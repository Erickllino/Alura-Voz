# 1° Challenge de Dados -  Alura

Esse projeto segue a metodologia de atuar em uma empresa hipotetica para experênciar as atividades de um cientisda de dados utilizando, a empresa foi nomeada Alura Voz.

A Alura Voz, uma empresa hipotética de telecomunicações, me contratou para atuar como cientista de dados na equipe de vendas. Logo na minha primeira semana, a liderança deixou claro que era essencial realizar um estudo sobre o churn da empresa. Foi explicado que o churn representa a saída de clientes e que, quando isso acontece, a empresa não apenas perde consumidores, mas também sofre impactos negativos em sua receita.

Diante desse cenário, recebi a missão de buscar, em um prazo de quatro semanas, uma alternativa para minimizar a saída de clientes. Para isso, fui apresentado a um conjunto de dados da Alura Voz, contendo diversas informações sobre os clientes, incluindo se eles permaneceram ou não na empresa.

Antes de propor qualquer solução, compreendi que o primeiro passo era analisar cuidadosamente os dados disponíveis. Após uma breve reunião, decidi que minha primeira semana seria dedicada a entender a estrutura do banco de dados, identificar os tipos de informações contidas nele, verificar a existência de valores inconsistentes e corrigi-los, caso necessário.

## Limpeza dos dados - limpeza.ipynb

### Dados

Ao observar a Base de dados da Alura Voz, verifiquei que essa é uma base disponibilizada via API em formato JSON com várias camandas de dados.

Junto a esses dados também foi disponibilizado o dicionário dos dados que nele contém todas as informações sobre as colunas do banco de dados.

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

Feito o reconhecimento e tratamento de dados, dei continuidade do trabalho, agora, analisando os dados. Conluí que preciso fazer uma análise gráfica para entender quais as variáveis que são relacionadas com o churn para que a equipe de vendas tenha uma noção do cenário atual, e também para que nós possa entender de uma forma mais clara e formar possíveis hipóteses do que está acontecendo com os clientes.

Planejei assim, fazer uma **análise estatística** dos dados, verificar os **tipos de dados** que temos, gerar gráficos de **distribuição de dados binários ou categóricos**, plot de **Boxplots** para detecção de outliers e **matriz de correlação**. Assim, de cada análise e verificação consegui identificar a relação dos dados com nosso alvo, identificar valores incoerêntes e/ou desnecessários e támbem entender ainda mais os dados que temos.



## Modelos de Machine Learning - modelos.ipynb

Ao revisar e discutir todas as análises realizadas na segunda semana, concluí que uma estratégia eficaz para minimizar a evasão de clientes na Alura Voz seria treinar um modelo capaz de identificar clientes com maior probabilidade de cancelar o serviço. Dessa forma, a equipe de vendas poderia agir preventivamente antes que a saída realmente ocorresse.

Com essa decisão tomada, iniciei a preparação dos dados para alimentar os modelos. Durante os estudos da segunda semana, já havia identificado variáveis pouco relevantes para o aprendizado, além de dados categóricos não numéricos, que precisavam ser transformados para serem interpretados pelos modelos matemáticos. Além disso, percebi que a variável-alvo estava desbalanceada, o que exigia ajustes para evitar viés nos resultados. Assim, tratei esses dados para adequá-los ao modelo.

Os algoritmos de classificação escolhidos para resolver esse problema foram **SVC**, **Decision Tree** e **Random Forest**. No entanto, ainda não havia um consenso sobre qual deles seria o mais adequado para essa situação. Por isso, decidi criar e treinar os três modelos, para que, na última semana, pudesse avaliar qual deles apresentava o melhor desempenho.

## Optimização - optimizacao.ipynb
