# Combinando condições com IN

O operador `IN` é usado para verificar se um valor pertence a uma lista de valores. Aparecendo juntamente com a cláusula `WHERE`, ele serve para evitar a repetição do comando `OR`, substituindo-o. Na consulta abaixo, serão selecionados todos os gêneros cujo nome é 'Rock', 'Jazz' ou 'Metal'

```sql
SELECT * FROM Genre WHERE Name IN ('Rock', 'Jazz', 'Metal');
```

**Saída:**

| GenreId | Name |
|---|---|
| 1 | Rock |
| 2 | Jazz |
| 3 | Metal |