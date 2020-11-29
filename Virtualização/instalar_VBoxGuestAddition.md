# Instalando VBoxGuestAddition

## Instalar VBoxGuestAddition em Ubuntu18.04 Guest 

* Clique em **Dispositivos** > **Inserir imagem de CD dos Adicionais para Convidado**
![Inserindo imagem iso](/Virutalização)

* Faça a montagem do cdrom com seguinte comando :

```
sudo mount /dev/cdrom /media/cdrom
``` 

* A montagem também pode ser feita usando o gerenciador de arquivos clicando com o botão direito do mouse na mídia e em seguida em `mount`

* Após a montagem acessar o diretório `/media/<username>/VBox_GAs` e executar o arquivo `VBoxLinuxAdditions.run`.

```
cd /media/<username>/VBox_GAs
sudo ./VBoxLinuxAdditions.run
```

* Reiniciar Guest.

* Para habilitar compartilhamento da área de transferência acessar o menu **Dispositivos** > **Aréa de tranferência compartilhada** > **Bidirecional**. Este passo permitirá usar o recurso de copia e cola entre o *host* e o *guest*.

* Para aumentar o tamanho da tela acessar o menu **Visualizar** > **Ajustar tamanho da janela**. Este passo permitirá ajustar o tamanha da janela do *guest* para ocupar a tele inteira.

### Possíveis exceções durante a instalação: 

### :exclamation: Erro no carregamento do módulo `iso9660` no kernel

Durante o processo de montagem da mídia é possivel ocorrer o seguinte erro:

**Mensagem de erro:**

`mount: unkown filesystem type 'iso9660'`

**Solução:**

O módulo `iso9660` não foi carregado. Para analisar os módulos do kernel e criar uma lista de dependências basta usar o comando `depmod`.

`sudo depmod -a`
 
Na sequência fazer a montagem do cdrom novamente e continuar o processo de instalação do *VBoxGuestAddition*.

### :exclamation: Erro ao inserir o disco óptico virtual 

Durante o processo de montagem da mídia é possivel ocorrer o seguinte erro:

**Mensagem de erro:**

`Could not mount the media/drive '/usr/share/virtualbox/VBoxGuestAdditions.iso' (VERR_PDM_MEDIA_LOCKED).`

**Solução:**

* Desligue o *guest*.
* Entre em **Configurações** > **Armazenamento**.
* Clique com o botão direito do *mouse* em VBoxGuestAdditions.iso
* Clique em remover conexão.
* Reinicie o processo de instalação *VBoxGuestAddition*.

### :exclamation: Não concluir o processo de execução do VBoxLinuxAdditions.run

Algumas bibliotecas devem estar instaladas para a execução do arquivo `VBoxLinuxAdditions.run`.
Por exemplo:

* make
* gcc
* perl

Para instalar esses pacotes basta usar os seguinte comandos:

```
sudo apt install build-essential
sudo apt-get install perl
```














