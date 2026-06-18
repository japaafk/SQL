# SELECT Básico

O comando `SELECT` é a base das consultas em SQL. Com isso, um `SELECT` básico retorna todas as colunas e linhas de uma tabela. Seu comando é escrito da seguinte forma:

```sql
SELECT colunas FROM tabela;
```

Tendo isso em mente, no banco de dados Chinook, a tabela `artists` armazena informações sobre artistas musicais. Seguindo a estrutura do comando abaixo, teremos como retorno os primeiros cinco artistas e a exibição de todas as colunas da tabela.

```sql
SELECT * FROM artist LIMIT 5;
```

| ArtistId | Name |
| --- | --- |
| 1 | AC/DC |
| 2 | Accept |
| 3 | Aerosmith |
| 4 | Alanis Morissette |
| 5 | Alice In Chains |