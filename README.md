Projeto de Banco de Dados - E-commerce

Este projeto apresenta a modelagem conceitual, lógica e a implementação de um banco de dados relacional para um cenário de e-commerce. O objetivo é criar um sistema completo de gerenciamento de informações de clientes, pedidos, produtos, fornecedores, pagamentos e entregas.

⚙️ Tecnologias Utilizadas

MySQL Workbench

SQL (Structured Query Language)

🔍 Cenário do Projeto

Foi modelado um sistema de e-commerce que contempla:

Clientes (Pessoa Física ou Jurídica)

Pedidos realizados por clientes

Produtos com fornecedores e controle de estoque

Entregas com status e código de rastreio

Pagamentos múltiplos por pedido

Vendedores que podem também ser fornecedores

🖋️ Modelo Conceitual (EER)

O modelo EER possui as seguintes entidades e relacionamentos:

Cliente

id_cliente (PK)

nome, email, telefone

Especializações: Pessoa Física (CPF, data_nascimento) ou Pessoa Jurídica (CNPJ, razão social)

Pedido

id_pedido (PK), id_cliente (FK)

data_pedido, valor_total

Pagamento

id_pagamento (PK), id_pedido (FK)

tipo, valor, data

Entrega

id_entrega (PK), id_pedido (FK, UNIQUE)

status, cod_rastreio

Produto

id_produto (PK)

nome, preco, descricao

Estoque

id_produto (PK, FK), quantidade

Fornecedor

id_fornecedor (PK)

nome, cnpj

Produto_Fornecedor (relacionamento N:N)

id_produto (FK), id_fornecedor (FK)

Vendedor

id_vendedor (PK), nome, email

Vendedor_Fornecedor (relacionamento opcional)

id_vendedor (FK), id_fornecedor (FK)

📄 Script SQL

O script SQL completo de criação das tabelas está incluído neste repositório no arquivo ecommerce_schema.sql. Ele inclui:

Criação das tabelas com chaves primárias e estrangeiras

Restrições de unicidade, integridade referencial e especializações (PF/PJ)

🔢 Consultas SQL Desenvolvidas

Foram criadas diversas consultas utilizando:

SELECT, WHERE, ORDER BY, GROUP BY, HAVING

Junções entre tabelas (JOIN) para relacionar informações

Atributos derivados com expressões aritméticas

Exemplos de Perguntas Respondidas:

Quantos pedidos cada cliente realizou?

Qual a relação de produtos e seus fornecedores?

Algum vendedor também é fornecedor?

Qual o status de entrega de cada pedido?

📅 Status do Projeto



📆 Futuras Melhorias

Inserção de dados fictícios para testes

Implementação de views e procedures

Criação de um dashboard para análise de vendas

📚 Licença

Este projeto é livre para uso educacional e fins de estudo.
