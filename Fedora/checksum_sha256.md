# Checksum sha256sum

`echo “<hash256ConhecidaDoArquivo> <filename>” | sha256sum --c`

ou

`echo “<hash256ConhecidaDoArquivo>  <filename>” | sha256sum --check

Exemplo:

`echo "65644342866e7bdea028ec1f12882538725ca438ebe016f62e545ff3f095a171 VirtualBox-6.1-6.1.16_140961_fedora32-1.x86_64.rpm" | sha256sum --check`
