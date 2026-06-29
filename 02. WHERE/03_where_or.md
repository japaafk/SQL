# Combinando condições com OR

O operador `OR` permite que pelo menos uma das condições checadas seja verdadeira. Desse modo, seguindo o exemplo abaixo a consulta irá retornar clientes que são do Brasil ou do Chile

```sql
SELECT * FROM Customer WHERE Country = 'Brazil' OR Country = 'Chile';
```

**SAÍDA:**

| CustomerId | FirstName | LastName | Company | Address | City | State | Country | PostalCode | Phone | Fax | Email | SupportRepId |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | Luís | Gonçalves | Embraer - Empresa Brasileira de Aeronáutica S.A. | Av. Brigadeiro Faria Lima, 2170 | São José dos Campos | SP | Brazil | 12227-000 | +55 (12) 3923-5555 | +55 (12) 3923-5566 | luisg@embraer.com.br | 3 |
| 10 | Eduardo | Martins | Woodstock Discos | Rua Dr. Falcão Filho, 155 | São Paulo | SP | Brazil | 01007-010 | +55 (11) 3033-5446 | +55 (11) 3033-4564 | eduardo@woodstock.com.br | 4 |
| 11 | Alexandre | Rocha | Banco do Brasil S.A. | Av. Paulista, 2022 | São Paulo | SP | Brazil | 01310-200 | +55 (11) 3055-3278 | +55 (11) 3055-8131 | alerc@uol.com.br | 5 |
| 12 | Roberto | Almeida | Riotur | Praça Pio X, 119 | Rio de Janeiro | RJ | Brazil | 20040-020 | +55 (21) 2271-7000 | +55 (21) 2271-7070 | roberto.almeida@riotur.gov.br | 3 |
| 13 | Fernanda | Ramos | NULL | Qe 7 Bloco G | Brasília | DF | Brazil | 71020-677 | +55 (61) 3363-5547 | +55 (61) 3363-7855 | fernadaramos4@uol.com.br | 4 |
| 57 | Luis | Rojas | NULL | Calle Lira, 198 | Santiago | NULL | Chile | NULL | +56 (0)2 635 4444 | NULL | luisrojas@yahoo.cl | 5 |