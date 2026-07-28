# RELACIONANDO CHAVES NO SQL

Para realizar consultas mais complexas no SQL, é fundamental entender como relacionar as chaves (PRIMARY KEY e FOREIGN KEY). Para ilustrar isso na prática, imagine um cenário em que precisamos identificar os 10 clientes com as maiores faturas do banco de dados

Para saber se alguma coluna de uma determinada tabela faz conexão com outra, podemos usar o comando `.schema nome_da_tabela`. Em seguida, a saída retornada é o `CREATE TABLE` da tabela, que mostrará os tipos de valores que as colunas aceitam e, caso façam conexão, o tipo de chave que elas possuem

<ins>**Passo a passo:**</ins>

**Passo 1:**
Selecionaremos os clientes que mais gastaram na compra dos álbuns
```sql
SELECT * FROM Invoice ORDER BY Total DESC LIMIT 10;
```

Saída:

| InvoiceId | CustomerId | InvoiceDate | BillingAddress | BillingCity | BillingState | BillingCountry | BillingPostalCode | Total |
|---|---|---|---|---|---|---|---|---|
| 404 | 6 | 2025-11-13 00:00:00 | Rilská 3174/6 | Prague | NULL | Czech Republic | '14300' | 25.86 |
| 299 | 26 | 2024-08-05 00:00:00 | 2211 W Berry Street | Fort Worth | TX | USA | '76110' | 23.86 |
| 96 | 45 | 2022-02-18 00:00:00 | Erzsébet krt. 58. | Budapest | NULL | Hungary | H-1073 | 21.86 |
| 194 | 46 | 2023-04-28 00:00:00 | 3 Chatham Street | Dublin | Dublin | Ireland | NULL | 21.86 |
| 89 | 7 | 2022-01-18 00:00:00 | Rotenturmstraße 4, 1010 Innere Stadt | Vienne | NULL | Austria | '1010' | 18.86 |
| 201 | 25 | 2023-05-29 00:00:00 | 319 N. Frances Street | Madison | WI | USA | '53703' | 18.86 |
| 88 | 57 | 2022-01-13 00:00:00 | Calle Lira, 198 | Santiago | NULL | Chile | NULL | 17.91 |
| 306 | 5 | 2024-09-05 00:00:00 | Klanova 9/506 | Prague | NULL | Czech Republic | '14700' | 16.86 |
| 313 | 43 | 2024-10-06 00:00:00 | 68, Rue Jouvence | Dijon | NULL | France | '21000' | 16.86 |
| 103 | 24 | 2022-03-21 00:00:00 | 162 E Superior Street | Chicago | IL | USA | '60611' | 15.86 |

**Passo 2:**
Utilizamos o comando `.schema` para descobrir as conexões da tabela
```
.schema Invoice

CREATE TABLE Invoice (
    InvoiceId       INTEGER PRIMARY KEY,
    CustomerId      INTEGER NOT NULL,
    InvoiceDate     DATETIME NOT NULL,
    BillingAddress  TEXT,
    BillingCity     TEXT,
    BillingState    TEXT,
    BillingCountry  TEXT,
    BillingPostalCode TEXT,
    Total           NUMERIC NOT NULL,
    FOREIGN KEY (CustomerId) REFERENCES Customer(CustomerId)
);
```

**Passo 3:**
Analisando o `CREATE TABLE` da tabela, podemos observar que a coluna `CustomerId` é uma foreign key da tabela `Customer`

**Passo 4:**
Agora, buscaremos saber quem são esses clientes, identificando-os por meio do seu ID. Para isso, vamos utilizar a sequência de comandos:
```sql
SELECT FirstName, LastName FROM Customer WHERE CustomerId IN (SELECT CustomerId FROM Invoice ORDER BY Total DESC) LIMIT 10;
```

Saída:

| FirstName | LastName |
|---|---|
| Luís | Gonçalves |
| Leonie | Köhler |
| François | Tremblay |
| Bjørn | Hansen |
| František | Wichterlová |
| Helena | Holý |
| Astrid | Gruber |
| Daan | Peeters |
| Kara | Nielsen |
| Eduardo | Martins |

Assim, descobrimos o primeiro e o último nome dos clientes que mais gastaram em ordem decrescente