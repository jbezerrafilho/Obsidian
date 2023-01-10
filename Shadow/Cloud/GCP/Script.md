----
#script #gce #google #cloud #engine

#### Explorando algumas opções

1. Startup Script (Cole Dentro de Management > Automation )

```bash
#shebang

#!/bin/bash
apt update
apt -y install apache2
echo "Hello World from $(hostname) $(hostname -I)" > \
/var/www/html/index.html
```


2. Instance Template

A criaçao tem um custo na inicialização. O recomendado é a criação de uma imagem.

3. Custom Images




