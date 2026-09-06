# CRIANDO TABELAS

A claúsula `CREATE TABLE` tem por funcionalidade criar uma nova tabela dentro do Banco de Dados. Com isso, após colocar um nome de identificação para a tabela é preciso nomear suas colunas juntamente com o <ins>tipo de dado específico</ins> que ela vai receber. Normalmente você precisa executar somente uma vez esse comando

## **Sintaxe Básica**
```sql
CREATE TABLE nome_da_tabela (
    coluna1 tipo_de_dado,
    coluna2 tipo_de_dado,
    coluna3 tipo_de_dado
);
```

Para servir de exemplo vamos criar a tabela `tabela_exemplo`. Tendo consigo uma coluna inteira como chave primária e uma coluna de texto

```sql
CREATE TABLE tabela_exemplo (
    Id INTEGER PRIMARY KEY,
    Descrição TEXT
);
```