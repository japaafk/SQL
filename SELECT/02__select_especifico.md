# Selecionando colunas específicas

O caracter `*` tem como função selecionar todas as colunas de uma determinada tabela, porém você também pode especificar qual(is) coluna(s) você quer ver apenas escrevendo seu nome. Neste caso, dentro da tabela `employee` queremos selecionar somente as colunas `FirstName` e `LastName` sem que apareçam outras informações

```
SELECT FirstName, LastName FROM employee;
```

Saída:
![alt text](saida_select_especifico.png)