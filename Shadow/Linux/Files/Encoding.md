----
#utf #encodig #unicode

❯ Unicode é uma tabela que define um codepoint para todos dos caracteres existentes no mundo.

❯ UTF-8 -> Unicode Transformation Format 8 bits. É um tipo de enconding que define o formato binário de cada caractere. Outros de tipos de encoding: UTF-16, ASCCII, WINDOWS 1252.

❯ Encoding e Charsert são sinônimos em JAVA.


```Shell
# Descobrindo o CharSet - Encoding
❯ file funcoes.txt 
funcoes.txt: ISO-8859 text, with CRLF line terminators

# Mudando o encoding do arquivo funcoes.txt
❯ iconv -f ISO-8859-1 -t UTF-8 funcoes.txt > funcoesN.txt
```
