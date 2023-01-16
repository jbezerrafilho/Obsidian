
----

#ssh

```shell
# Evite quedas na conexão SSH por inatividade
$ vim ~/.ssh/config (Add 'ServerAliveInterval 50')

# Criando uma chave para VM no GCP
$ ssh-keygen -t rsa -f chave -C ubuntu (gerando chave)

#scp #copia-host-remote
❯ scp -i private_key path/file user@ip:/path

```

