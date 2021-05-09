# Como mudar o layout do teclado

## Editando o arquivo de configuração

As configurações de teclado estão armazenadas no arquivo `/etc/default/keyboard` por meio das seguintes diretivas:
```
# KEYBOARD CONFIGURATION FILE

# Consult the keyboard(5) manual page.

XKBMODEL="pc105"
XKBLAYOUT="br,us"
XKBVARIANT=""
XKBOPTIONS=""

BACKSPACE="guess"
```
Em que:

- `XKBMODEL`: é a variável referente ao modelo do teclado. O arquivo `/usr/share/X11/xkb/rules/base.lst` contém as opções das vaŕivás e os seus repectivos modelos.
- `XKBLAYOUT`: contém a lista de layouts utilizados. Os valores da lista devem ser separados por virgula.

## Usando DPKG

É possível modificar o layout usando o dpkg:

``` 
dpkg-reconfigure keyboard-configuration
```
