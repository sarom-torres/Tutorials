# Alias 

## Pricipais comandos

- Listar os alias disponíveis: `alias -p`
- Remover um alias específico: `unalias alias_name`
- Remover todos os alias: `unalias -a`

# Criar Alias 

## Alias temporário

Para criar um alias temporário basta utlizar o comando `alias` seguido do nome e do comando que será associado aquele nome.
```
alias alias_name='command'
```

## Alias permanente
Para definir permanentemente um alias é possível incluí-lo diretamente no arquivo `~/.bashrc` ou criar um arquivo separado chamado `.bash_aliases`.

### Arquivo .bashrc
Nesse caso, basta incluir a linha do comando alias no arquivo `~/.bashrc`: 
```
alias alias_name='command'
```

### Arquivo .bash_aliases
Crie o arquivo `~/.bash_aliases` contendo todos os aliases necessários e acrescente o seguinte conteúdo no arquivo `.bashrc`:
```
if [ -f ~/.bash_aliases ]; then

. ~/.bash_aliases

fi
``` 
Ao reiniciar o sistema, esse novo arquivo contendo os alias será carregado, caso queira carregá-lo automaticamente após sua edição execute:
```
source ~/.bash_aliases

ou

. ~/.bash_aliases
```
