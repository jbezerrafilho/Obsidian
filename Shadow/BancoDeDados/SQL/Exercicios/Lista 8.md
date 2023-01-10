-----
#view #index 


```SQL

-- 1) Faça um select somente de 10 editoras de GO

	SELECT * FROM editora WHERE estado = "GO" LIMIT 10;

-- 2) Exiba o nome das editoras em ordem inversa e retorne as 3 primeiras

	SELECT nome FROM editora ORDER BY nome DESC LIMIT 3;

-- 3) Exiba todos os estados que temos editoras cadastradas

	SELECT DISTINCT estado  FROM editora;

-- 4) Crie uma view para o select que você fez no exercício 1 com o nome de GOIAS.

	CREATE VIEW GOIAS AS
	SELECT * FROM editora WHERE estado = "GO" LIMIT 10;

	SELECT * FROM GOIAS;

-- 5) Crie uma view para o select que você fez no exercício 3 com o nome de ESTADOS.

	CREATE VIEW ESTADOS AS
	SELECT DISTINCT estado  FROM editora;
	
	SELECT * FROM ESTADOS;
	
-- 6) Crie um índice para o estado na tabela Editora
	
	CREATE INDEX index_estado ON editora (estado);
	
-- 7) Crie um índice para o nome do autor.
	
	CREATE INDEX indice_nome ON autor (nome);
	
-- 8) Utilize subselect e exclua todos os livros da editora XPTO
	
	DELETE FROM livro WHERE editora_id = (
		SELECT id FROM editora 
		WHERE nome = "XPTO"
	);
	
-- 9) Utilize subselect e exclua todos os livros do autor José Buscapé
	
	DELETE FROM livro WHERE autor_id = (
		SELECT id FROM autor 
		WHERE nome = "José Buscapé"
	);

-- 10) Exclua a view GOIAS
	
	DROP VIEW GOIAS;
	
-- 11) Exclua o índice da tabela Editora
	
	DROP INDEX index_estado;
	
-- 12) Exclua a view Estados

	DROP VIEW ESTADOS;
	
-- 13)  Exiba em ordem alfabética as editoras e mostre as 7 primeiras (somente o nome).

	SELECT nome FROM editora ORDER BY nome LIMIT 7;

-- 14) Exclua o índice da tabela autor

	DROP INDEX indice_nome;
	
-- 15) Crie um índice para o nome do livro

	CREATE INDEX indice_nome ON livro (titulo);









