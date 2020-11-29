# Instalando VirtualBox

1. Baixar virtualBox e fazer checksum.

[Link para download e checksum](https://www.virtualbox.org/wiki/Linux_Downloads)

2. Atualizar sistema.

`dnf update`

3. Instalar Qt e SDL para VirtualBox utilizar interface gráfica.

`dnf install @development-tools`

`dnf install kernel-devel kernel-headers dkms qt5-qtx11extras elfutils-libelf-devel zlib-devel`

4. Instalar VirtualBox.

`dnf install <file.rpm>`

5. Durante a instalação o VirtualBox cria um grupo chamado vboxusers. Todos usuários que utilizarão a entrada usb a partir do VirtualBox devem ser incluídos nesse grupo.

`usermod -a -G vboxusers <username>`
