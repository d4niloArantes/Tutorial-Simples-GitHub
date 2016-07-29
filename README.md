# Tutorial-Simples-GitHub
Neste tutorial nós vamos aprender como criar um repositório Git no computador, comandos para versionamento de projetos, 
a conectar sua conta do GitHub e fazer o upload de seus arquivos.

Para isso, já pressuponho que *esteja instalado o Git* em seu computador. [Ir ao site do Git](https://git-scm.com/)

## REPOSITÓRIO GIT LOCAL

#### Para criar um repositório Git Local
	$ git init 		[se já estiver dentro da pasta] 
ou

	$ git init /home/repo   [se indicando caminho do novo repositório]

#### Para adicionar um arquivo ao git
	$ git add nome-do-arquivo
Para adicionar todos os arquivos:

	$ git add .

#### Verifica os arquivos que estão preparados para o commit
	$ git status
	
#### Commit - Para gravar as alterações no repositório
	$ git commit 				[para comitar todos arquivos adicionados]
	$ git commit -m "nome-do-arquivo"	[para comitar somente o arquivo solicitado]
Se receber uma mensangem *Please tell me who you are.*, basta coloque seu email e nickname do GitHub:

	$ git config --global user.email "email@email.com"
	$ git config --global user.name "Nick Name"
Após rodar o commit um editor de texto com uma mensagem para você será aberta.
Escreva algum comentário no início mesmo do arquivo sobre o commit, salve e saia do editor.

#### Para ver os commits realizados
	$ git log

## REPOSITÓRIOS REMOTOS
Para adicionar um repositório remoto como o caso do GitHub você deve criar um pelo site e adicioná-lo ao Git com o comando:

	$ git remote add origin https://github.com/<Usuario>/<NomeDoRepositorioGitHub.git>
Comando para enviar os commits para o repositório remoto:

	$ git push
Se receber uma mensagem: *When push.default is set to 'matching'...*, acontece porque você não especificou em qual branch que será enviada.
Por padrão o git tem a branch master. Para configurá-la:

	$ git push -u origin master
