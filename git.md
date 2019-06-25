# Git

Traz modificações do repositório remoto para o local, sem aplicar ao branch local

```bash
git fetch
```

Aplica modificações ao branch local

```bash
git merge
```

Atalho: fetch + merge

```bash
git pull
```

Cria uma branch a partir da branch atual (master)

```bash
git branch funcionalidade2
```

Vai para o novo branch

```bash
git checkout funcionalidade2
```

Atalho: branch + checkout

```bash
git checkout -b funcionalidade2
```

Lista as branchs do repositório local e verifica qual delas está em uso

```bash
git branch
```

Verifica o estado do repositório

```bash
git status
```

Envia a branch para o repositório remoto

```bash
git push origin funcionalidade2
```

Remove uma branch no repositório remoto

```bash
git push origin --delete NOME_DA_BRANCH
```

Remove uma branch no repositório local

```bash
git branch -d NOME_DA_BRANCH
```

Cria uma tag no repositório local

```bash
git tag 1.0.0
```

Lista as tags existentes

```bash
git tag
```

Envia uma tag para o repositório remoto

```bash
git push origin 1.0.0
```

Remove tag no repositório remoto

```bash
git push --delete origin TAG_NAME
```

Remove uma tag no repositório local

```bash
git tag -d TAG_NAME
```

Log de alterações

```bash
git log --graph --oneline --decorate --all
```

Integra um commit no master na branch funcionalidade2

```bash
git checkout funcionalidade2
git rebase master
```

Como funciona o git rabse:

1 - Mudanças na branch da funcionalidade são temporariamente removidas;

2 - Os commits novos existentes na master são trazidos para a branch da funcionalidade;

3 - Mudanças na branch da funcionalidade são novamente aplicadas na branch funcionalidade2;
