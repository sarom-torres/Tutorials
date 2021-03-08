## Listar nomes de usuário

Para listar os nomes de usuário basta utilizar o comando `cat` para mostrar o conteúdo do arquivo `/etc/passwd`. 
Para filtrar a saída do comando e mostrar apenas os nomes de usuário use o comando abaixo, em que `-F` descreve o separador.
 ``` 
 cat /etc/passwd | awk -F: '{print $1}'
```
ou
```
cat /etc/passwd | cut -d: -f1
```
## Listar usuários conectados

Para listar usuários conectados use os comandos `who` ou `users`.

## Listar grupos do usuário atual

Para listar os grupos a qual o usário atual pertence basta usar o seguinte comando:
```
groups <username>
```

## Listar grupos

Para listar todos os grupos do sistema basta utilizar o comando `cat` para mostrar o conteúdo do arquivo `/etc/groups`. 
Para filtrar a saída do comando e mostrar apenas os nomes dos gropus use o comando abaixo, em que `-F` descreve o separador
 ``` 
 cat /etc/group | awk -F: '{print $1}'
```
ou
```
cat /etc/group | cut -d: -f1
```

### Referências
- [Devconnected](https://devconnected.com/how-to-list-users-and-groups-on-linux/#:~:text=In%20order%20to%20list%20groups,groups%20available%20on%20your%20system.).

