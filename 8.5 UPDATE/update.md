# Atualizando registros com UPDATE

A cláusula `UPDATE` serve para atualizar/alterar uma ou mais linhas (registros) já existentes em sua tabela. Para isso, é de suma importância que você não omita o operador de filtragem (`WHERE`) no momento de executar esse comando: caso contrário, todas as linhas da sua tabela podem ser atualizadas com o valor prescrito

Abaixo temos um exemplo de como esse comando é executado

```sql
UPDATE tabela SET coluna_a_ser_modificada = 'valor_a_ser_inserido' WHERE Id = 1;
```

**NOTA:** "Id = 1" foi somente um exemplo de coluna filtrada, nesse campo você utiliza a filtragem que bem entender