----


### Lab


![[Pasted image 20221227173331.png]]

>[!note] O objetivo deste Lab é trabalhar com cluster kubernetes em produção.

Foi criado um template com ubuntu 18.04 para gerar 04 VM's para o laboratório.
Veja [[SSH]]. Veja também [[VPC]]. Altere o [[SySAdmin#^ed9efd|hostname]] se necessário.

#dominio
O domínio pode ser adquirido no [Freenom](https://freenom.com), [Godaddy](https://www.godaddy.com/pt-br), [Hostinger](https://www.hostinger.com.br).


```shell
# Script para rodar no provisionamento #shebang

#!/bin/bash
sudo su
apt update && apt upgrade -y
curl https://releases.rancher.com/install-docker/20.10.sh | sh
usermod -aG docker ubuntu

# Install Docker-Compose
❯ sudo curl -L "https://github.com/docker/compose/releases/download/1.25.5/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

❯ chmod +x /usr/local/bin/docker-compose

❯ ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose

# Subindo e parando containers via Compose 
❯ docker compose -f rancher-composer.yml up -d
❯ docker-compose -f rancher-composer.yml down


```
Mais exemplo de  [[Script]].


>[!success] Rancher gerencia Kubernetes
>>[!todo] Kubernetes orquestra Containers 
>>>[!example] Docker cria os containers



```shell
# Criando o cluster kubernetes com o rancher

docker run -d --privileged --restart=unless-stopped --net=host -v /etc/kubernetes:/etc/kubernetes -v /var/run:/var/run rancher/rancher-agent:v2.4.3 --server https://104.154.135.147 --token hvmf4nwgz8gcvqbjdh6tr8gsjcxvh65rg7jwnkkphjfffd8nrf2d8x --ca-checksum 8cc424eaeb6c746c5a824403f59a073666fedf3c7d581af2d863f8012360983a --node-name k8s-3 --etcd --controlplane --worker

```










