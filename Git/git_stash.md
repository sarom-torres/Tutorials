# Git Stash

## Caso queira baixar novidades do remoto e tenha alterações locais que ainda não quer fazer *commit*

É possível estar trabalhando localmente e não ter concluído o trabalho ao ponto de querer fazer um *commit*, mas ainda assim querer as novidades do repositório remoto (*commits* novos que foram colocados por lá). Para tal pode-se fazer uso do `git stash`. O fluxo seria:

```bash
# O diretório irá para o estado limpo
git stash

# Para trazer os últimos commits que estão no remoto
git pull origin master

# Para trazer para o diretório de trabalho as alterações que colocou no stash
git stash pop
```

Após isso seu repositório local estará sincronizado com o repositório remoto e ainda assim você terá as alterações que fez.

**Atenção:** Se as alterações que fez forem nas mesmas linhas que vieram com o `git push`, então você terá um `merge conflict` que terá que resolver manualmente. Use o Visual Studio Code para te ajudar a encontrar e resolver.

Uma vez que resolveu os conflitos, então você precisará fazer:

```bash
git add arquivos-com-conflito
```
