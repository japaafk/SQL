# ALTERANDO TABELAS

O comando `ALTER TABLE` é utilizado para alterar a estrutura de uma tabela que já existe 

Para exemplificar esse conceito vamos adicionar a coluna `HorárioCriação` na tabela `tabela_exemplo` para gravar quando cada linha foi criada

```sql
ALTER TABLE tabela_exemplo 
ADD COLUMN HorárioCriação DATETIME DEFAULT CURRENT_TIMESTAMP;
```