# Projeto de Administração de Compras de Supermercado

## Descrição

Este projeto é um sistema simples de administração de compras de supermercado, desenvolvido utilizando PostgreSQL. O objetivo é criar um banco de dados para gerenciar informações relacionadas a produtos, categorias, compras e itens de compra em um ambiente de supermercado.

## Estrutura do Banco de Dados

O banco de dados é composto pelas seguintes tabelas:

1. **Categorias**: Armazena as categorias de produtos.
   - `id`: Identificador único da categoria (chave primária).
   - `nome`: Nome da categoria.

2. **Produtos**: Armazena informações sobre os produtos.
   - `id`: Identificador único do produto (chave primária).
   - `nome`: Nome do produto.
   - `preco`: Preço do produto.
   - `categoria_id`: Identificador da categoria do produto (chave estrangeira referenciando a tabela `categorias`).
   - `data_insercao`: Data em que o produto foi inserido no banco de dados (definida automaticamente para a data atual).

3. **Compras**: Armazena informações sobre as compras realizadas.
   - `id`: Identificador único da compra (chave primária).
   - `data`: Data da compra (definida automaticamente para a data atual).
   - `total`: Valor total da compra.

4. **Itens_Compra**: Armazena os itens de cada compra.
   - `id`: Identificador único do item (chave primária).
   - `compra_id`: Identificador da compra (chave estrangeira referenciando a tabela `compras`).
   - `produto_id`: Identificador do produto (chave estrangeira referenciando a tabela `produtos`).
   - `quantidade`: Quantidade do produto comprado.
   - `preco_unitario`: Preço unitário do produto na compra.

## Scripts SQL

Os scripts SQL fornecidos incluem:

1. **Criação das Tabelas**: Scripts para criar as tabelas `categorias`, `produtos`, `compras` e `itens_compra`, incluindo a definição de relacionamentos e restrições.

2. **Inserção de Dados**: Scripts para inserir dados de exemplo nas tabelas, incluindo categorias, produtos e compras.

3. **Consultas de Exemplos**: Exemplos de consultas para recuperar dados e realizar operações básicas de manipulação de dados, como inserção, atualização e exclusão.

## Como Executar

1. **Configuração do Banco de Dados**:
   - Certifique-se de ter o PostgreSQL instalado e em execução.
   - Crie um banco de dados no PostgreSQL para o projeto.

2. **Execução dos Scripts SQL**:
   - Execute o script de criação das tabelas para configurar o banco de dados.
   - Execute o script de inserção de dados para popular o banco de dados com dados de exemplo.
