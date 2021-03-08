# Ansible

No Ansbile um _script_ é chamado de **_playbook_**. Um _playbook_ descreve quais **_hosts_** (servidores remotos) serão configurados e uma lista ordenada de **_tasks_** (tarefas) para executar neles.

O Ansible:
- Executa cada tarefa em paralelo em cada um dos hosts.
- Espera até que todos os hosts tenham completado ua tarefa antes de iniciar a execução da próxima tarefa.
- Executa as tarefas na ordem em que foram especificadas.

A sintaxe do Ansible é realizada em YAML, a qual é uma linguagem de formato de dados a qual facilita a leitura e a escrita de comandos para humanos.
