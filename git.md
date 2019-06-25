# GIT

Traz modificações do repositório remoto para o local, sem aplicar ao branch local

```git fetch```

Aplica modificações ao branch local

```git merge```

Atalho: fetch + merge

```git pull```

Cria uma branch a partir da branch atual (master)

```git branch funcionalidade2```

Vai para o novo branch

```git checkout funcionalidade2```

Atalho: branch + checkout

```git checkout -b funcionalidade2```

Lista as branchs do repositório local e verifica qual delas está em uso

```git branch```

Verifica o estado do repositório

```git status```

Envia a branch para o repositório remoto

```git push origin funcionalidade2```

Remove uma branch no repositório remoto

```git push origin --delete NOME_DA_BRANCH```

Remove uma branch no repositório local

```git branch -d NOME_DA_BRANCH```

Cria uma tag no repositório local

```git tag 1.0.0```

Lista as tags existentes

```git tag```

Envia uma tag para o repositório remoto

```git push origin 1.0.0```

Remove tag no repositório remoto

```git push --delete origin TAG_NAME```

Remove uma tag no repositório local

```git tag -d TAG_NAME```
