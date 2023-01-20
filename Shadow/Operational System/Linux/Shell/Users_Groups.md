-----

```shell
#useradd #userdel #usermod

$ useradd jose
$ useradd linux

#adduser
$ adduser (Criando usuários com wizard)

Obs: No Centos, a criação do usuário já cria a pasta home
Obs1: No Debian é necessário especificar a opçao -m para criar a home
Obs2: Outro conceito importante no linux é que ao criar um usuário, um grupo   primário é criado com o mesmo nome do usuário.

#etc_passwd
$ cat /etc/passwd (Verificamos usuários do sistema)
$ usermod -s /bin/bash paty (Alterando o shell do user paty)

#groupadd #groupdel #groupmod
$ groupadd rh

#etc_group
$ cat /etc/group (Verifica grupos)

Obs: Todo usuário pertence a um único grupo primário, mas pode ser adicionado a vários grupos suplementares - secundários.

$ usermod -G ti paty (Add paty ao grupo suplementar ti. -G grupo secundário)
$ groups paty (lista grupos a que 'paty' pertence)

#id_user
$ id paty (Lista grupos com seus respectivos ids)

#etc_shadow
$ cat /etc/shadow

-----------------------------------------------------------------------

#elevacao_privilegio

$ su <opcoes> <usuario> (switch user)
$ su (Caso não seja informado user, será considerado root)
$ su - (Carrega o perfil de root completo)

#sudo
$ sudo su (Permite ao usuário logado, executar 'um' comando com privilégio adm)

#sudoers
$ cat /etc/sudoers (Define quais usuários possuem determinado nível de privilégio e quais comando o mesmo poderá executar sem a necessidade do root)
$ visudo /etc/sudoers (Mostra permissões para grupos de comandos)
$ usermod -G google-sudoers paty (Add paty ao grupo sudoers)

-----------------------------------------------------------------------

```
