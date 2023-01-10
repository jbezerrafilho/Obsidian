----
#agregacao #dml #sql 

```SQL
1) Conte o número de editoras cadastradas

SELECT *  FROM editora;

2) Calcule a média do preço de venda dos livros

SELECT AVG(precovenda) FROM livro;   

3) Atualize o preço de venda do livro 1 aumentando seu valor em 7%

UPDATE livro set precovenda  = precovenda +  (precovenda * 1.07)
WHERE id = 1;

4) Conte a quantidade de editoras de MG.

SELECT COUNT(*) FROM editora 
WHERE estado = "MG";

5) Conte o número de editoras agrupando por estado.

SELECT estado, COUNT(*) as Total FROM editora 
GROUP BY estado;

6) Diminua o preço de todos os livros da editora 1 em 19%.

UPDATE livro set precovenda = precovenda  - (precovenda * 0.19)
WHERE editora_id = 1;

7) Qual o maior código de autor cadastrado?

SELECT MAX(id) FROM autor; 

8) Qual o menor código de autor cadastrado?

SELECT MIN(id) FROM autor; 

9) Conte o número de editoras, agrupando por estado e somente para estados que tenham 40 ou mais editoras.

SELECT estado, COUNT(*) FROM editora 
GROUP BY estado
HAVING COUNT(*) >= 40;

10) Aumente o preço de todos os livros em 7,5%

UPDATE livro set precovenda = precovenda + (precovenda * 1.07);

11) Exclua todas as editoras do estado DF.

DELETE FROM editora 
WHERE estado = "DF";

12) Os livros podem ser vendidos em 3 parcelas sendo a primeira parcela 30% do valor do livro e a segunda e terceira sendo 35% cada. Faça um select que mostre o nome do livro juntamente com o preço dele e os valor das parcelas.

SELECT titulo , precovenda,
precovenda  * 0.3 as "Parcela 1",
precovenda  * 0.35 as "Parcela 2",
precovenda  * 0.35 as "Parcela 3"
FROM livro;

13) Todas as editoras do DF mudaram para GO. Atualize no banco de dados por favor!

UPDATE editora set estado = "DF"
WHERE estado = "GO";

14) Quantas editoras temos em cidades que começam pela letra M?

SELECT cidade, COUNT(*) from editora 
WHERE cidade LIKE "M%";

15) Altere o preço de todos os livros dando um desconto de 6%

UPDATE livro set precovenda = precovenda - (precovenda * 0.06);
UPDATE livro set precovenda = precovenda * 0.94;

