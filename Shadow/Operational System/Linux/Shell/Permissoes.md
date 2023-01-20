-----

>[!success] As permissões de acesso à arquivos e diretórios num SO definem quem podem acessar determinado  recurso e o nível de privilégio sobre o item acessado.

De forma resumida, as permissões são atributos que definem se o arquivo ou diretório pode ser ==Read== , ==Write== ou ==Execute==. Uma sequência de 12 bits define uma permissão no Linux.

#permissão
- 3 bits iniciais  para `special mode`
- 9 bits restantes para `file mode`


>[!tip] A permissão conhecida como 'file mode'  é formada por 9 bits. Entenda que separamos 3 bits para representar a permissão do dono do arquivo ou diretório, 3 bits para o grupo proprietário do arquvio ou diretório e 3 bits para outros usuários do sistema. 

#### Por que 3 bits?

**Porque 2³ = 8 que equivale à base octal, então dispomos de 3 bits que lemos da direita para esquerda de acordo com o sistema posicional da base 2.

>[!note] (1 1 1) ₂ = (2² + 2¹ + 2⁰)  = 7₁₀ 

4 2 1   4 2 1   4 2 1
 U           G        O   , onde U = User, G = Group e O = Other.
**r w x    r w x  r w x

**A permissão de execução para o diretório recém criado é default e  significa que qualquer usuário  poder entrar no diretório.

```shell
$ chmod 755 ninja -v

$ chmod a=rw script.sh -v ('=' atribuir)
$ chmod u+x script.sh -v ('+' append)
$ chmod g-r script.sh -v ('-' retirar)

-------------------------------------------------

$ chgrp new_group folder/ or file
$ chown user folder/ or file
$ chown user.group folder/ or file (altera dono e grupo de uma vez)


```
`











