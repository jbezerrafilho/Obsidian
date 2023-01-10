#lista1 #command #DDL

[[SQLite#^82d538|Comandos SQLite]]


[[Glossary#^99f21e|DDL]]

```SQL 
CREATE TABLE alunos (codigo integer, nome text, telefone text, cidade text);

CREATE TABLE alunos2 (codigo integer, nome varchar(200), telefone varchar(50), cidade varchar(100));

CREATE TABLE funcionarios (nome text, endereco text, telefone text, cidade text, estado varchar(2), cep varchar(9), rg text, cpf text, salario real);

CREATE TABLE fornecedores (nome text, endereco text, telefone text, cidade text, estado varchar(2), cep varchar(9), cnpj varchar(14), email text);

CREATE TABLE livros (codigo integer, nome text, categoria text, resumo text, precocusto real, precovenda real);

CREATE TABLE livros (id int, titulo text, autor_id int, editora_id int, estilo_id int, sinopse text, isbn text);

CREATE TABLE estoque (codigo integer, nomedoproduto text, categoria text, quantidade int, fornecedor text);

CREATE TABLE notas (codigo integer, nomedoaluno text, 
					"1bim" real, "2bim" real, "3bim" real, "4bim" real);

CREATE TABLE caixa (codigo integer, data date, descricao text, debito real, credito real);

CREATE TABLE contasAPagar (codigo integer, data_conta date, 
						   descricao text, valor real, data_pagamento date);

CREATE TABLE contasAReceber (codigo integer, data_conta date, descricao text, valor real, data_recebimento date);

CREATE TABLE filmes (codigo integer, nome text, 
					 sinopse text, categoria text, diretor text);

CREATE TABLE CDS (codigo integer, nome text, 
				  cantor text, ano date, quantidademusicas integer);

===========================================================================

DROP TABLE alunos;

DROP TABLE livros;

DROP TABLE contasAPagar;

DROP TABLE contasAReceber;

DROP TABLE filmes;

===========================================================================

ALTER TABLE alunos2 RENAME TO super_alunos;

ALTER TABLE estoque RENAME TO produtos;

ALTER TABLE notas RENAME TO aprovados;

ALTER TABLE aprovados RENAME TO notas;
```


