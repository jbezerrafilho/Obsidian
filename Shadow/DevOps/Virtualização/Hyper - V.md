----

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
