# Combinando condições com AND

Pode-se usar o operador `AND` para combinar diversas condições. Desse modo, utilizando a mesma estrutura `WHERE` podemos ter como retorno clientes que são do Brasil e que pertencem ao estado de São Paulo (SP)

```
SELECT * FROM Customer WHERE Country = 'Brazil' AND State = 'SP';
```

**Saída:**

![alt text](exemplo_AND.png)