# Função LIKE

A função `LIKE` no SQL é utilizada para procurar padrões em textos. Sendo muito útil quando você não sabe exatamente o valor que deseja encontrar, mas conhece parte dele. Além disso, junto dele é possível utilizar um coringa, o símbolo `%`, na qual representa zero, um ou vários caracteres

```sql
SELECT * FROM PLaylist WHERE Name LIKE 'Classical %';
```

**Saída:**

| PlaylistId | Name |
|---|---|
| 13 | Classical 101 - Deep Cuts |
| 14 | Classical 101 - Next Steps |
| 15 | Classical 101 - The Basics |