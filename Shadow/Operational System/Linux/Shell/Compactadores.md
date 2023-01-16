----


#### ZIP

Permite compactar arquivos no padrão no formato PKZIP e Winzip no padrão Windows. #zip

`$ zip -r dados.zip /etc/`


#### TAR
Permite  'empacotar' arquivos sem realizar compactação efetiva
Utilizado em conjunto com o padrão GZIP, compacta e descompacta 

- GZIP - Extensão "tar.gz" mais utlizada e efeciente na compressão
- BZIP2 - Extensão "tar.bz2"
- Compress - Extensão "tar.Z"

- c -> Compacta
- x -> Extrai
- t -> Lista conteúdo do arqquivo compactado
- z -> Modo de operação `gzip`
-  j -> Modo de operação `bzip2`
- Z -> Modo de operação `compress`
- f -> Operando com arquivos. O padrão é dispositivo de fita.
- v -> Verbose
- p -> Preserva as permissões do arquivo de origem
- r -> Acrescenta arquivos dentro do pacote tar

#tar-gzip
`$ tar czf dados.tar.gz /etc`
#tar-bzip2
`$ tar cjf dados.tar.bz2 /etc`




