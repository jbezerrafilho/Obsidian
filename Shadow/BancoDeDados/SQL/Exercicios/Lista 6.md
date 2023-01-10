-----
#sql #command  #DML

```SQL
-- Selecione o campo 'título' na tabela livro cujo alias é 'l' e o campo 'nome' da tabela editora cujo alias é 'e' ONDE a condição é atendida
SELECT l.titulo, e.nome  FROM livro l, estilo e WHERE e.id = l.editora_id ;

-- Selecione o campo titulo no alias 'l'(tabela livro) e nome no alias 'e'(tabela estilo) em que o título comece com 'A'.
SELECT l.titulo, e.nome 
FROM livro l, estilo e
WHERE e.id  = l.estilo_id
AND l.titulo LIKE "A%";

7)  Selecione o nome do autor, da editora, do estilo e do livro de todos os livros de autores cujo nome comece por D.

SELECT a.nome, e.nome, s.nome, l.titulo 
FROM livro l, autor a, editora e, estilo s
WHERE a.id = l.autor_id 
AND e.id = l.editora_id 
AND s.id = l.estilo_id 
AND a.nome LIKE "J%";

8)  Selecione o nome do autor, da editora, do estilo e do livro de todos os livros de editoras paulistas.

SELECT  a.nome, e.nome, e2.nome, l.titulo  
FROM autor a, editora e, estilo e2, livro l 
WHERE a.id = l.autor_id 
AND e.id = l.editora_id 
AND e2.id = l.estilo_id 
AND e.estado = "MG";

9)  Atualize o autor do livro de id 1 para autor_id 2.

SELECT a.nome , a.id , l.titulo , l.id 
FROM autor a , livro l 
WHERE a.id = l.autor_id ;

UPDATE livro set autor_id = 2
WHERE id = 1;


15)  Selecione o nome do livro e do autor de em ordem alfabética por autor.
SELECT l.titulo  , a.nome 
FROM livro l, autor a
WHERE a.id  = l.autor_id
ORDER BY a.nome DESC ;

```
