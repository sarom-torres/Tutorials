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
**:<num_linha>** | Mover o cursor para uma determinada linha
**:$** | Mover o cursor para o fim do arquivo
**dd** | Deletar linha
**u** | Desfazer
