# Análise Exploratória — Projeto Olist

## 1. Distribuição dos dados

### 1.1 Distribuição dos pedidos por status

A análise dos 99.441 pedidos identificou predominância do status `delivered`, que representa 96.478 registros, aproximadamente 97,02% do total.

Os pedidos cancelados correspondem a 625 registros (0,63%), enquanto 609 pedidos (0,61%) foram classificados como indisponíveis.

Os resultados indicam uma concentração expressiva de pedidos entregues. Entretanto, os registros cancelados e indisponíveis merecem investigação em análises posteriores.

### 1.2 Distribuição dos produtos por categoria

A análise dos 32.951 produtos cadastrados identificou as seguintes categorias com maior quantidade de registros:

- Cama, mesa e banho: 3.029 produtos.
- Esporte e lazer: 2.867 produtos.
- Móveis e decoração: 2.657 produtos.
- Beleza e saúde: 2.444 produtos.
- Utilidades domésticas: 2.335 produtos.

Os resultados demonstram que determinadas categorias possuem maior representatividade no catálogo da plataforma.

Essa distribuição considera os produtos cadastrados, não necessariamente os produtos vendidos.

### 1.3 Principais conclusões

A primeira análise exploratória revelou uma elevada concentração de pedidos entregues e uma distribuição diversificada de produtos entre diferentes categorias.

Também foram identificados pedidos cancelados e indisponíveis, além da necessidade de investigar possíveis produtos sem categoria identificada.


## 2. Análise temporal — Evolução dos pedidos

A análise temporal identificou crescimento expressivo no volume de pedidos ao longo de 2017. Em janeiro daquele ano foram registrados 800 pedidos, enquanto novembro apresentou o maior volume da série, com 7.544 pedidos.

Durante 2018, o volume permaneceu elevado, com destaque para janeiro, que apresentou 7.269 pedidos.

Também foram identificados volumes muito baixos em setembro e outubro de 2016, assim como em setembro e outubro de 2018.

Esses resultados indicam possíveis períodos incompletos de observação ou limitações na cobertura temporal dos dados. Portanto, esses meses precisam ser investigados antes de serem utilizados em comparações e conclusões sobre sazonalidade.

**Principais achados:**
- Crescimento do volume de pedidos durante 2017.
- Maior movimentação em novembro de 2017.
- Manutenção de volumes elevados entre janeiro e agosto de 2018.
- Necessidade de investigar os meses com poucos registros nas extremidades da série histórica.



## 3. Identificação de possíveis outliers

### 3.1 Análise dos preços dos produtos

Foi aplicado o método do Intervalo Interquartil (IQR) para identificar possíveis valores extremos nos preços dos produtos.

Os resultados encontrados foram:

- Primeiro quartil (Q1): R$ 39,89.
- Terceiro quartil (Q3): R$ 130,00.
- Intervalo interquartil (IQR): R$ 90,11.
- Limite superior: R$ 265,16.
- Quantidade de possíveis outliers: 8.896 registros.

Todos os 8.896 registros identificados estão acima do limite superior, representando aproximadamente 7,90% dos itens analisados.

Esse resultado demonstra a presença de produtos com preços significativamente elevados em relação à maior parte dos registros.

### 3.2 Análise dos valores de frete

Na análise dos valores de frete, foram identificados os seguintes resultados:

- Primeiro quartil (Q1): R$ 12,90.
- Terceiro quartil (Q3): R$ 20,96.
- Intervalo interquartil (IQR): R$ 8,06.
- Limite inferior: R$ 0,81.
- Limite superior: R$ 33,05.
- Quantidade de possíveis outliers: 12.224 registros.

Foram identificados 509 registros abaixo do limite inferior e 11.715 acima do limite superior, correspondendo a aproximadamente 10,85% dos itens analisados.

A maior parte dos possíveis valores extremos está concentrada nos fretes mais elevados.

### 3.3 Principais conclusões

A análise identificou possíveis outliers tanto nos preços dos produtos quanto nos valores de frete. Os fretes apresentaram maior proporção de valores extremos (10,85%) em comparação aos preços (7,90%).

Os resultados reforçam a presença de distribuições assimétricas, com alguns valores significativamente superiores à concentração principal dos dados.

É importante destacar que valores extremos não representam necessariamente erros, podendo corresponder a situações comerciais legítimas. Nenhum registro foi removido ou alterado durante essa análise.


## 4 Análise de correlação entre preço e frete

Foi calculado o coeficiente de correlação entre os preços dos produtos e os respectivos valores de frete, obtendo o resultado de **0,4142**.

O resultado indica uma correlação positiva moderada entre as variáveis, sugerindo que produtos com preços mais elevados tendem a apresentar valores de frete também maiores.

Essa relação demonstra uma associação entre preço e frete, mas não significa necessariamente que uma variável seja responsável pelo comportamento da outra.

### 4.1 Principais conclusões

A análise identificou uma relação positiva moderada entre os preços dos produtos e os valores de frete. Esse resultado complementa as análises estatísticas anteriores e contribui para compreender o comportamento dos valores financeiros presentes nos pedidos.



## 5. Distribuição geográfica dos clientes e pedidos

### 5.1 Clientes únicos por estado

A análise dos clientes únicos, utilizando a coluna `customer_unique_id`, identificou maior concentração nos seguintes estados:

