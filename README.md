# 🏠 House-Sales-in-King-County-USA
 Projeto fictício. O conteúdo apresentado neste projeto, incluindo a empresa, as perguntas e os dados, não são reais. A ideia desse projeto foi inspirada no [blog](https://medium.com/@meigarom/os-5-projetos-de-data-science-que-far%C3%A1-o-recrutador-olhar-para-voc%C3%AA-c32c67c17cc9)📝 
 Os dados utilizados foram retirados do [site](https://www.kaggle.com/datasets/harlfoxem/housesalesprediction?resource=download)🔎. O objetivo é fornecer um estudo de caso fictício para exemplificar a aplicação de técnicas e metodologias em um contexto simulado.
***
## 🚀 Contexto e Descrição do Desafio fictício
 A House Rocket é uma plataforma digital que atua no mercado imobiliário, utilizando tecnologia para simplificar e agilizar a compra e venda de imóveis. Como Cientista de Dados contratado pela empresa, sua missão é encontrar as melhores oportunidades de negócio nesse setor. O objetivo principal do CEO da House Rocket é maximizar a receita da empresa por meio da aquisição estratégica de imóveis bem localizados e com preços atrativos, visando a revenda posterior com lucro.

#### As questões que devem ser respondidas são:
 - Quais casas o CEO da House Rocket deveria comprar e por qual preço de compra?

 - Uma vez a casa em posse da empresa, qual o melhor momento para vendê-las e qual seria o preço da venda?

 - A House Rocket deveria fazer uma reforma para aumentar o preço da venda? Quais seriam as sugestões de mudanças? Qual o incremento no preço dado por cada opção de reforma?
***

## 🛠️ Etapas para Solucionar o Problema de Negócio:

 1. Coleta de dados via Kaggle: Obtendo os dados relevantes para análise da plataforma Kaggle.
 2. Entendimento do negócio: Compreendendo os objetivos e desafios da House Rocket.
 3. Tratamento de dados: Realizando transformações e limpeza dos dados para garantir sua qualidade.
 4. Exploração de dados: Analisando os dados em busca de padrões e insights.
 5. Formulação de hipóteses: Elaborando suposições sobre os fatores que influenciam os preços de venda.
 6. Análise estatística: Aplicando técnicas estatísticas para testar e validar as hipóteses.
 7. Resultados para o negócio: Avaliando os insights obtidos em termos de relevância e impacto para a empresa.
 8. Conclusão e recomendações: Apresentando conclusões e oferecendo recomendações claras e direcionadas para a House Rocket.

***

## 📋 Descrição dos atributos presentes nos dados

| Atributos | Descrição |
|----------|----------|
| id  | Número de Indentificação do imóvel  | 
| date  | Data em que a casa foi vendida  | 
|price | Preço cobrado pelo proprietário para a venda|
|bedrooms | Quantidade de quartos|
|bathrooms | Quantidade de Banheiros (1 - Banheiro completo, 0.5 - Banheiro sem chuveiro, 0.25 - Somentee chuveiro)|
|sqft_living | Área em pés quadrados de área habitada|
|sqft_lot | Área em pés quadrados de terreno|
|floors | Quantidade de andares do imóvel(1 - Andar completo, 0.5 - Andar Parcial)|
|waterfront | Representa se a vista do imóvel para água, como um lago, rio, oceano ou mar(0 - Não, 1 - Sim)|
|view | Indice que representa a qualidade da vista da propriedade, variando de 0 até 4(0 - Baixo, 4 - Alto)|
|condition | Indice que representa a condição da propriedade, variando de 1 até 5(0 - Baixo, 5 - Alto)|
|grade | Indice que representa a avalização do imóvel, variando de 1 até 13(1 - Baixo, 13 - Alto)|
|sqft_above | Área em pés quadrados no andar superior|
|sqft_basement | Área em pés quadrados no porão (0 - Casa sem porão)|
|yr_built | Ano da construção da propriedade|
|yr_renovated | Ano da reforma da propriedade (0 - Casa nunca reformadas)|
|zipcode | Código de Endereço Postal ou CEP da casa| 
|lat | Latitude| 
|long | Longitude| 
|sqft_living15 | Média da área habitada em pés quadrados dos 15 vizinhos mais próximos| 
|sqft_lot15 | Média da área do lote em pés quadrados dos 15 vizinhos mais próximos| 

***

## 📌 Levantamento de Hipóteses sobre o Comportamento do Negócio

| Hipóteses |
|-----------|
|H1: Imóveis com mais quartos (bedrooms) têm preços de venda mais altos.|
|H2: Imóveis com mais banheiros (bathrooms) têm preços de venda mais altos.|
|H3: Imóveis com melhores avaliações (grade) têm preços de venda mais altos.|
|H4: Imóveis com vista para o mar, lago, rio ou oceano têm preços de venda mais altos.|
|H5: Imóveis construídos depois de 1960 são mais baratos para comprar e lucram mais na hora da revenda.|
|H6: Casas reformadas têm preços de venda mais altos.|
|H7: Imóveis localizados em áreas com melhores vistas (view) têm preços de venda mais altos.|
|H8: Imóveis com mais andares (floors) têm preços de venda mais altos.|

***
## 💡Resultado das Hipóteses e solução para as questões do Negócio 

### 📄 Hipóteses 

| Hipóteses | Resultados | Análises | Transformando Dados em Insights Estratégicos |
|-----------|------------|----------|----------------------------------------------|
| H1: Imóveis com mais quartos (bedrooms) têm preços de venda mais altos. | Falso | Após análise do gráfico, observa-se que o número de quartos não é o único fator determinante para o preço dos imóveis. De fato, é possível observar que casas com 8 quartos possuem uma média de preço maior em comparação com casas com 10 ou 11 quartos. | Negócio: Número de quartos é um fator irrelevante no investimento de imóveis. |
| H2: Imóveis com mais banheiros (bathrooms) têm preços de venda mais altos. | Verdadeiro | Após análise do gráfico, fica evidente que imóveis com mais de 5 banheiros apresentam, em média, preços mais elevados em comparação com aqueles que possuem menos banheiros. Isso sugere que a quantidade de banheiros é um fator relevante na determinação do preço de um imóvel. | Negócio: Investir em imóveis com mais banheiros. |
| H3: Imóveis com melhores avaliações (grade) têm preços de venda mais altos. | Verdadeiro | Após a análise dos gráficos, fica evidente que há uma relação positiva entre a avaliação do imóvel e o seu preço de venda. Quanto maior a avaliação do imóvel, maior tende a ser o seu preço de venda. Isso sugere que os compradores estão dispostos a pagar mais por imóveis com uma avaliação mais alta. | Negócio: Investir em imóveis com avaliações maiores. |
| H4: Imóveis com vista para o mar, lago, rio ou oceano têm preços de venda mais altos. | Verdadeiro | Após uma análise cuidadosa, é possível constatar que imóveis com vista para o mar, lago, rio ou oceano têm preços de venda significativamente mais altos em comparação com imóveis sem vista. Em média, o valor dos imóveis com vista é cerca de 211,7% mais alto do que aqueles sem vista. | Negócio: Investir em imóveis com vista para a água. | 
| H5: Imóveis construídos depois de 1960 são mais baratos para comprar e lucram mais na hora da revenda. | Falso | Após uma análise mais detalhada, constata-se que o ano de construção dos imóveis não afetam seu valor de venda. | Negócio: O ano da construção é um fator irrelevante no investimento de imóveis. |
| H6: Casas reformadas têm preços de venda mais altos. | Verdadeiro | Após análise dos dados, pode-se confirmar que casas que passaram por reformas têm seu valor aumentado em média em cerca de 43,2% | Negócio: Investir em casas não reformadas e reforma-las. |
| H7: Imóveis localizados em áreas com melhores vistas (view) têm preços de venda mais altos. | Verdadeiro | Após análise dos dados, é evidente que imóveis com vistas privilegiadas, têm preços de venda mais elevados em comparação com imóveis sem essa característica. |Negócio: Investir em imóveis com boa vista. |
|H8: Imóveis com mais andares (floors) têm preços de venda mais altos. | Falso | Após análise dos dados, constata-se que o número de andares dos imóveis não influenciam tanto no seu valor de venda. | Negócio: Número de quartos é um fator irrelevante no investimento de imóveis. |


### ⚙️ Questões do Negócio

 - As questões que devem ser respondidas como Cientista de Dados são:

 - Quais casas o CEO da House Rocket deveria comprar e por qual preço de compra?

 - Uma vez a casa em posse da empresa, qual o melhor momento para vendê-las e qual seria o preço da venda?

 - A House Rocket deveria fazer uma reforma para aumentar o preço da venda? Quais seriam as sugestões de mudanças? Qual o incremento no preço dado por cada opção de reforma?

 As questões foram respondidas e os objetivos foram alcançados. Para selecionar as casas que a imobiliária deve comprar, considerou-se a condição da casa com uma avaliação igual a 5 e um preço abaixo da mediana, agrupados por código postal. Para a venda das casas, agrupou-se de acordo com o código postal e estação do ano, calculando-se a mediana. Casas com preços abaixo da mediana tiveram seu valor de venda definido como 1,25 vezes o seu preço, enquanto casas com preços acima da mediana tiveram seu valor de venda definido como 1,1 vezes o seu valor. Como resultado, verificou-se que as melhores estações do ano para a venda dos imóveis são a primavera e o verão.

 Além disso, foi observado que as reformas nos imóveis têm um impacto significativo no valor. Em média, casas que passaram por reformas têm um valor cerca de 43,2% maior do que casas sem reformas. Com base nisso, as melhores sugestões para aumentar o valor dos imóveis seriam melhorar as condições da casa e a vista dos imóveis.








