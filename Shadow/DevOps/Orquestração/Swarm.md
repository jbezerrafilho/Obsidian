--------

#docker #swarm #service #replicas #orquestração 

>Orquestração é a ação de implantar,  gerenciar, escalar conteiners numa aplicação

### Tecnologias de Orquestração

^312d34

- **Docker Swarm (Fácil de configurar, mas peca pela falta de recursos)
- **Kubernetes (Um pouco mais difícil de configurar, mas tem o pacote mais completo)
- **Mesos Apache (Bem mais difícil de configurar, menos utilizado)

### Swarm

- **Escala horizontalmente
- **Cluster (Agrupamento de máquinas em paralelo)
- **Comandos semelhantes ao docker
- **Docker tem o swarm integrado, porém desabilitado

#### Arquitetura

- <font color="orange"> <b>Nodes</b></font> - Instância de uma máquina fisica ou virtual integrante do Swarm
- <font color="orange"> <b>Manager Node</b></font> - Gerencia os Nodes do cluster. Equivale ao Node Master no k8s
- <font color="orange"> <b>Work Node</b></font> - Nodes que trabalham sendo gerenciados pelo Manager. Lá vivem os containers
- <font color="orange"> <b>Services</b></font> - Conjunto de Tasks que o manager envia para os nodes
- <font color="orange"> <b>Tasks</b></font> - Comandos executados nos Nodes

**Para realizar os lab's, pode-se utilizar a nuvem AWS, GCP ou Docker Labs.

```shell
# O comando abaixo inicializa o swarm na máquina física ou virtual e a adiciona
# como Node Manager. Pode ser necessário usar a flag '--advertise-addr'
❯ docker swarm init --advertise-addr <IP>
❯ docker swarm join --token <token> <ip>:<porta>
❯ docker swarm join-token manager
❯ docker node ls 
❯ docker node ps
❯ docker info (Verifique informações Swarm)
❯ docker swarm leave (Remove do Swarm, mas o node ainda consta no Cluster)
❯ docker node rm <ID>

# Infra pronta, agora iniciamos os serviços
# Service equivale a um container
❯ docker service create --name <name> <imagem>
❯ doker service ls
❯ doker service rm <ID> <Nome>
❯ docker service inspect <ID>

# Réplicas, Escalar
❯ docker service create --name nginx --replicas=3 -p 80:80 nginx
❯ docker service scale <nome_service>=<replicas>
❯ docker service update --image <Image> <Service>

# Descubra onde e quais containers estão rodando
❯ docker service ls
❯ docker service ps <ID_Service>

# Usando o compose 
❯ docker stack deploy -c <Arquivo.yaml> <nome_service>

# Node não recebe as Tasks do Manager
❯ docker node update --availability drain <ID_node>
❯ docker node update --availability active <ID_node>

# Criando redes para Swarm. Driver default: Overlay
❯ docker network create --driver overlay swarm
❯ docker service create --network swarm --name nome <image>
❯ docker service update --network-add swarm <ID_service>
```

**Para criar o laboratório no AWS, os seguinte passos foram realizados:

- **Na zona de Ohio foi criado um Security Group para liberar o acesso SSH-22, HTTP-80 e Docker-2377 (Inbound Rules)

```shell
# Amazon Linux AWS "centos rhel fedora"

ssh -i "docker-swarm-ohio.pem" ec2-user@ec2-13-58-33-107.us-east-2.compute.amazonaws.com

ssh -i "docker-swarm-ohio.pem" ec2-user@ec2-18-189-195-68.us-east-2.compute.amazonaws.com

ssh -i "docker-swarm-ohio.pem" ec2-user@ec2-3-145-44-57.us-east-2.compute.amazonaws.com

#!/bin/bash
sudo yum install docker -y \
&& sudo  service docker start \
&& sudo usermod -a -G docker ec2-user \
&& sudo reboot

```
Leia [[SySAdmin]], [[SSH]]

