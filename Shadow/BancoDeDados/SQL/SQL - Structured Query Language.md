***
#teoria 


### Estrutura analítica de uma Query

>[!success] SELECT  consulta a coluna e executa um comando

>[!todo] FROM indica em qual tabela está a coluna

>[!example] WHERE define as restrições de consulta

>[!warning] LIMIT numa tabela que não conhecemos é prudente limitar a saída


Ao realizarmos uma simples consulta trazendo todos os campos de uma tabela, como por exemplo  `SELECT * FROM funcionario;` , receberemos como saída os registros ordenados de forma ASC pelo PK da tabela em questão. Podemos usar o `ORDER BY` para alterarmos este default. Poderemos usar as funções `MAX() e MIN()` .


### Convenções

- Nome da tabela no singular
- Campo Primary Key definido como **id
- Campo Foreign Key definido como **tabela_id

