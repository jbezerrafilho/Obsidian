-----
#docker #image 

❯ [[Container]], [[Volumes]], [[Network]]

>As imagens são divididas em camadas.
 Cada instrução no Dockerfile representa uma layer
 Quando algo é atualizado, apenas as layers depois da linha atualizada são refeitas
 O resto permanece em cache, tornando o build mais rápido


### Instruções básicas 

- **FROM : imagem base;
- **WORKDIR: diretório da aplicação
- **EXPOSE: Porta da aplicação
- **COPY : Cópia de arquivos necessários

```bash

❯ docker build . (Criando uma imagem no dir atual)
❯ docker tag id nome_imagem:tag
❯ docker build -t meu_app:tag  . (-t tag)
❯ docker rmi image -f (-f force pra imagens vinculadas)
❯ docker image prune
❯ docker rmi $(docker image ls -aq) --force

```

### Enviando imagens para o Docker Hub

```shel
❯ docker login
❯ docker logout

# Antes de enviar a imagem, crie um repositório no Hub Docker
❯ docker build -t jbezerrfilho/node . (Criando a imagem)
❯ docker push jbezerrafilho/node (Enviando a imagem)
```

 [Hub Docker](https://hub.docker.com)


 