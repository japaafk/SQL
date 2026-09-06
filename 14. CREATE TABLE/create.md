# CRIANDO TABELAS

A cláusula `CREATE TABLE` é usada para criar uma nova tabela dentro do Banco de Dados. Ao definir um nome para a tabela, é necessário nomear suas colunas juntamente com o <ins>tipo de dado específico</ins> que ela vai receber. Geralmente, esse comando é executado apenas uma vez

## **Sintaxe Básica**
```sql
CREATE TABLE nome_da_tabela (
    coluna1 tipo_de_dado,
    coluna2 tipo_de_dado,
    coluna3 tipo_de_dado
);
```

Para servir de exemplo, vamos criar a tabela `tabela_exemplo`. Tendo consigo uma coluna do tipo inteira como chave primária e uma coluna do tipo texto
**Nota:** Caso queira vizualar a tabela criada, por precedência é preciso adicionar valores nas suas linhas usando o o comando `INSERT INTO`

```sql
CREATE TABLE tabela_exemplo (
    Id INTEGER PRIMARY KEY,
    Descrição TEXT
);
```