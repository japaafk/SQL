# Selecionando colunas específicas

O caracter `*` tem como função selecionar todas as colunas de uma determinada tabela, porém você também pode especificar qual(is) coluna(s) você quer ver apenas escrevendo seu nome. Neste caso, dentro da tabela `employee` queremos selecionar somente as colunas `FirstName` e `LastName` sem que apareçam outras informações

```sql
SELECT FirstName, LastName FROM employee;
```

Saída:

| FirstName | LastName |
|---|---|
| Andrew | Adams |
| Nancy | Edwards |
| Jane | Peacock |
| Margaret | Park |
| Steve | Johnson |
| Michael | Mitchell |
| Robert | King |
| Laura | Callahan |