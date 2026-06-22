# Função ORDER BY

A função `ORDER BY` permite organizar o resultado de saída, por padrão os resultados são apresentados em ordem crescente. No exemplo abaixo, os nomes serão apresentados em ordem alfabética

```sql
SELECT FirstName, LastName FROM Employee ORDER BY LastName;
```

**Saída:**

| FirstName | LastName |
|---|---|
| Andrew | Adams |
| Laura | Callahan |
| Nancy | Edwards |
| Steve | Johnson |
| Robert | King |
| Michael | Mitchell |
| Margaret | Park |
| Jane | Peacock |