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
git commit --amend -m "nova mensagem"
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
git push origin :{nome da branch} #para excluir a branch do github
```

### unindo as branchs

```
git merge {nome da branch}
```

### comando rebase

- >É utilizado para integrar as alterações de uma branch em outra de uma maneira que mantém um histórico linear, ao contrário do merge, que pode criar um histórico mais complexo com commits de merge.

```
git rebase main
```

### comando stash

- >Permite guardar alterações temporariamente sem criar um commit. Isso é útil quando o código não está em um estado funcional, e precisamos mudar de foco rapidamente.

```
git stash #armazena as modificações feitas
git stash pop #aplica a ultima modificação armazenadas (indice na frente do pop aplica com o indice da lista e remove da lista)
git stash list
git stash clear
git stash push -m "message content"
git stash apply {indice do stash list} #aplica a modificação armazenada desejada de acordo com o indice da lista
git stash drop # remove o item da stash
```

### comando restore

```
git restore
git restore --staged #staging area
```

### criando tags

- >As tags funcionam como checkpoints em um jogo, permitindo que possamos marcar um estado específico do nosso código que queremos salvar e, se necessário, retornar a ele no futuro.

```
git tag {nome_da_tag}
git tag {nome_da_tag} {ID_commit}
git push origin {nome_da_tag}
git push origin --tags
```

### criando annotated tags

```
git tag -a {nome_da_tag} -m "mensagem na tag"
git tag -v {nome_da_tag} #tras os informações da tag
```
