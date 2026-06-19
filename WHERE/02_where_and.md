# Combinando condições com AND

Pode-se usar o operador `AND` para combinar diversas condições. Desse modo, utilizando a mesma estrutura `WHERE` podemos ter como retorno clientes que são do Brasil e que pertencem ao estado de São Paulo (SP)

```sql
SELECT * FROM Customer WHERE Country = 'Brazil' AND State = 'SP';
```

**Saída:**

| CustomerId | FirstName | LastName | Company | Address | City | State | Country | PostalCode | Phone | Fax | Email | SupportRepId |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | Luís | Gonçalves | Embraer - Empresa Brasileira de Aeronáutica S.A. | Av. Brigadeiro Faria Lima, 2170 | São José dos Campos | SP | Brazil | 12227-000 | +55 (12) 3923-5555 | +55 (12) 3923-5566 | luisg@embraer.com.br | 3 |
| 10 | Eduardo | Martins | Woodstock Discos | Rua Dr. Falcão Filho, 155 | São Paulo | SP | Brazil | 01007-010 | +55 (11) 3033-5446 | +55 (11) 3033-4564 | eduardo@woodstock.com.br | 4 |
| 11 | Alexandre | Rocha | Banco do Brasil S.A. | Av. Paulista, 2022 | São Paulo | SP | Brazil | 01310-200 | +55 (11) 3055-3278 | +55 (11) 3055-8131 | alerc@uol.com.br | 5 |