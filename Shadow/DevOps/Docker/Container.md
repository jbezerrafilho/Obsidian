----
#docker #container

❯ [[Imagens]], [[Volumes]], [[Network]]

###### Criando Container's


 ```Docker
# Subindo, Reiniciando e Executando Containers

❯ docker info
❯ docker run -it ubuntu (-it intereactive terminal);
❯ docker run -d -p 3000:80 nginx (-p porta 3000 host, 80 nginx)
❯ docker start -ai container (Reinicia o container que está parado)
❯ docker exec -it container bash (Executa o comando bash num container em   
execução)

# Parando e Removendo Containers

❯ docker stop -t 0 container
❯ docker rm container 
❯ docker rm container --force (Caso esteja em execução)
❯ docker rm $(docker ps -aq) --force (Remove todos os containers)
❯ docker container prune (Remove containers parados)

# Logs

❯ docker logs -f container (-f follow)
 
# Por ser efêmero, podemos utilizar um container e descartá-lo

❯ docker run -it -rm ubuntu (-rm remove)

# Utilitários & Análise

❯ docker cp node:/app ./dir_host/ (Copia arquivos entre container e host)
❯ docker top container (Lista processos em execução no container)
❯ docker inspect container
❯ docker stats (Lista consumo de CPU, MEM, NET, I/O de cada container em execução)

```

>❯ docker system prune; (Remove imagens, containers e networks não utilizados)


