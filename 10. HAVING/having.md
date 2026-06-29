# Filtrando dados agrupados com HAVING

A cláusula `HAVING` é usada para filtar os resultados agregados, sendo semelhante ao `WHERE`, porém utilizada após o agrupamento das linhas. **Nota:** é essencial que existam funções de agregação ou que as linhas estejam agrupadas para utilizar esse operador. No exemplo abaixo, retornaremos os países que possuem mais de 5 clientes

```sql
SELECT Country, COUNT(*) AS QuantidadeCliente FROM Customer GROUP BY Country HAVING COUNT(*) > 5 ORDER BY QuantidadeCliente DESC;
```

**Saída:**

| Country | QuantidadeCliente |
|---|---|
| USA | 13 |
| Canada | 8 |