# Projeto Olist — Análise de Dados de E-commerce

## 1. Sobre o projeto

Este projeto tem como objetivo analisar dados públicos de operações de comércio eletrônico da Olist, buscando identificar padrões de vendas, comportamento comercial e desempenho logístico.

A análise foi desenvolvida utilizando PySpark para processamento dos dados e Looker Studio para construção de um dashboard interativo.

## 2. Fonte dos dados

Foi utilizado o conjunto de dados **Brazilian E-Commerce Public Dataset by Olist**, disponibilizado no Kaggle.

Fonte: https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

A base contém informações anonimizadas sobre pedidos, clientes, produtos, vendedores, pagamentos, avaliações e entregas, referentes ao período de 2016 a 2018.

## 3. Objetivos

- Analisar a evolução mensal dos pedidos e da receita.
- Identificar as categorias com maior participação na receita.
- Avaliar a distribuição geográfica dos pedidos.
- Analisar a situação dos pedidos.
- Investigar o tempo médio e a pontualidade das entregas.
- Comparar preços médios dos produtos e valores médios de frete.

## 4. Ferramentas e tecnologias

- Python
- PySpark
- Google Colab
- Google Drive
- Looker Studio
- CSV

## 5. Etapas do projeto

O desenvolvimento foi organizado nas seguintes etapas:

1. Obtenção e validação dos dados.
2. Análise exploratória dos dados (EDA).
3. Tratamento e preparação dos dados.
4. Construção de bases analíticas.
5. Desenvolvimento do dashboard interativo.
6. Interpretação dos resultados e elaboração das conclusões.

## 6. Estrutura do projeto

```text
projeto-olist-analise-ecommerce/
│
├── README.md
│
├── notebooks/
│   ├── analise_exploratoria.ipynb
│   └── tratamento_preparacao_dados.ipynb
│
├── dados/
│   ├── indicadores_gerais.csv
│   ├── evolucao_mensal_dashboard.csv
│   ├── receita_por_categoria.csv
│   ├── pedidos_por_status.csv
│   ├── pedidos_por_estado.csv
│   ├── preco_frete_faixas.csv
│   ├── pedidos_por_tempo_entrega.csv
│   ├── pontualidade_entregas.csv
│   └── tempo_entrega_por_estado.csv
│
└── documentacao/
    ├── justificativa_problema_e_dados.md
    ├── fontes_e_metodo_coleta.md
    └── interpretacao_resultados_conclusoes.md
```

## 7. Principais resultados

A análise contemplou 99.441 pedidos e identificou os seguintes resultados:

- Receita total de aproximadamente R$ 15,84 milhões, considerando produtos e frete.
- Ticket médio de R$ 160,58.
- São Paulo, Rio de Janeiro e Minas Gerais concentraram aproximadamente 66,60% dos pedidos.
- Tempo médio de entrega de 12,56 dias.
- 93,23% das entregas com datas válidas foram realizadas dentro do prazo.

## 8. Dashboard

O projeto conta com um dashboard interativo desenvolvido no Looker Studio, dividido em três páginas:

- Visão Geral.
- Vendas e Categorias.
- Clientes e Logística.

**Link do dashboard:** [Dashboard](https://datastudio.google.com/reporting/db990dd8-eb9d-4836-8121-03dcfe573845/page/CsSEG/edit)

## 9. Documentação

Os documentos complementares do projeto incluem:

- Justificativa do problema e da escolha dos dados.
- Fontes e método de coleta dos dados.
- Interpretação dos resultados e conclusões.

## 10. Considerações finais

O projeto demonstra a aplicação de ferramentas de processamento e visualização de dados para transformar informações de comércio eletrônico em indicadores relevantes para análise e apoio à tomada de decisões.

A experiência também permitiu desenvolver conhecimentos práticos em Python, PySpark, análise exploratória, preparação de dados e construção de dashboards.
