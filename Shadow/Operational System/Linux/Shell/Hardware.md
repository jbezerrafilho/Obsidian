-----

#dmesg 
`$ dmesg - exibe o registro de toda inicialização`

#mensagens_sistema_tempo_real 
`$ cat /proc/kmsg  - exibe as mensagens do sistema em tempo real`

#lspci
`$ lspci - lista dispositivos pci`

#lsusb
`$ lsusb - lista dispositvos USB`

#lsmod
`$ lsmod - lista os módulos(drivers) linux`

#insmod
`$ insmod <arquivo> <opcoes> - instala, carrega o módulo no kernel`

#rmmod
`$ rmmod <nome_modulo> - remove o módulo driver desativando o hardware`

**Mais informações de hardware no path `/proc`
- Diretório virtual
- Uso exclusivo do kernel para gerenciamento do sistema e seus recursos
- Existe apenas enquanto o computador está ligado
- Não podemos gravar ou criar neste diretório

#cpuinfo
`$ cat /proc/cpuinfo`
`$ cat /proc/meminfo`
`$ cat /proc/scsi/scsi`
