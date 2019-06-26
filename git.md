# Git

## Comandos básicos

Traz modificações do repositório remoto para o local, sem aplicar ao branch local:

```bash
git fetch
```

Aplica modificações ao branch local:

```bash
git merge
```

Atalho: pull = fetch + merge:

```bash
git pull
```

Verifica o estado do repositório:

```bash
git status
```

Log de alterações:

```bash
git log --graph --oneline --decorate --all
```

## Branches

Cria uma branch a partir da branch atual (master):

```bash
git branch funcionalidade2
```

Vai para o novo branch:

```bash
git checkout funcionalidade2
```

Atalho: branch + checkout:

```bash
git checkout -b funcionalidade2
```

Lista as branchs do repositório local e verifica qual delas está em uso:

```bash
git branch
```

Envia a branch para o repositório remoto:

```bash
git push origin funcionalidade2
```

Remove uma branch no repositório remoto:

```bash
git push origin --delete NOME_DA_BRANCH
```

Remove uma branch no repositório local:

```bash
git branch -d NOME_DA_BRANCH
```

## Tags

Cria uma tag no repositório local:

```bash
git tag 1.0.0
```

Lista as tags existentes:

```bash
git tag
```

Envia uma tag para o repositório remoto:

```bash
git push origin 1.0.0
```

Remove tag no repositório remoto:

```bash
git push --delete origin TAG_NAME
```

Remove uma tag no repositório local:

```bash
git tag -d TAG_NAME
```

## Integrando branchs

A integração entre branchs pode ser feita por meio de rebase ou merge.

Integra um commit no master na branch funcionalidade2:

```bash
git checkout funcionalidade2
git rebase master
```

Como funciona o git rebase:

1 - Mudanças na branch da funcionalidade são temporariamente removidas;

2 - Os commits novos existentes na master são trazidos para a branch da funcionalidade;

3 - Mudanças na branch da funcionalidade são novamente aplicadas na branch funcionalidade2;

Merge do branch funcionalidade2 para o master:

```bash
git checkout master
git merge funcionalidade2
git push
```

## Diferenças entre git merge e git rebase

Ambos os comandos têm o mesmo propósito: integrar mudanças de uma branch em outra. Porém cada um faz essa tarefa de uma forma diferente.

Git Merge: O comando possui a vantagem de ser uma **operação não destrutiva**, ou seja, as branchs envolvidas não sofrem qualquer alteração que possa eventualmente trazer algum problema (como visto mais abaixo com o comando git rebase). Porém, o git merge adiciona um commit adicional de merge toda vez que um mesmo arquivo for alterando em ambas as branchs. Se a branch principal do projeto for muita ativa, o histórico de commits pode ficar um tanto "poluído".

Git Rebase: O comando incorpora os novos commits assim como o git merge, porém ao invés de utilizar um commit de merge, ele **rescreve o histórico** criando um novo commit para cada commit a ser incorporado. Essa reescrita do histórico de commits pode ser um tanto perigosa caso não sejam seguidas boas práticas de rebase como a seguinte:

Atenção: **você não deve fazer rebase na branch master**, já que isso reescreverá alguns commits da master no seu repositório local. Isso faz com que a sua branch master local se torne diferente da master do repositório remoto ou de outros membros da equipe. Os demais membros podem encontrar vários problemas ao tentar sincronizar seus repositórios nesses casos.

## Resolvendo conflitos

```bash
git config --global merge.tool meld
git config --global mergetool.meld.path "/usr/bin/meld"
git config --global mergetool.prompt false
git config -l --global
```

Executa diff com a ferramenta gráfica meld:

```bash
git difftool
```

Após entregar modificações no branch funcionalidade2:

```bash
git checkout master
git pull
git checkout funcionalidade2
git rebase master
```

Em caso de conflito, o git exibe mensagem informando que após a resolução do conflito você deve executar "git rebase --continue".

```bash
git mergetool
```

O meld exibe 3 vias com as versões do arquivo em questão:

- Via Central: apresenta o arquivo na situação que estava antes da alteração local e remota.
- Via da Esquerda: apresenta o arquivo na situação após a alteração existente no repositório remoto.
- Via da Direita: apresenta o arquivo na situação após a alteração existente no repositório local.

O resultado da resolução de conflitos deve ser feito substituindo o conteúdo da via central pois é esta via que será utilizada no próximo commit.

Após editado o conteúdo, clique no texto da aba central, clique no botão "Salvar" e feche o Meld.

```bash
git rebase --continue
```

Uma vez que o rebase foi concluído, é possível enviar as alterações para a branch master:

```bash
git checkout master
git merge funcionalidade2
```
