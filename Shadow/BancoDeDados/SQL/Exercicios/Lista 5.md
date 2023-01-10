----
#command #DDL #sql 

```SQL
  CREATE TABLE livro (
  id int, 
  titulo text, 
  autor_id int, 
  editora_id int, 
  estilo_id int, 
  sinopse text, 
  isbn text
  );

 CREATE TABLE editora (
 id int,
 nome text,
 cidade text,
 estado varchar(2),
 telefone text,
 email text
 );

 CREATE TABLE estilo (
 id int,
 nome text
 );

 CREATE TABLE autor (
 id int, 
 nome text,
 cidade text,
 estado varchar(20),
 telefone text
 );

```

#DML 

```SQL 

INSERT INTO livro (id, titulo, autor_id, editora_id, estilo_id) VALUES (1, "Auto da Compadecida", 4, 3, 1);
INSERT INTO livro (id, titulo, autor_id, editora_id, estilo_id) VALUES (2, "O Saci", 1, 2, 3);
INSERT INTO livro (id, titulo, autor_id, editora_id, estilo_id) VALUES (3, "Senhora", 2, 1, 5);
INSERT INTO livro (id, titulo, autor_id, editora_id, estilo_id) VALUES (4, "Dom Casmurro", 3, 4, 4);
INSERT INTO livro (id, titulo, autor_id, editora_id, estilo_id) VALUES (5, "O Continente", 5, 5, 2);



INSERT INTO editora (id, nome, cidade, estado, telefone)
VALUES (1, "RIO", "Rio de Janeiro", "RJ", "33445566");
INSERT INTO editora (id, nome, cidade, estado, telefone)
VALUES (2, "FTD", "São Paulo", "SP", "23454556");
INSERT INTO editora (id, nome, cidade, estado, telefone)
VALUES (3, "Alta Books", "Belo Horizonte", "MG", "56890944");
INSERT INTO editora (id, nome, cidade, estado, telefone)
VALUES (4, "Sextante", "Curitiba", "PR", "87340945");
INSERT INTO editora (id, nome, cidade, estado, telefone)
VALUES (5, "Rocco", "Recife", "PE", "87340945");


INSERT INTO estilo (id, nome) VALUES (1, "Comédia");
INSERT INTO estilo (id, nome) VALUES (2, "Drama");
INSERT INTO estilo (id, nome) VALUES (3, "Ficção");
INSERT INTO estilo (id, nome) VALUES (4, "Suspense");
INSERT INTO estilo (id, nome) VALUES (5, "Romance");

INSERT INTO autor (id, nome, cidade, estado, telefone) 
VALUES (1, "Monteiro Lobato", "Taubaté", "SP");
INSERT INTO autor (id, nome, cidade, estado) 
VALUES (2, "José De Alencar", "Messejana", "CE");
INSERT INTO autor (id, nome, cidade, estado) 
VALUES (3, "Machado De Assis", "Rio De Janeiro", "RJ");
INSERT INTO autor (id, nome, cidade, estado) 
VALUES (4, "Ariano Suassuna", "Recife", "PE");
INSERT INTO autor (id, nome, cidade, estado) 
VALUES (5, "Érico Veríssimo", "Porto Alegre", "RS");

UPDATE autor set id=5 where estado = "RS";
UPDATE editora set id = 4 where nome = "Sextante";

SELECT  * FROM estilo ORDER BY nome;
SELECT titulo, estilo_id from livro;

```
