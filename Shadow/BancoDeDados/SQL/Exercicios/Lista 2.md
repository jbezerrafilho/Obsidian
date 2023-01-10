-----
#command #sql #DDL 

[[Lista 1]]

```SQL

CREATE TABLE alunos (codigo int, nome text, telefone text, cidade text);
CREATE TABLE caixa (codigo int, data date, descricao text, debito real, credito real);

ALTER TABLE caixa RENAME TO dinheiro;
ALTER TABLE super_alunos RENAME TO alunos;
ALTER TABLE alunos RENAME TO estudantes;
ALTER TABLE caixa RENAME TO muito_dinheiro;

-- Criando um campo na tabela
ALTER TABLE alunos ADD estado TEXT;
ALTER TABLE alunos ADD cpf TEXT;
ALTER TABLE alunos ADD rg TEXT;
ALTER TABLE caixa ADD observacao TEXT;
ALTER TABLE caixa ADD saldo numeric;
ALTER TABLE muito_dinheiro ADD campo numeric;

DROP TABLE dinheiro;
DROP TABLE notas;
DROP TABLE estudantes;
DROP TABLE alunos;
```
