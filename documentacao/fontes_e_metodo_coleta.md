# Fontes e Método de Coleta dos Dados — Projeto Olist

## 1. Fonte dos dados

Os dados utilizados neste projeto foram obtidos por meio do conjunto de dados público **Brazilian E-Commerce Public Dataset by Olist**, disponibilizado na plataforma Kaggle.

O conjunto apresenta informações anonimizadas sobre operações de comércio eletrônico realizadas no Brasil entre 2016 e 2018.

Fonte: https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

## 2. Método de obtenção

A base de dados foi baixada da plataforma Kaggle em formato CSV e armazenada no Google Drive para utilização no ambiente Google Colab.

Posteriormente, os arquivos foram carregados utilizando PySpark, permitindo a leitura, validação e processamento dos dados.

## 3. Estrutura dos dados

O conjunto original é composto por nove arquivos CSV:

1. `olist_customers_dataset.csv` — informações dos clientes.
2. `olist_geolocation_dataset.csv` — informações geográficas.
3. `olist_order_items_dataset.csv` — itens associados aos pedidos.
4. `olist_order_payments_dataset.csv` — informações de pagamentos.
5. `olist_order_reviews_dataset.csv` — avaliações dos pedidos.
6. `olist_orders_dataset.csv` — informações gerais dos pedidos.
7. `olist_products_dataset.csv` — informações dos produtos.
8. `olist_sellers_dataset.csv` — informações dos vendedores.
9. `product_category_name_translation.csv` — tradução dos nomes das categorias.

## 4. Processo de leitura e validação

Após a obtenção dos arquivos, foi realizada a leitura dos dados utilizando PySpark no Google Colab.

O processo de validação contemplou:

- Verificação da quantidade de registros e colunas.
- Conferência dos tipos de dados.
- Verificação de identificadores únicos.
- Identificação de registros duplicados.
- Verificação de valores nulos.
- Conferência da integridade dos relacionamentos entre as tabelas.

Essas verificações permitiram avaliar a consistência dos dados antes das etapas seguintes do projeto.

## 5. Processamento e preparação

Os dados foram processados utilizando PySpark, com operações de limpeza, ajustes e preparação das informações necessárias às análises.

Foram realizados relacionamentos entre tabelas por meio de identificadores, possibilitando a construção de bases analíticas específicas para os indicadores do projeto.

Os arquivos originais foram preservados, e as bases resultantes foram exportadas em formato CSV para utilização no Looker Studio.

## 6. Considerações sobre a origem dos dados

Por se tratar de uma base pública e anonimizada, não foram utilizados dados pessoais identificáveis dos clientes.

As análises foram realizadas considerando as informações disponibilizadas no conjunto de dados e respeitando suas limitações, especialmente quanto ao período histórico e às variáveis existentes.