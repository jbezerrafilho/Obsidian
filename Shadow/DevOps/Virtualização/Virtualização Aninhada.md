------

**Para simular o laboratório faremos uso de um Host com win 11, subiremos uma VM com win Server 2019. É necessário expor a virtualização da VM com Windows 2019  através do comando abaixo.

#powershell #hyper-v_cli

```shell
	Set-VMProcessor -VMName hostname -ExposeVirtualizationExtensions $true
	Start-VM -Name vm1, vm2 (Iniciando VMs pelo Shell)
	
```
