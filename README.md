# Distinct-manual-
A declaração é usada para retornar apenas valores distintos (diferentes).SQL SELECIONAR declaração distinta

------

# -------SQL SELECIONAR declaração distinta-----

------

## A instrução nÍTIDA SQL SELECT

A declaração é usada para retornar apenas valores distintos (diferentes).`SELECT DISTINCT`

Dentro de uma tabela, uma coluna muitas vezes contém muitos valores duplicados; e às vezes você só quer listar os diferentes valores (distintos).

### SELECIONE Sintaxe DISTINTA

SELECT DISTINCT *column1*, *column2, ...*
FROM *table_name*;

------

## Banco de dados de demonstração

Abaixo está uma seleção da tabela "Clientes" no banco de dados de amostras northwind:

| CustomerID | CustomerName                       | ContactName        | Address                       | City        | PostalCode | Country |
| :--------- | :--------------------------------- | :----------------- | :---------------------------- | :---------- | :--------- | :------ |
| 1          | Alfreds Futterkiste                | Maria Anders       | Obere Str. 57                 | Berlin      | 12209      | Germany |
| 2          | Ana Trujillo Emparedados y helados | Ana Trujillo       | Avda. de la Constitución 2222 | México D.F. | 05021      | Mexico  |
| 3          | Antonio Moreno Taquería            | Antonio Moreno     | Mataderos 2312                | México D.F. | 05023      | Mexico  |
| 4          | Around the Horn                    | Thomas Hardy       | 120 Hanover Sq.               | London      | WA1 1DP    | UK      |
| 5          | Berglunds snabbköp                 | Christina Berglund | Berguvsvägen 8                | Luleå       | S-958 22   | Sweden  |

------

## SELECIONAR exemplo sem distinto

A seguinte instrução SQL seleciona todos os valores (incluindo as duplicatas) da coluna "País" na tabela "Clientes":

### Exemplo

SELECT Country FROM Customers;

Agora, vamos usar a declaração e ver o resultado.`SELECT DISTINCT`

------

------

## SELECIONE EXEMPLOS DISTINTOS

A seguinte instrução SQL seleciona apenas os valores DISTINTOS da coluna "País" na tabela "Clientes":

### Exemplo

SELECT DISTINCT Country FROM Customers;

A seguinte declaração SQL lista o número de diferentes países clientes (distintos):

### Exemplo

SELECT COUNT(DISTINCT Country) FROM Customers;

**Nota: O exemplo acima não funcionará no Firefox!** Como o COUNT (DISTINCT *column_name*) não é suportado nos bancos de dados do Microsoft Access. O Firefox está usando o Microsoft Access em nossos exemplos.

Aqui está a solução alternativa para o MS Access:

### Exemplo

SELECT Count(*) AS DistinctCountries
FROM (SELECT DISTINCT Country FROM Customers);



**EXEMPLO 1**

Eu quero o id e nome dos vendedores que venderam produtos mais caros que 500

**SELECT**  * **FROM** tb_sale **INNER JOIN** tb_seller **ON** tb_seller.id = tb_sale.seller_id **WHERE** price > 500 

neste exemplo acima, se o vendedor efetuou duas vendas, o nome aparecerá duplicado no resultado, para nao aparecer duplicado incluir o DISTINCT na formula

**SELECT DISTINCT**  **FROM** tb_sale **INNER JOIN** tb_seller **ON** tb_seller.id = tb_sale.seller_id **WHERE** price > 500 
