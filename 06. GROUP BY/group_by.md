# Função GROUP BY

No SQL, a cláusula `GROUP BY` é responsável por agrupar linhas que possuem valores iguais em uma ou mais colunas, permitindo que você aplique funções de agregação sobre cada grupo.

```sql
SELECT Country, COUNT(*) AS QuantidadeClientes FROM Customer GROUP BY Country;
```

**Saída:**

| Country | QuantidadeClientes |
|---|---|
| Argentina | 1 |
| Australia | 1 |
| Austria | 1 |
| Belgium | 1 |
| Brazil | 5 |
| Canada | 8 |
| Chile | 1 |
| Czech Republic | 2 |
| Denmark | 1 |
| Finland | 1 |
| France | 5 |
| Germany | 4 |
| Hungary | 1 |
| India | 2 |
| Ireland | 1 |
| Italy | 1 |
| Netherlands | 1 |
| Norway | 1 |
| Poland | 1 |
| Portugal | 2 |
| Spain | 1 |
| Sweden | 1 |
| USA | 13 |