# Combinando condições com OR

O operador `OR` permite que pelo menos uma das condições checadas seja verdadeira. Desse modo, seguindo o exemplo abaixo a consulta irá retornar clientes que são do Brasil ou do Chile

```sql
SELECT * FROM Customer WHERE Country = 'Brazil' OR Country = 'Chile';
```

**SAÍDA:**

![alt text](tabela_OR.png)