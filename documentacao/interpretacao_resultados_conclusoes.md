# Interpretação dos Resultados e Conclusões — Projeto Olist

## 1. Objetivo da análise

Este relatório apresenta a interpretação dos principais resultados obtidos na análise do Brazilian E-Commerce Public Dataset by Olist.

O objetivo foi investigar o comportamento das vendas, a distribuição geográfica dos pedidos, o desempenho das entregas e a relação entre preços dos produtos e valores de frete, utilizando PySpark para processamento e análise dos dados e Looker Studio para a construção do dashboard.

## 2. Indicadores gerais

A base analisada contém **99.441 pedidos**, com receita total de aproximadamente **R$ 15,84 milhões**, considerando a soma dos preços dos produtos e dos valores de frete.

O ticket médio calculado foi de **R$ 160,58 por pedido**.

Foram identificados 96.478 pedidos com status de entrega concluída, representando aproximadamente 97,02% do total de pedidos.

Esses indicadores demonstram o volume expressivo de operações da plataforma durante o período analisado.

## 3. Desempenho das vendas

A análise da evolução mensal permite acompanhar as variações no volume de pedidos e na receita ao longo do período disponível.

A comparação entre essas duas métricas ajuda a identificar períodos de maior e menor movimentação comercial e possíveis diferenças entre crescimento do número de pedidos e crescimento da receita.

Na análise por categoria, destacaram-se:

- Saúde e Beleza: R$ 1.441.248,07.
- Relógios e Presentes: R$ 1.305.541,61.
- Cama, Mesa e Banho: R$ 1.241.681,72.
- Esportes e Lazer: R$ 1.156.656,48.
- Informática e Acessórios: R$ 1.059.272,40.

Essas categorias representam importantes participações no faturamento total analisado.

## 4. Distribuição geográfica dos pedidos

A distribuição por estado demonstra uma concentração significativa dos pedidos na região Sudeste.

Os três estados com maior quantidade de pedidos foram:

- São Paulo: 41.746 pedidos.
- Rio de Janeiro: 12.852 pedidos.
- Minas Gerais: 11.635 pedidos.

Juntos, esses estados representam aproximadamente 66,60% dos pedidos.

Esse resultado evidencia a importância do mercado consumidor desses estados para a operação da plataforma.

## 5. Desempenho logístico

O tempo médio geral de entrega foi de **12,56 dias**, considerando 96.470 pedidos entregues com datas válidas para o cálculo.

A distribuição dos prazos foi:

- Até 7 dias: 26.099 pedidos (27,05%).
- De 8 a 14 dias: 40.189 pedidos (41,66%).
- De 15 a 21 dias: 17.697 pedidos (18,34%).
- Acima de 21 dias: 12.485 pedidos (12,94%).

Na análise de pontualidade, foram identificados:

- Entregas no prazo: 89.936 (93,23%).
- Entregas atrasadas: 6.534 (6,77%).

Os resultados indicam um percentual elevado de entregas realizadas dentro do prazo previsto. Entretanto, os atrasos identificados representam uma oportunidade de melhoria logística.

A comparação entre os estados também revela diferenças no tempo médio de entrega. Roraima apresentou média de 29,39 dias, enquanto São Paulo apresentou média de 8,76 dias.

## 6. Relação entre preço dos produtos e frete

A análise por faixa de preço mostrou que o frete médio aumenta conforme as faixas de preço dos produtos aumentam.

Na faixa de até R$ 39,90, o preço médio foi de R$ 25,71 e o frete médio de R$ 14,36.

Na faixa acima de R$ 349,90, o preço médio foi de R$ 713,95 e o frete médio de R$ 42,76.

Esse comportamento sugere uma relação entre o valor dos produtos e o custo de envio, embora a análise por faixas não permita afirmar que o aumento do preço seja a causa direta do aumento do frete.

## 7. Conclusão

A análise dos dados da Olist permitiu identificar características importantes do desempenho comercial e logístico da plataforma.

Os resultados apontam concentração de pedidos em determinados estados, destaque de algumas categorias no faturamento e um percentual elevado de entregas realizadas dentro do prazo.

Também foram identificadas diferenças relevantes no tempo médio de entrega entre os estados e variações no valor médio do frete conforme a faixa de preço dos produtos.

O projeto demonstrou como ferramentas de processamento de dados, como PySpark, e ferramentas de visualização, como Looker Studio, podem ser utilizadas em conjunto para transformar grandes volumes de dados em informações úteis para a tomada de decisões.

Conclui-se que a análise de dados permite compreender melhor o funcionamento da operação, identificar oportunidades de melhoria e apoiar decisões relacionadas às vendas, à logística e à experiência dos consumidores.