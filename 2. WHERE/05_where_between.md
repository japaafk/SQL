# Filtrando dados por alcance com BETWEEN

O operador `BETWEEN` serve para retornar valores dentro de um determinado intervalo; com isso, juntamente com ele, é usado o operador `AND`. Normalmente, seu uso está ligado à filtragem de valores numéricos; porém, ele também pode ser usado na filtragem de valores alfabéticos. Abaixo, será usado como exemplo a tabela `Customer`, no qual serão retornados os IDs dos clientes que estão no intervalo entre 10 e 20

```sql
SELECT CustomerId, FirstName, LastName FROM Customer WHERE CustomerId BETWEEN 10 AND 20; 
```

**Saída:**

| CustomerId | FirstName | LastName |
|---|---|---|
| 10 | Eduardo | Martins |
| 11 | Alexandre | Rocha |
| 12 | Roberto | Almeida |
| 13 | Fernanda | Ramos |
| 14 | Mark | Philips |
| 15 | Jennifer | Peterson |
| 16 | Frank | Harris |
| 17 | Jack | Smith |
| 18 | Michelle | Brooks |
| 19 | Tim | Goyer |
| 20 | Dan | Miller |