# Meu primeiro contato com git e github

## Compartilhando e Colaborando em projetos
### Comandos iniciais após criado o repositório

```
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:ialeonardomartini/git-github-projeto_inicial.git
git push -u origin main
```

### Clonando um repositorio

```
git clone {URL do repositorio do github}
```

### Commit

- >Deve ser realizado sempre que concluir uma tarefa especifica ou resolver algum bug

- >O controle de mudanças do Git é feito através dos commits

- >Todo commit conta com um id único e traz uma referência aos commits anteriores

```
git status #verificar quais arquivos foram modificados
git add . #adicionar mudanças
git commit -m "mensagem contexto de commits" #registrar as mudanças no repositorio
```

### Enviar commits para o github

```
git remote
git push origin main #subir as mudanças para o repositorio
```

### pull para baixar novos commits

```
git pull origin main #baixar as mudanças para o repositorio local
```

### Desfazendo um commit

```
git log
git revert {ID do commit}
```

### Resetar um commit

```
git reset --hard {ID do commit anterior como backup}
```

### amemd em um commit

- >Utilizado para alterar a mensagem do ultimo commit sem precisar criar um novo
- >Utilizado tambem para adicionar arquivos que foram esquecidos no commit anterior

```
git commit --amemd -m "nova mensagem"
```

## Dominando controle de versão de código

- >HEAD é o commit mais recent da branch atual

### comandos e parametros do log

```
git log --oneline #log resumido em uma linha
git log -p #exibir o log por completo como mudanças por exemplo
git log --graph #melhora o visual do log
git log --pretty
git log --format
git log --help (para pretty e format, que são as mesmas coisas)
```

### Vendo alterações de um commit especifico

```
git show #detalhes do ultimo commit HEAD
git show {hash do commit}
git show --help
```

### Comando diff

- >Este comando é fundamental para visualizar as diferenças entre o estado atual do código e o último commit. Ele mostra as alterações feitas nos arquivos que ainda não foram adicionados ao stage.

```
git diff #diferença entre as modificações atuais para a HEAD
git diff {hash commit mais antigo}..{hash commit mais novo} #diferença entre dois commits
```

### branch

- >Uma branch no Git é uma ramificação que permite desenvolver novas funcionalidades ou correções de forma independente, sem afetar o código principal

```
git branch #quais são os branchs existentes no trabalho
git branch {nome do novo branch} #cria uma nova branch
git switch {nome do branch} #altera para a branch selecionada
git switch -c 'nova-branch' #cria uma nova branch e ja torna local de trabalho
bit branch -d {nome da branch} #para excluir uma branch
```

### unindo as branchs

```
git merge {nome da branch}
```

this is only a test