# Utilizando o editor vim

## Modos de operação

Existem diversos tipos de modos de operação no vim, os três modos básicos são:
- **Normal:** para navegação e edições simples. `ESC`;
- **Insert:** para inserção explicita e mudanças no texto. `i`;
- **Linha de comando:** para operação tais como salvar, sair, etc.

## Comandos básicos

### Modo INSERÇÃO
Comando | Descrição
:-------| :--------
**:q!** | Sair sem salvar
**:w**|Salvar
**:x!** ou **:wq** | Salvar e sair
**:set number** | Mostrar a numeração das linhas
**0** | Mover o cursor para o início da linha
**$** | Mover o cursor para o fim da linha
**:<num_linha>** | Mover o cursor para uma determinada linha
**dd** | Deletar linha
**u** | Desfazer
**gg** | Mover o cursor para o início do arquivo
**:$** ou **G** | Mover o cursor para o fim do arquivo
**yy** | Copiar texto de uma linha
**<qtdade_linhas>yy** | Copiar texto de uma quantia específica de linhas 
**yw** | Copiar uma palavra
**y$** | Copiar texto do cursor até final do arquivo
**p** | Colar texto que foi copiado
