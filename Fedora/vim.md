# Utilizando o editor vim

## Modos de operação

Existem diversos tipos de modos de operação no vim, os três modos básicos são:
- **Normal:** para navegação e edições simples. `ESC`;
- **Insert:** para inserção explicita e mudanças no texto. `i`;
- **Visual:** para identificar trechos de texto. `v`;

## Comandos básicos
Comando | Descrição
:-------| :--------
**:q!** | Sair sem salvar
**:w**|Salvar
**:x!** ou **:wq** | Salvar e sair
**:set number** | Mostrar a numeração das linhas

## Comandos de movimentação
Comando | Descrição
:-------| :--------
**0** | Mover o cursor para o início da linha
**$** | Mover o cursor para o fim da linha
**:<num_linha>** | Mover o cursor para uma determinada linha
**gg** | Mover o cursor para o início do arquivo
**:$** ou **G** | Mover o cursor para o fim do arquivo

## Comandos de edição
Comando | Descrição
:-------| :--------
**dd** | Deletar linha
**dw** | Deletar palavra
**daw**| Deletar palavra e espaços antes e depois
**SHIFT + D** | Deletar do cursor até o final da linha
**u** | Desfazer
**yy** | Copiar texto de uma linha
**<qt_linhas>yy** | Copiar texto de uma quantia específica de linhas 
**yw** | Copiar uma palavra
**y$** | Copiar texto do cursor até final do arquivo
**p** | Colar texto que foi copiado
**gg=G** | Identar o texto de todo o arquivo
**=G** | Identar o texto a partir da linha do cursor

## Comandos de busca
Comando | Descrição
:-------| :--------
**/[palavra-chave]** | Procura palavra-chave no documento
**:s/[palavra-chave]/[nova-palavra]** | Substituir palavra-chave por nova-palavra na linha atual
**:1,10 s/[palavra-chave]/[nova-palavra]** | Substituir palavra-chave por nova-palavra da linha 1 até a linha 10
**:1,$ s/[palavra-chave]/[nova-palavra]** | Substituir palavra-chave por nova-palavra da primeira linha até o fim do arquivo
