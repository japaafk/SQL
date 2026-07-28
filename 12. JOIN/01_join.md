# Combinando tabelas com JOIN

A cláusula `JOIN` combina linhas de duas ou mais tabelas com base em colunas relacionadas. Retornando apenas as linhas que possuem valores correspondentes em ambos os lados. Aqui, relacionamos álbuns com artistas para mostrar o título de cada álbum ao lado do nome do artista

```sql
SELECT Album.Title AS Álbum, Artist.Name AS Nome FROM Album JOIN Artist ON Album.ArtistId = Artist.ArtistId LIMIT 5; 
```

**Saída:**

| Álbum | Nome |
|---|---|
| For Those About To Rock We Salute You | AC/DC |
| Balls to the Wall | Accept |
| Restless and Wild | Accept |
| Let There Be Rock | AC/DC |
| Big Ones | Aerosmith |    