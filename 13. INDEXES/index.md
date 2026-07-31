# INDEXES

Os Índices `INDEXES` são recursos utilizados pelos bancos de dados para otimizar o tempo de resposta das consultas

No terminal do SQLite, você pode ativar um cronômetro interno com o seguinte comando:
```
.timer ON
```

A partir disso, o tempo exato de execução aparecerá abaixo da saída de cada comando

## **Consulta sem INDEX**

Primeiro, fazemos uma busca normal na coluna `Name` antes de criar o índice:
\`\`\`sql   
SELECT TrackId, Name FROM Track WHERE Name LIKE 'Love%';
\`\`\`

| TrackId | Name                        |
|---------|------------------------------|
| 24      | Love In An Elevator          |
| 56      | Love, Hate, Love             |
| 413     | Loverman                     |
| 440     | Love Gun                     |
| 493     | Love Is Blind                |
| 571     | Love Of My Life              |
| 751     | Love Child                   |
| 803     | Love Conquers All             |
| 808     | Love Don't Mean a Thing       |
| 828     | Love Bites                   |
| 1042    | Love And Marriage            |
| 1055    | Loves Been Good To Me        |
| 1189    | Love Is The Colour           |
| 1483    | Love Or Confusion            |
| 1943    | Love Me Like A Reptile       |
| 2180    | Love Boat Captain            |
| 2540    | 'Love Me Darlin''            |
| 2628    | Love Removal Machine         |
| 2632    | Love                         |
| 2690    | Love Is Strong               |
| 2937    | Love Is Blindness            |
| 2952    | Love Comes Tumbling          |
| 2967    | Love And Peace Or Else       |
| 2997    | Love Rescue Me               |
| 3135    | Love Ain't No Stranger       |
| 3355    | Love Comes                   |
| 3460    | Love Is a Losing Game        |

*Run Time: real 0.052671 user 0.000000 sys 0.000000*

## **Criando um INDEX**

E como otimizaremos esse comando? Bom, a resposta para isso está na criação de um `INDEX`, no qual possibilita a redução do tempo de execução de um comando em uma tabela específica e em uma coluna específica

A estrutura básica para sua criação é:
```
CREAT INDEX nome ON tabela (coluna, ...);
```

Aplicando essa sintaxe ao nosso cenário:
```
CREATE INDEX Track_nome ON Track (Name);
```

## **Comparando o Resultado**

Com o índice já criado, executamos exatamente a mesma consulta:
\`\`\`sql
SELECT TrackId, Name FROM Track WHERE Name LIKE 'Love%';
\`\`\`

| TrackId | Name                        |
|---------|------------------------------|
| 2632    | Love                         |
| 3135    | Love Ain't No Stranger       |
| 1042    | Love And Marriage            |
| 2967    | Love And Peace Or Else       |
| 828     | Love Bites                   |
| 2180    | Love Boat Captain            |
| 751     | Love Child                   |
| 3355    | Love Comes                   |
| 2952    | Love Comes Tumbling          |
| 803     | Love Conquers All             |
| 808     | Love Don't Mean a Thing       |
| 440     | Love Gun                     |
| 24      | Love In An Elevator          |
| 493     | Love Is Blind                |
| 2937    | Love Is Blindness            |
| 2690    | Love Is Strong               |
| 1189    | Love Is The Colour           |
| 3460    | Love Is a Losing Game        |
| 2540    | 'Love Me Darlin''            |
| 1943    | Love Me Like A Reptile       |
| 571     | Love Of My Life              |
| 1483    | Love Or Confusion            |
| 2628    | Love Removal Machine         |
| 2997    | Love Rescue Me               |
| 56      | Love, Hate, Love             |
| 413     | Loverman                     |
| 1055    | Loves Been Good To Me        |

*Run Time: real 0.049966 user 0.000000 sys 0.015625*

### Diferença das Consultas

**REDUÇÂO DO TEMPO:** Como podemos analisar o tempo de processamento (real time) diminuiu. Em tabelas pequenas a diferença parece sutil, mas em bancos de dados com milhões de registros a diferença passa de minutos para milissegundos.