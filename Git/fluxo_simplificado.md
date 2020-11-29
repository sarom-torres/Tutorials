## Fluxo de trabalho simplificado

Sugiro que faça a seguinte configuração no git de seu computador (configure uma única vez) para fazer o `rebase` a cada `git pull` e não um `merge`: 

`git config --global pull.rebase true` 


É possível trabalhar diretamente no ramo master local. Antes, 
```bash
git clone url-repositório

# trabalhe no relatório
git add arquivos
git commit -m "mensagem"
# repita os 2 passos acima quantas vezes for necessário


git pull --rebase origin master
# se der conflito, resolva, faça git add e git rebase --continue

git push origin master
```
