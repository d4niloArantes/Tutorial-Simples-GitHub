# Tutorial-Simples-GitHub
Neste tutorial nós vamos aprender como criar um repositório Git no computador, comandos para versionamento de projetos, 
a conectar sua conta do GitHub e fazer o upload de seus arquivos.

Para isso, já pressuponho que *esteja instalado o Git* em seu computador. [Ir ao site do Git](https://git-scm.com/)
+ Não se incomodem com a falta de acentuação

## REPOSITORIO GIT LOCAL

#### Para criar um repositorio Git Local
	$ git init 		[se ja estiver dentro da pasta] 
ou

	$ git init /home/repo   [se indicando caminho do novo repositorio]

#### Para adicionar um arquivo ao git
	$ git add nome-do-arquivo
Para adicionar todos os arquivos:

	$ git add .

#### Verifica os arquivos que estao preparados para o commit
	$ git status
	
#### Commit - Para gravar as alterações no repositorio
	$ git commit 				[para comitar todos arquivos adicionados]
	$ git commit -m "nome-do-arquivo"	[para comitar somente o arquivo solicitado]
Se receber uma mensangem *Please tell me who you are.*
Coloque seu email e nickname do GitHub:

	$ git config --global user.email "email@email.com"
	$ git config --global user.name "Nick Name"
Apos rodar o commit um editor de texto com uma mensagem para voce sera aberta.
Escreva algum comentario no inicio mesmo sobre o commit, salve o arquivo e saia do editor.

#### Para ver os commits realizados
	$ git log

## REPOSITORIOS REMOTOS
Para adicionar um repositorio remoto como o caso do GitHub voce deve ter criado um repositorio pelo site e adiciona-lo
ao Git com o comando:

	$ git remote add origin https://github.com/<Usuario>/<NomeDoRepositorioGitHub.git>
Comando para enviar os commits para o repositorio remoto:

	$ git push
Se receber uma mensagem: *When push.default is set to 'matching'...*
Isso acontece pq voce nao especificou em qual branch que sera enviada.
Por padrao o git tem a branch master. Para configura-la:

	$ git push -u origin master
