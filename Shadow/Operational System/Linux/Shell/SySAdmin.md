------

#services
```shell

❯ sudo service docker status
❯ sudo  service docker start (Serviço enable temporário, após reboot fica off)
❯ sudo chkconfig docker on (Serviço habilitado após o reboot)
❯  systemctl status mariadb.service 
❯  systemctl is-enabled mariadb.service
```

#hostname
`❯ hostnamectl set-hostname <hostname>` ^ed9efd

#setup-keyboard #abnt
`❯ loadkeys br-abnt2`  

#gerenciador-pacotes
`❯ apt-cache search mariadb.server`

#listen #ports
`❯ netstat -lntp`


#encerrar-sessao
❯  `exit` 
❯  `logout`
❯  `Ctrl D`

#reiniciar #restart
❯ `reboot`
❯ `init 6`
❯ `Ctrl Alt Del`

#Desligar #shutdow
❯ `shutdown -h now`
❯ `init 0`
❯ `halt`
❯ `poweroff`

❯ `uname a - print system information` #system_information
❯ `cat /etc/redhat-release `
❯ `cat /etc/os-release - mais completo que o anterior` #versao_so
❯ `cat /etc/debian_version `
❯ `cat /etc/os-release  - mais completo que o anterior` #versao_so  
❯ `free -m - exibe memoria em MB` #memoria

❯ `df -h - reporta o espaço usado pelos pontos de montagem no disco` #disk_free

❯ `du -hs - espaço usado pelos arquivos num diretório` #du #disk_usage

❯  `w - usuários conectados`

==========================================================

#### NET








