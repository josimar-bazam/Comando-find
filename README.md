# Comando - find

Usando o comando find para listar extensão de arquivos.

**Objetivo é apresentar alguns exemplos que pode ajudar no dia a dia, caso alguém precise listar quais arquivos ou extensão estão presente dentro de um arquivo que possui código fonte com diferente tipo de extensão**

```
Navegar até o diretório onde esta o arquivo ou pasta.
$ cd /user/nome-arquivo/
$ find . -type f | sed -n 's/..*\.//p' | sort | uniq -c

Um exemplo que o find vai trazer de informação de quantos arquivos;

7 babelrc
   5 conf
   2 config
   4 dockerignore
   1 ebextensions/logrotate/abc-agentes
   1 ebextensions/patterns/nginx
   7 env
   1 eslintignore
  60 feature
   2 featurebookignore
   1 gif
  19 gitignore
  24 gitkeep
   5 groovy
 237 html

Listar extensão de arquivos dentro de um diretório.

$ cd /user/nome-arquivo/
$ find .

Exemplo;

$ find .
.
./.gitignore
./migrations_btg
./migrations_abc/CLIENT_TESTE_APP1

Removendo todos os arquivos uma determinada extensão:

Exemplo, na pasta /user/ tem um arquivo com a extensão .xml

$ find user/ -name *.xml -exec rm {} \;

Através do exemplo acima, serão localizados todos os arquivos com extensão .xml, dentro do diretório “/user/”. 
Podemos, alterar “*.xml” por qualquer outra extensão de arquivo, como por exemplo “*.png”, “*.css”, “*.html” e entre outros.



```
