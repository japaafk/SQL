# Função DISTINCT

A função `DISTINCT` é usada para eliminar valores duplicados dos resultados de uma consulta. Ela se encaixa perfeitamente no exemplo da tabela `Customer`

### Tabela sem `DISTINCT`:

```SELECT Country FROM Customer LIMIT 10;```

**Saída:**

| Customer |
| --- |
| Brazil |
| Germany |
| Canada |
| Norway |
| Czech Republic |
| Czech Republic |
| Austria |
| Belgium |
| Denmark |
| Brazil |

### Tabela com `DISTINCT`:

```SELECT DISTINCT Country FROM Customer LIMIT 8;```

**Saída:**

| Country |
| --- |
| Brazil |
| Germany |
| Canada |
| Norway |
| Czech Republic |
| Austria |
| Belgium |
| Denmark |