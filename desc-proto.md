# PTC_Projeto1

## Execução do protocolo:

* Dentro do diretório do projeto vá até o diretório `cmake-build-debug`:
```
$ cd cmake-build-debug
```
* Execute duas instâncias do protocolo passando como argumento o nome da porta serial que será utilizada. 
Cada instância pode ser executada utilizando o seguinte comando.
```
$ ./protocol-1 [nome-porta-serial]
```

## Sequência de operações que serão mostradas durante a execução do protocolo
Serão apresentados em telas os dados no seguinte formato:
``` 
[{CAMADA}] {método-da-classe} -> {nome-variável}: {status}
```

### Transmissão

* Serão apresentados os dados obtidos do terminal.
* Na sequência será exibida mensagem a ser transmitida contendo as flags e o cabeçalho, além da quantidade de bytes enviados.
* Em caso de timeout na camada ARQ, pacote de dados é reenviado e seu conteúdo é mostrado em tela.

### Recepção
* As mensagens apresentadas em tela especificam se é uma mensagem de ACK ou um pacote de dados.
* Em caso de sucesso, será exibida mensagem Good FCS, bem como seu conteúdo representando que não houve corrompimento no pacote.
* Caso contrário, será exibida a mensagem de Bad FCS e o pacote será descartado.
