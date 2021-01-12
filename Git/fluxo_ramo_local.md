## Fluxo de trabalho fazendo uso de ramos locais

```bash
git clone url-repositório

git checkout -b nome-branch

# edite arquivos
git add arquivos
git commit -m "mensagem"

git checkout master
git pull --rebase origin master
# se der conflito, resolva, faça git add e rebase --continue

git checkout nome-branch
git rebase master
# se der conflito, resolva, faça git add e rebase --continue

git checkout master
git rebase nome-branch
git push origin master

git branch -d nome-branch

```
