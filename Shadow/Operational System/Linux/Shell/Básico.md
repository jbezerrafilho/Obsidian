----
#buscareversa #comandos_basicos #bash-aliasing 

```shell

#alias
$ alias ls="ls --color" (Highlight default)

#history #! #recuperar-comando
$ history (Exibe comandos anteriores)
$ !10 (Executa o comando na posição 10 ho history)

#mkdir 
$ mkdir dir{01,02,03} (Cria três diretórios)
$ mkdir dir1/sub1 -p (Cria o diretório pai caso não exista)
$ mkdir -p curso/{linux,redes,servidores}

#apagar-arquivos #apagar-diretórios
$ rmdir dir01
$ rm -rf dir01 (Apaga diretórios e arquivos - CUIDADO!)

#link-simbolico
$ ln -s curso/linux/dir01/peba.txt peba.txt (link para arquivo)
$ ln -s curso/linux/dir01 dir01 (link para diretório)

#find-files 
$ find . -name peba.txt (Procure no dir atual o arquivo peba.txt)

#du #disk-usage
$ du -h
$ du -hs (h - humano, s - summarize)
$ du -chs * (Tamanho individual de cada pasta)

#visualizadores-arquivo #cat #more #less #head #tail #tail-log
❯ cat query.sql (Visualiza conteúdo do arquivo) 
❯ more query.sql (Visualiza conteúdo com paginação) 
❯ head query.sql (Visualiza as 10 primeiras linhas) 
❯ tail query.sql (Visualiza as 10 últimas linhas)
❯ tail -f  /var/log/audit/audit.log (Monitora saída logs, f - follow)

(Aprimoração do more, use a / para pesquisa, 'n' para próxima ocorrência, 'Shift n' para ocorrência anterior)
cless query.sql 
  		
#i/o 
Operações de I/O possuem três variações que são chamadas de descritores:
- stdin:  0, entrada padrão (teclado)
- stdout: 1, saída padrão (tela do terminal)
- stderr: 2, saída padrão (filtra os erros)

#redirecionador 
#> #>> 
Os redirecionadores '> e >>' tem a funçao de enviar para um arquivo por exemplo.
❯ ls /dev/ > /root/dispositivos.txt 
('1>', este descritor 1 está implícito. Poderia ser o '2>')
❯ du -hs * >> /root/ok.txt 2>> /root/erro.txt 
(Muito usado para migração de dados, por exemplo)

#< #<<
Os redirecionadores '< e <<' faz com que um determiando comando receba algo como entrada

#buraco-negro #dev-null #bit-bucket
Para economizar espaço no disco e ao mesmo tempo não usarmos o buffer, podemos direcionar a saída para '/dev/null', pois toda informação enviada para ele será descartada.

#concatenaçao
A saída de um comando se torna a entrada de outro comando. Utilizamos o
'|'.

#conectores 
$ clear; cd /etc; cp -a services /root 
(; - conector, não confunda com concatenação)

#filtros #grep #egrep
$ grep "bash" /etc/passwd
$ cat /etc/passwd | grep "bash"
$ grep -v "bash" /etc/passwd (v - invert match)
$ grep -r "bash" /etc/* (filtra a string 'bash' de forma recursiva)

O grep pode ser utlizado também em conjunto com algum metacaracter fazendo o papel que é do egrep - utilizado para expressões regulares.

$ ls -l /etc/ | grep ^d (^ - meta que indica início da linha com 'd')
$ ls -l /etc/ | grep ^d -v (v - invert match)

O egrep permite o uso de Regex em sua sintaxe para uma busca mais elaborada.
$ ls -l /etc | grep ^d -v | egrep "Dec|2020"
(Pesquise arquivos ignorando as linhas que começam com 'd' e refine a pesquisa com 'Dec' ou '2020')

$ ls -l /etc | grep ^d -v | egrep "Dec.*2020" (Dec && 2020)

```




	
