# Comandos GitHub

Adicionar nome usuário
$ git config --global user.name "Seu nome"

Adicionar email
$ git config --global user.email "seu email"

Para definir editor padrão do git
$ git config --global core.editor nome_variavel_ambimente_aponta_editor

para iniciar um repositorio git 
$ git init

criar arquivos
$touch arqui.txt outro.java

Verifica os status dos arquivos no git
$ git status

Add arquivos 
$ git add *
ou
$git add .

Comitar os arquivos e armezenar no repositorio
$ git commit -m "Digitar seu comentario"

Historico de commites
$ git log

Forma simplificada de exibir os commites
$ git log --oneline

Exibir o graph de commit
$ git log --graph

Adicionar e comitar os arquivos
$ git commit -am "seu comentario"

Mostra em que ramo (branch) está
$ git branch

Rastrear um commit antigo
$ git checkout aqui_code_do_hash

Para voltar para ultima versão 
$ git checkout master

Mostrar o que foi modificado
$ git diff

Discartar as mudanças dos arquivos
$ git checkout nome_do_arquivo

Para remover o conteudo já add do conteiner
$ git reset HEAD

Para remover um commit (comando pode trazer inconsistência no repositorio)
$ git reset --hard aqui_code_do_hash

Para criar um novo branch
$ git checkout -b nome_branch

Para add todos os arquivos
$ git add *

Exibir o graph de commit de todas as branch
$ git log --oneline --graph --all (forma simplificada)
OU
$ git log --graph --all

O bash travar o terminal clicar em Q

Para efetuar o merge de branch
1) entrar na branch que vai receber o código
$ git checkout nome_branch_1
2) para enviar os arquivos
$ git merge nome_branch_2

Em caso de conflito
Accept Current Change - Aceita as modificações do HEAD
Accept Incoming Change - Aceita a segunda modificação
Accept Both Changes - aceita as duas modificações
Compare Changes - compara os arquivos
Depois add os arquivo e comitar

Para abortar um merge de branchs
$ git merge --abort

Exibir arquivos ocultos
$ ls -a

Criar pasta
$ mkdir nome_pasta

Para enviar os arquivos comitados para o repositorio
$ git push

Verificar se existe um repositorio remoto
$ git remote

Para mais detalhes do repositorio remoto
$ git remote -v

Para baixar as alterações do repositorio
$ git pull

Boas pratica de de comentarios
Uma dica boa para facilitar a criação dos commits, 
é validá-los usando a seguinte frase: 
“Se aplicado, esse commit vai” 
(ou, no inglês, “If applied, this commit will”). 
Veja um exemplo abaixo:

$ git log --oneline -4 

d759236 Change config to upload 

ae6a172 Merge branch 'assync-spam-job' into 'master' 

ef10959 Disable worker for spam learn. 

4210b8c Merge branch 'sentry-error-spam' into 'master'

Baixar o projeto do repositorio sem fazer o merge 
$ git fetch

Removendo branch
// delete branch locally
$ git branch -d localBranchName
// delete branch remotely
$ git push origin --delete remoteBranchName