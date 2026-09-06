# EXCLUINDO TABELAS

Quando uma tabela não é mais necessária, basta executar o comando `DROP TABLE` para excluí-la permanentemente. 
**ATENÇÃO:** Caso você exclua uma tabela sem inteção, não é possível recuperá-la, por isso, é necessária muito atenção antes de rodar esse comando

Agora, vamos deletar a `tabela_exemplo`, criada por nós anteriormente
```sql
DROP TABLE IF EXISTS tabela_exemplo;
```