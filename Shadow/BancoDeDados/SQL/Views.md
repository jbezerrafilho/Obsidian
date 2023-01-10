-----
#views #DDL 

A **view** pode ser definida como uma tabela virtual composta por linhas e colunas de dados vindos de tabelas relacionadas em uma query (um agrupamento de SELECT’s, por exemplo). As linhas e colunas da view são geradas dinamicamente no momento em que é feita uma referência a ela.

[View](http://www.devmedia.com.br/conceitos-e-criacao-de-views-no-sql-server/22390)

```SQL

CREATE view MinasGerais as
SELECT  a.nome, e.nome, e2.nome, l.titulo  
FROM autor a, editora e, estilo e2, livro l 
WHERE a.id = l.autor_id 
AND e.id = l.editora_id 
AND e2.id = l.estilo_id 
AND e.estado = "MG";

DROP view MinasGerais;

