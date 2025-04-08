# Meu primeiro contato com git e github

## Comandos iniciais após criado o repositório

```
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:ialeonardomartini/git-github-projeto_inicial.git
git push -u origin main
```
## Clonando um repositorio

```
git clone URL(do repositorio do github)
```

## Commit

- Deve ser realizado sempre que concluir uma tarefa especifica ou resolver algum bug
- O controle de mudanças do Git é feito através dos commits
- Todo commit conta com um id único e traz uma referência aos commits anteriores

```
git status
git add .
git commit -m "mensagem contexto de commits"
```

## Enviar commits para o github

```
git remote
push origin main
```