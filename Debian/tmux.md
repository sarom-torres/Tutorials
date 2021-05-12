# Tmux

> O **Tmux** é um mutiplexador de terminal que permite executar multitarefas em diferentes sessões.

O Tmux é baseado em três ambientes para organizar as tarefas:
- `Sessões`: ambiente da tarefa global que está sendo executada. 
- `Janelas`: atividades executadas dentro de uma sessão.
- `Paineis`: varios ambientes dentro de uma janela.

Exemplo: 
É possível executar uma `sessão` para testes em um código. Dentro dessa sessão serão abertas duas `janelas`, uma para editar o código e outra para visualizar os diretórios. Dentro da janela de edição dos códigos serão criados três `painéis`: um para editar o código, outro para monitorar os processos  e o terceiro para monitorar os logs.
![image](https://user-images.githubusercontent.com/34520860/117897105-6ee1d880-b298-11eb-88fa-ce8150322a28.png)

## Instalando o Tmux

### Ubuntu / Debian
```
sudo apt install tmux
```
### Fedora
```
sudo yum install tmux
```

## Comandos Tmux 

### Comandos Externos
- `tmux`: inicia uma sessão Tmux.
- `tmux new -s <nome_da_sessao>`: inicia uma sessão Tmux com um nome pré-definido.
- `tmux detach`: sai da sessão atual, porém mantém o processo em plano de fundo.
- `tmux attach`: entra em uma sessão. 
- `tmux a -t <nome_da_sessao>`: especifica o nome da sessão para a qual se quer entrar.
- `tmux ls`: lista as sessões ativas.


### Comandos Internos

> O Tmux é controlado através do comando `CTRL+b`.

- `CTRL+b` `c`: cria uma nova janela.
- `CTRL+b` `n`: troca para a próxima janela.
- `CTRL+b` `p`: troca para a janela anterior.
- `CTRL+b` `,`: renomeia a janela.
- `CTRL+b` `,`: apresenta uma lista das janelas.
- `CTRL+b` `&`: fecha a janela atual atual.
- `CTRL+b` `%`: cria painéis na vertical.
- `CTRL+b` `"`: cria painéis na horizontal.