- São Paulo (SP): 40.302 clientes.
- Rio de Janeiro (RJ): 12.384 clientes.
- Minas Gerais (MG): 11.259 clientes.
- Rio Grande do Sul (RS): 5.277 clientes.
- Paraná (PR): 4.882 clientes.

São Paulo apresenta a maior concentração de consumidores, seguido por Rio de Janeiro e Minas Gerais.

### 5.2 Distribuição dos pedidos por estado

A análise dos pedidos, utilizando a identificação `order_id`, apresentou os seguintes destaques:

- São Paulo (SP): 41.746 pedidos.
- Rio de Janeiro (RJ): 12.852 pedidos.
- Minas Gerais (MG): 11.635 pedidos.
- Rio Grande do Sul (RS): 5.466 pedidos.
- Paraná (PR): 5.045 pedidos.

Os resultados demonstram que São Paulo concentra o maior volume de pedidos, seguido por Rio de Janeiro e Minas Gerais.

### 5.3 Principais conclusões

A análise geográfica identificou forte concentração de clientes e pedidos nos estados da região Sudeste, especialmente em São Paulo, Rio de Janeiro e Minas Gerais.

Também foi observada uma diferença entre a quantidade de clientes únicos e a quantidade de pedidos, indicando que alguns consumidores realizaram mais de uma compra.

Esses resultados demonstram a importância da região Sudeste para a operação da Olist e permitem compreender melhor a distribuição geográfica de seus consumidores.



## 6. Prazo de entrega e avaliação dos clientes

### 6.1 Análise do prazo de entrega

A análise considerou 96.470 pedidos entregues com datas válidas.

- Prazo médio de entrega: 12,50 dias.
- Prazo mediano de entrega: 10 dias.
- Menor prazo: 0 dias.
- Maior prazo: 210 dias.
- Desvio padrão: 9,56 dias.

Os resultados mostram variação nos prazos de entrega. A média superior à mediana indica que entregas com prazos mais longos influenciam o resultado geral.

### 6.2 Situação das entregas

A comparação entre a data estimada e a data real de entrega identificou:

- Entregues no prazo: 89.936 pedidos (93,23%).
- Entregues com atraso: 6.534 pedidos (6,77%).

A maioria dos pedidos foi entregue dentro do prazo estimado. Entretanto, os 6.534 pedidos atrasados merecem atenção.

### 6.3 Relação entre prazo de entrega e avaliação dos clientes

A comparação das avaliações dos clientes apresentou os seguintes resultados:

| Indicador | Atrasado | No prazo |
|---|---:|---:|
| Pedidos avaliados | 6.381 | 89.442 |
| Nota média | 2,27 | 4,29 |
| Nota mediana | 1,0 | 5,0 |

Os pedidos atrasados apresentaram avaliações consideravelmente inferiores às dos pedidos entregues no prazo. A diferença nas médias e medianas indica uma associação expressiva entre atrasos e menor satisfação dos consumidores.

### 6.4 Principais conclusões

- 93,23% dos pedidos foram entregues dentro do prazo estimado.
- Os pedidos atrasados apresentaram nota média de 2,27, enquanto os entregues no prazo obtiveram média de 4,29.
- A mediana de avaliação foi 1 para pedidos atrasados e 5 para pedidos entregues no prazo.
- Os resultados indicam que o cumprimento dos prazos está associado a avaliações mais positivas dos clientes.

O prazo de entrega representa um aspecto importante da experiência do consumidor. Os resultados sugerem que atrasos estão associados à redução da satisfação dos clientes, reforçando a importância de acompanhar e melhorar o desempenho logístico.


## 7. Relação entre quantidade de produtos, preço e frete

### 7.1 Consolidação dos pedidos

A análise utilizou a tabela de itens dos pedidos, agrupando os registros por pedido para calcular:

- Quantidade de itens por pedido.
- Valor total dos produtos.
- Valor total do frete.

Essa consolidação permitiu avaliar o relacionamento entre as variáveis no nível de cada pedido.

### 7.2 Análise de correlação

Os coeficientes de correlação identificados foram:

| Relação entre variáveis | Correlação |
|---|---:|
| Quantidade de itens x Valor dos produtos | 0,1531 |
| Quantidade de itens x Valor do frete | 0,4369 |
| Valor dos produtos x Valor do frete | 0,4128 |

Os resultados indicam:

- Quantidade de itens e valor dos produtos: correlação positiva fraca.
- Quantidade de itens e valor do frete: correlação positiva moderada.
- Valor dos produtos e valor do frete: correlação positiva moderada.

### 7.3 Visualização dos resultados

Foi criado um mapa de calor (heatmap) para representar visualmente os coeficientes de correlação entre as três variáveis analisadas.

A visualização facilita a identificação da intensidade e da direção das relações entre quantidade de itens, valor dos produtos e valor do frete.

### 7.4 Principais conclusões

- A quantidade de itens apresenta uma relação positiva fraca com o valor total dos produtos.
- A quantidade de itens apresenta uma relação positiva moderada com o valor total do frete.
- O valor dos produtos também apresenta uma relação positiva moderada com o valor do frete.
- Os resultados representam associações estatísticas e não comprovam relações de causalidade.

Os pedidos com maior quantidade de itens ou maior valor de produtos tendem a apresentar valores totais de frete mais elevados. Entretanto, a quantidade de itens não determina necessariamente o valor total da compra.


