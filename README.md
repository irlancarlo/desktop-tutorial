## Comandos Git
* Projeto criado para aprender comandos git no git bash. E alguns comandos linux.

Adicionar nome do usuário
```sh
$ git config --global user.name "Seu nome"
```

Adicionar email
```sh
$ git config --global user.email "seu email"
```

Para definir editor padrão do git
```sh
$ git config --global core.editor nome_variavel_ambimente_aponta_editor
$ git config --global core.editor caminho_completo_executavel
```
> Nota: aqui usei o visual code e criei a variavel de ambiente `code`

Para iniciar um repositorio git 
```sh
$ git init
```

Verificar se existe alguma mudança nos arquivos
```sh
$ git status
```

Adicionar arquivos 
```sh
$ git add *
$ git add .
```

Comitar os arquivos e armezenar no repositorio
```sh
$ git commit -m "Digitar seu comentario"
```

Adicionar e comitar os arquivos
```sh
$ git commit -am "seu comentario"
```

Para enviar os arquivos comitados para o repositorio
```sh
$ git push
```

Para baixar as alterações do repositorio
```sh
$ git pull
```

Baixar o projeto do repositorio sem fazer o merge
```sh
$ git fetch
```

Historico de commites
```sh
$ git log
```

Forma simplificada de exibir os commites
```sh
$ git log --oneline
```

Exibir o graph de commit
```sh
$ git log --graph
```

Exibir o graph de commit de todas as branch
```sh
$ git log --oneline --graph --all (forma simplificada)
$ git log --graph --all
```

Mostar a branch atual
```sh
$ git branch
```

Rastrear um commit antigo
```sh
$ git checkout code_hash_branch
```

Mostrar o que foi modificado
```sh
$ git diff
```

Discartar as mudanças do(s) arquivo(s)
```sh
$ git checkout nome_do_arquivo outro_arquivo (específico)
git checkout . (todos)
```

Para remover o conteudo já add no conteiner
```sh
$ git reset HEAD .
```

Para remover um commit (comando pode trazer inconsistência no repositorio)
```sh
$ git reset --hard aqui_code_do_hash
```

Para criar um novo branch
```sh
$ git checkout -b nome_branch
```

Para remover uma branch local
```sh
$ git branch -d nome_branch_local
```

Para remover uma branch remota
```sh
$ git push origin --delete nome_branch_remota
```

Para efetuar o merge de branch
1) entrar na branch que vai receber o código
```sh
$ git checkout nome_branch_1
```

2) para receber os arquivos
```sh
$ git merge nome_branch_2
```

Em caso de conflito. Abrir o editor configurado para git. Em `$ git config --global core.editor`
```sh
code .
code nome_arquivo
```
> Accept Current Change - Aceita as modificações do HEAD
> Accept Incoming Change - Aceita a segunda modificação
> Accept Both Changes - aceita as duas modificações
> Compare Changes - compara os arquivos
> Depois add os arquivo e comitar

Após resolver os conflitos: 
```sh
$ git add
$ git commit -m "comentário"
$ git push
```

Para abortar um merge de branches
```sh
$ git merge --abort
```

Verificar se existe um repositorio remoto
```sh
$ git remote
```

Para mais detalhes do repositorio remoto
```sh
$ git remote -v
```

Boas pratica de comentarios. Uma dica boa para facilitar a criação dos commits, é validá-los usando a seguinte frase: “Se aplicado, esse commit vai” (ou, no inglês, “If applied, this commit will”). Veja um exemplo abaixo:
```sh
$ git log --oneline -4 
d759236 Change config to upload 
ae6a172 Merge branch 'assync-spam-job' into 'master' 
ef10959 Disable worker for spam learn. 
4210b8c Merge branch 'sentry-error-spam' into 'master'
```

## Comandos linux

Criar arquivos. `$ touch arqui.txt outro.java`

Caso o bash travar o terminal clicar em `Q`.

Exibir arquivos ocultos. `$ ls -a`

Criar pasta. `$ mkdir nome_pasta`



## License

MIT

**Free Software, Hell Yeah!**
