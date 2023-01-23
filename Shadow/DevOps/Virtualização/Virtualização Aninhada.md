------

**Para simular o laboratório faremos uso de um Host com win 11, subiremos uma VM com win Server 2019. É necessário expor a virtualização da VM com Windows 2019  através do comando abaixo.

#powershell #hyper-v_cli

```shell
	
	Set-VMProcessor -VMName hostname -ExposeVirtualizationExtensions $true
	Start-VM -Name vm1, vm2 (Iniciando VMs pelo Shell)
	Add-VMNetworkAdapter -VMName "centOS7" -Name "LAN" -DeviceNaming ON (Criando NIC)
	New-VMSwitch -Name "InternalNat" -SwitchType Internal (Criando um Switch Virtual)
	
	------------------------------------------------
	
	#NAT_Hyper-V
	
	Get-NetAdapter (Descobrir o índice da interface de rede)
	New-NetIPAddress -IPAddress 192.168.0.1 -PrefixLength 24 -InterfaceIndex 56      
	New-NetNat -Name "NATinterno" -InternalIPInterfaceAddressPrefix 192.168.0.0/24
	Remove-NetNat -Name "NATinterno"
	
	#powershell_direct #powershell_ISE
	
	Enter-PSSession -VMName rts-dc1 
	
	#criar-diretorio
	New-Item -ItemType Directory C:\Hyper-V ou mkdir c:\Hyper-V
```
