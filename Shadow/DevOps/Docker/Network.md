-----
#docker #network

❯ [[Imagens]], [[Volumes]], [[Container]]

>Conteiners são objetos - pedaços de software isolados da comunicação externa. A melhor de separar os containers em redes individuas, algo 'subnets' do mundo docker.


### Tipos De Conexões

- **Host: Comunicação com a máquina hospedeira
- **Bridge: Comunicação entre dois ou mais containers
- **Macvlan: Permite a conexão ao container via MAC Address
- **None: Remove todas as conexões do container
- **Plugins: Permite extensões de terceiros para criar redes


```shell
❯ docker network ls
❯ docker network create name (Cria a rede com o driver bridge - default)
❯ docker network create -d macvlan name (-d driver)
❯ docker network rm name
❯ docker network prune (Remover redes não utilizadas)
❯ docker network connect container
❯ docker network disconnect container
❯ docker network inspect
```
