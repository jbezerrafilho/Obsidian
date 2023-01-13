-----

>[!success] As permissões de acesso à arquivos e diretórios num SO definem quem podem acessar determinado  recurso e o nível de privilégio sobre o item acessado.

De forma resumida, as permissões são atributos que definem se o arquivo ou diretório pode ser ==Read== , ==Write== ou ==Execute==. Uma sequência de 12 bits define uma permissão no Linux.

#permissão
- 3 bits iniciais (special modes, permissões especiais ou estendidas)

- 9 bits restantes (file mode, permissões para 03 classes de usuários, sendo:)
	- Usuário proprietário | dono do arquivo
	- Grupo proprietário do arquivo
	-  Outros usuários

>[!tip] User  RWX Group RWX Other RWX

A permissão de execução para o diretório significa poder entrar no diretório.

Valor Octal:
- 0 - Sem valor ( - - -)
- 1 - Execute (- - x)
- 2 - Write (- w -)
- 3 - Write e Execute (- w x)
- 4 - Read (r - -)
- 5 - Read e Execute (r - x)
- 6 - Read e Write (r w -)
- 7 - Read, Write e Execute (r w x)

`$ chmod 755 ninja -v`
`$ chmod a=rw,g=r,o=r script.sh -v (Podemos adicionar '+', retirar '-' ou atribuir '=' permissão`











