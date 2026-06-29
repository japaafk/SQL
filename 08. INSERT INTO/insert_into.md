# Inserindo linhas em uma tabela
O comando `INSERT INTO` é utilizado para adicionar novos registros (linhas) em uma tabela. Ele é executado do seguinto modo:

```sql
INSERT INTO Tabela (Coluna) VALUES ('Valor inserido');
```

No exemplo abaixo, vamos inserir um valor temporário na coluna `Name` da tabela `Artist` para demonstração do comando

```sql
INSERT INTO Artist (Name) VALUES ('Banda Exemplo');
```

Se estiver incerto se o comando funcionou ou não, verifique se o valor armazenado utilizando o comando `WHERE`. Caso o terminal não apresente nada, siginifica que o valor não foi inserido na tabela corretamente