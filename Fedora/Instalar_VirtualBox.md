# Instalando VirtualBox

* Baixar virtualBox e fazer checksum.

[Link para download e checksum](https://www.virtualbox.org/wiki/Linux_Downloads)

* Atualizar sistema.

```
dnf update
```

* Instalar Qt e SDL para VirtualBox utilizar interface gráfica.

```
dnf install @development-tools

dnf install kernel-devel kernel-headers dkms qt5-qtx11extras elfutils-libelf-devel zlib-devel
```

* Instalar VirtualBox.

```
dnf install <file.rpm>
```

* Durante a instalação o VirtualBox cria um grupo chamado vboxusers. Todos usuários que utilizarão a entrada usb a partir do VirtualBox devem ser incluídos nesse grupo.
```
usermod -a -G vboxusers <username>
```
