------
#k8s #orquestração

>💡 Todo o processo de implantação e gerenciamento automático de containers é conhecido        como orquestração. O K8S foi criado pelo Google.

**[[Swarm#Tecnologias de Orquestração|Tecnologias de Orquestração]]
Consulte [[Objetos K8S]].

#### Arquitetura 

-   Nodes Workers ( Minions - são hosts físicos ou virtuais onde o k8s está instalado e onde os containers vivem)
-   Cluster ( Agrupamento de vários nodes )
-   Node Master ( Gerencia os nodes do cluster )

>[!note]
>Node Master tem a finalidade de vigiar os nodes do cluster e orquestrar os constainers de cada node worker.


#### Conceitos 

- Control Plane : Gerencia - controla os processos nos nodes
- Deployment: Objeto que executa uma imagem / projeto num Pod
- Services: Serviços que expõe os Pod's ao mundo externo



#### Componentes

>[!abstract]
> -  **Servidor API** ( FrontEnd Kubernets - Usuários, gerenciadores de dispositivos, CLI, todos conversam com o API para interagir com o cluster Kubernetes )
> 
> -  **Etcd key store service** ( Armazenamento de key - value distribuído e confiável usado pelo k8s para aramazenar todos os dados usados para gerenciar os clusters )
> 
> -  **Scheduler** ( Atribui o trabalho dos containers por vários nodes. Ele procura por containers recém criados e os distribui pelos worker nodes)
> 
> - **Controller** ( Cérebro por trás da orquestração, são processos responsáveis por perceber e responder quando os containers, nodes e endpoints ficam inativos, criando novos containers )
> 
> - **Container Runtimer** ( Executa os containers. Usamos o docker. Poderia ser RKT ou CRI-O )
> 
> - **Kubelet Service** ( Agente que é executado em cada nó do cluster garantindo que os containers estejam sendo executados conforme o esperado )


### Master vs Worker Nodes

-   Master ( Kube API Server, etcd, controller, scheduller )
-   Worker Node ( Container Runtime, Kubelet )

### Utilitário kubectl Command

>[!note]
>Ferramenta usada para implantar e gerenciar aplicativos nos clusters kubernets. Serve ainda para obter informações dos clusters, obter status dos nodes, etc…


```shell
$ kubectl run hello-minikube 
$ kubectl cluster-info 
$ kubectl get nodes
```

Veja [[Objetos K8S]].




















