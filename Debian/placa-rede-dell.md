# Configuração de placa de rede Dell

## Checando informações da placa

 Verificar vendor e modelo de placas de rede
```
#  lspci -nnk | grep -iA2 net
```

Logs de update
```
# dmesg | grep ath10k
```

## Instalação driver de wireless proprietaro Qualcomm

### Adicionar os repósitórios non-free na lista

Abra o arquivo `source.list`

```
# vim /etc/apt/sources.list
```
Onclua no arquivo as seguintes linhas

```
# contrib non-free
deb http://deb.debian.org/debian buster main contrib non-free
deb-src http://deb.debian.org/debian buster main contrib non-free

deb http://deb.debian.org/debian-security/ buster/updates main contrib non-free
deb-src http://deb.debian.org/debian-security/ buster/updates main contrib non-free

deb http://deb.debian.org/debian buster-updates main contrib non-free
deb-src http://deb.debian.org/debian buster-updates main contrib non-free
```

Faça o update de pacotes proprietaros
```
# apt update
# apt list --upgradable -a
# reboot
```
