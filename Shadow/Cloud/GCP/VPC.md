
### Virtual Private Cloud

- VPC é recurso Global do Google
- Não está vinculado a uma região apenas
- Rede Isolada dentro do Google Cloud Provider - GCP
- Controle total do que entra e sai
- Best Practice - Crie todos os recursos GCP (Compute, storages, databases) dentro da VPC
- Contém Subnets que podem estar em uma ou mais regiões


### Necessidade de Subnets?

- Recursos como VM, Storages, Load Balancer tem necessidades diferentes
	- VMs, Storages - recurso privado de acesso externo da internete
	- Load Balance - recurso público com acesso à internet

- Como separar os recursos conforme a necessidade? 
	- Subnets

- Alta Disponibilidade - Distribuir recursos em regiões diferentes através das Subnets
-


### Criando VPCs e Subnets

- By default, cada projeto tem sua VPC padrão
- Ao criarmos nossa própria VPC,  temos duas opções:
	- Auto mode: Subnets criadas automaticamente em cada região
	- Custom mode: Subnets criadas manualmente (Recomendado para produção)

- Opções ao criarmos subnets
	- Habilitar Private Google Access - Permite VM's conectarem às API's do Google usando IP privado
	- Enable FlowLogs - Troubleshoot da VPC


### CIDR (Classless Inter-Domain Routing) Blocks

<p>Notação para descrever blocos de endereços IP e é usado fortemente em várias configurações de rede. Os endereços IP contêm 4 octetos, cada um consistindo de 8 bits dando valores entre 0 e 255. O valor decimal que vem após a barra é o número de bits que consiste no prefixo de roteamento. Isso, por sua vez, pode ser traduzido em uma máscara de rede e também designa quantos endereços disponíveis estão no bloco.</p>
[CIDR](http://cidr.xyz)

### Firewall Rules

- Configure a regra para entrada e saída de tráfego
	- Stateful - Set up  padrão do Firewall (Tudo que entra, sai)
	- Defina prioridades: 0 -  mais alta, 65535 - mais baixa
	- Regra Default implícita com prioridade 65535:
		- Permite qualquer saída (egress)
		- Nega qualquer entrada (ingress)
		- Regra default não pode ser excluída
		- Pode-se sobrescrever (Override) definindo nova regra com prioridade maia alta
	 - Default VPC tem 4 rules com prioridade 65534
		 - **default-allow-internal (Comunicação interna VM's)
		 - **default-allow-ssh (incoming TCP porta 22- Linux)
		 - **default-allow-RDP (incoming TCP porta 3389 - Windows)
		 - **default-allow-icmp (incoming ICMP from any source on the network)


#### Ingress and Egress Rules


