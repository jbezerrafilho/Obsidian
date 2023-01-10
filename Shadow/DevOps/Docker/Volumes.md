-----
#docker #volumes

❯ [[Imagens]], [[Container]], [[Network]]

>O Container por ter um comportamento transitório, efêmero, não persiste dados. Por este motivo precisamos criar Volumes.

### Tipos De Volumes

- Anônimos (Anonymous) : Diretórios criado pela flag -v, porém com nome aleatório
- Nomeados (Named): Gerenciado pelo docker
- Bind Mount: Um forma de salvar dados no host sem o gerenciamento do docker
 [[BancoDeDados/MySQL/Instância|Exemplo]] de criação de um volume numa instância MySQL não gerenciado pelo Docker


```shell
❯ docker volumes ls (listando volumes gerenciado pelo docker)
❯ docker volume create name
❯ docker volume inspect hash ou nome_volume
❯ docker volume rm hash ou nome_volume
❯ docker volume prune (Remove volumes não utilizados)

Volumes Anonymous
--------------------------------------------------------------

❯ docker run --name ubuntu -it  -v /data ubuntu:18.04
❯ docker inspect ubuntu (verifique o volume /data e seu hash)
❯ docker inspect volume hash
❯ docker run --name ubuntu -it  -v /data ubuntu:18.04

Volumes Nomeados
--------------------------------------------------------------

❯ docker run --name ubuntu -it  -v ubuntu_volume:/data ubuntu:18.04
❯ docker volume ls
	DRIVER    VOLUME NAME
	local     ubuntu_volume

Volumes Bind Mount
---------------------------------------------------------------

❯ docker run --name ubuntu -it  -v path_absolute_host:/data ubuntu:18.04


```
Veja um exemplo de bind mount na criação da instância do [[BancoDeDados/PostgreSQL/Instância|PostgreSQL]]
