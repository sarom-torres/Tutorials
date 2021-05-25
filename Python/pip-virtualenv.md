## PIP
`pip` é uma ferramenta para instalação de pacotes Python que estão no repositório [PyPi (Python Package Index)](https://pypi.org/).

- Para **instalar** o pip3 use o seguinte comando:
```
$ sudo apt install python-pip3
```
- Para checar a **versão** do pip

```
$ pip3 --version
```
- Para **listar** os packages instalados
```
$ pip3 list
```
- Para **mostrar informações** de um package instalado
```
$ pip3 show [package-name]
```
## Virtualenv
`virtualenv` é uma ferramenta pra criar ambientes Python isolados e que contém sua própria cópia de:
- interpretador python
- pip
- sites-packages (bibliotecas instalada a partir do PyPI)

- Para instalar o virtualenv globalmente:
```
$ sudo pip3 install virtualenv
```
- Criar um **novo virtualenv**
```
$ cd ~/[diretorio-projeto]
$ virtualenv env
``` 
  1. `env` é, por convenção, o nome do diretório na qual o ambiente virtual será criado `~/[diretorio-projeto]/env/`
  2. caso o `git` seja usado, **não** deve ser feito o commit do repositório env.

- Para **instalar um pacote** no virtualenv
```
$ env/bin/pip3 install [nome do pacote]
```
- **Executar script** no virtualenv
```
$ env/bin/python3 [script]
```
- Para usar o interpretador e o pip do ambiente virtual sem digitar o caminho `env/bin` use:
> Esse comando deve ser executado sempre que o terminal for reiniciado
```
$ source env/bin/activate
```
- Para checar qual interpretador ou pip está sendo usado:
```
$ which python   
/usr/bin/python   ## global

$ which python   ## ambiente virtual
/home/user/[diretorio-projeto]/env/bin/python
```
- Parar de usar o interpretador e pip de um ambiente virtual:
```
deactivate
```

## Arquivo requirements.txt 

O arquivo `requirements.txt` é usado para instalar as dependências necessárias para um determinado ambiente virtual e pode ser definido da seguinte maneira:
```
$ env/bin/pip3 install -r requirements.txt
```
## Referências
[Tutorial - dabapp](https://www.dabapps.com/blog/introduction-to-pip-and-virtualenv-python/)
