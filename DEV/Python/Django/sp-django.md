# Usando Djangosaml2

## Preparando ambiente de instalação

Instale as bibliotecas mínimas necessárias para o funcionamento do djangosaml2.
```
apt-get install libxml2-dev libxmlsec1-dev libxmlsec1-openssl python3-pip xmlsec python3-dev libssl-dev libsasl2-dev
```
Instale, crie e ative o ambiente virtual.
```
pip3 install virtualenv
mkdir djangosaml2_project && cd "$_"
virtualenv -ppython3 env
source env/bin/activate
```

Instale o djangosaml2
```
pip install djangosaml2
```
