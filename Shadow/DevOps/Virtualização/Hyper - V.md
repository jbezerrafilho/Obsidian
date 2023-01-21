----
#hypervisor #hyper-v #virtua-box

### História

A Microsoft pra variar dormiu no ponto com a vritualização, demorou a lançar o Hyper-V. Antes, porém, já utilizavam o Virtual PC para emular o Windows XP que tinha muita incompatibilidade com o Windows 7. A partir do Win 2008m, foi lançado a primeira versão do Hyper V.

### Tipos de Hypervisor

1. Baremetal - O Hypervisor tem contato direto com o hardware. Ex: Hyper V, VMWare, Citrix XenServer
2.  Hosted - O Hypervisor tem contato direto com o SO. Ex: Virtual Box


### Requirements

- Windows 10 ou Enterprise 64 bits
- Windows Server 2016 Standard ou DataCenter
- Processador 64 bits
- Virtualization enable in the BIOS
- [[Acrônimos#^eef5d1|DEP]] Data Execution Protection 
- [[Acrônimos#^c17aec|SLAT]] Second Level Address Translation 

>[!tip] `msinfo32 mostram o DEP e SLAT ativos`
>


>[!Note] Podemos rodar VM's a partir do Windows 10, Windows 2016 e Hyper V Server

 
### Virtual Switches

- **External - connects to a physical or wireless adapter
- **Internal - Parent and virtual machine connections only
- **Private - Virtual Machine Connections only

O host que gerencia o Hyper V tem um NIC  network interface card e cada VM possui um VNIC que é conectado à um switch virtual tal qual um switch físico.

[[Virtualização Aninhada]]
