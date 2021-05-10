## :mag: Comandos para instalar o grep manualmente.

Para fazer download e descompatar o arquivo use os seguintes comandos:
```
$ wget https://ftp.gnu.org/gnu/grep/grep-3.3.tar.xz
$ tar -Jxf grep-3.3.tar.xz
```
Entre no diretório e execute o Makefile:
```
$ cd grep-3.3/
$ ./configure
$ make
$ sudo make install
```
Verifique o local de instalação e a versão do grep instalado
```
$ type -a grep
$ grep -V | head-n1grep (GNU grep) 3.3
``` 

