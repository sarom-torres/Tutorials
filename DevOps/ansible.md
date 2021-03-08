# Ansible

No Ansbile um _script_ é chamado de `playbook`. Um _playbook_ descreve quais `hosts` (servidores remotos) serão configurados e uma lista ordenada de `tasks` (tarefas) para executar neles.

O Ansible:
- Executa cada tarefa em paralelo em cada um dos hosts.
- Espera até que todos os hosts tenham completado ua tarefa antes de iniciar a execução da próxima tarefa.
- Executa as tarefas na ordem em que foram especificadas.

A sintaxe do Ansible é realizada em YAML, a qual é uma linguagem de formato de dados a qual facilita a leitura e a escrita de comandos para humanos.


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
