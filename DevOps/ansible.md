# Ansible

No Ansbile um _script_ é chamado de `playbook`. Um _playbook_ descreve quais `hosts` (servidores remotos) serão configurados e uma lista ordenada de `tasks` (tarefas) para executar neles.

O Ansible:
- Executa cada tarefa em paralelo em cada um dos hosts.
- Espera até que todos os hosts tenham completado ua tarefa antes de iniciar a execução da próxima tarefa.
- Executa as tarefas na ordem em que foram especificadas.

A sintaxe do Ansible é realizada em YAML, a qual é uma linguagem de formato de dados que facilita a leitura e a escrita de comandos para humanos.


## Características do Ansible

- Sintaxe de fácil leitura.
- Não há necessidade de instalação de agentes nos servidores remotos.
- Baseado em **_Push_**.
- Utiliza módulos para executar tarefas.
- Pequena camada de abstração.

## Arquivo ansible.cfg

O Ansible procura pelo arquivo `ansible.cfg` nos seguintes lugares e ordem:

- Arquivo especificado na variável de ambiente `ANSIBLE_CONFIG`.
- `.ansible.cfg` (arquivo no diretório atual).
- `~/.ansible.cfg` (arquivo no diretório `home`).
- `/etc/ansible/ansible.cfg`

## Comandos Iniciais 

- `-m`: define o módulo que será utilizado.
- `-b`: para executar o comando como root.

### Executar commandos no servidor remoto

Para executar comandos na CLI do servidor remoto é utilizado o módulo `command`. O comando a ser executado deve ser passado como argumento utilizando a flag `-a`. Conforme exemplo abaixo.
```
ansible <name-server> -m command -a <comando>
```
O módulo `command` geralmente é usado como módulo _default_, portanto é possível omití-lo durante a execução. Conforme exemplo:

```
ansible <name-server> -a <"comando com mais de uma palavra">
```
## True e Yes em Ansible

**Valores YAML** sinalizados como verdadeiros ou falsos seguem as convenções dessa linguagem, que são:

* YAML - Verdadeiro
```
true, True, TRUE, yes, Yes, YES, on, On, ON, y, Y
```
* YAML - Falso
```
false, False, FALSE, no, No, NO, off, Off, OFF, n, N
```
**Argumentos de módulos** são strings e são interpretados conforme convenções pré-determinadas pelo Ansible, que são:

* Argumento do Módulo - Verdadeiro
```
yes, on, 1, true
```

* Argumento do Módulo - Verdadeiro
```
no, off, 0, false
```
