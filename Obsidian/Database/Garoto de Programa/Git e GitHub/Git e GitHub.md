## Git
Criado por Linus Torvalds em 2005, Git é um sistema distribuído de controle de versão que permite que desenvolvedores armazenem, modifiquem e gerenciem código de maneira organizada. Ele opera localmente, garantindo independência no desenvolvimento, mas também pode ser sincronizado com repositórios remotos para colaboração.

### Primeiros passos
#### Terminal
Existem dois principais terminais para escrever em GIT:
- <mark style="background: #BBFABBA6;">Git Bash</mark>
	- Emula o terminal Bash, comum em sistemas Linux e macOS.
	- Ideal para rodar scripts `.sh` e comandos encadeados.
	- Experiência mais próxima do Git original: Como o Git foi criado para Unix, o Bash oferece uma experiência mais natural e completa.

- <mark style="background: #BBFABBA6;">CMD</mark>
	- Ambiente nativo do Windows
	- Você pode usar os comandos Git normalmente
	- Não tem suporte nativo a comandos Unix, o que pode limitar algumas automações ou scripts.

Se você está acostumado com o Windows e só quer rodar comandos Git simples, o CMD dá conta. Mas se você quer mais poder, flexibilidade e comandos extras, o Git Bash é o queridinho da galera dev.

#### Configuração
Antes de utilizar o Git, é necessário configurar algumas informações por motivos relacionados à identidade , rastreabilidade e padronização nos projetos.
- <mark style="background: #BBFABBA6;">Nome do usuário</mark>
	O Git associa cada commit a uma pessoa. Quando você faz um , o Git registra quem fez aquela alteração usando o nome que você configurou.
- <mark style="background: #BBFABBA6;">E-mail</mark>
	Assim como o nome, o e-mail também é usado para identificar os commits. É especialmente importante quando você usa plataformas como GitHub, GitLab ou Bitbucket, pois elas associam os commits ao seu perfil com base nesse e-mail.
- <mark style="background: #BBFABBA6;">Ramificação padrão</mark>
	Essa configuração define o nome da **branch** (um dos capítulos). Antes era comum usar `master`, mas `main` se tornou o padrão atual para nomear a branch **principal** de um repositório
```ad-bug
title: Code
collapse: closed
```bash
git config --global user.name "Seu Nome"
git config --global user.email seu@email.com
git config --global init.defaultBranch main
```



### Inicializando o GIT
1. Primeiramente, precisamos indicar um diretório, indicando o caminho dos arquivos
	- **Dica**: Para indicar o diretório de forma mais rápida, arraste a pasta em que estão os arquivos para o terminal
	
	- Exemplo:
		1. **Mudando de diretório:**
			`cd` C:\Users\ricar\Documents
			
		2. **Traz uma relação de todos os arquivos do diretório:**
			dir

2. Dessa forma podemos dar início ao GIT com o comando `git init`

3. Inicialmente os arquivos estão em um estado que chamamos de **[^1]Untracked**

4. Por isso precisamos colocar os arquivos no modo **Tracked** com o comando `add`
	- **Exemplo**
		`git add` arquivo
		
	- Contudo, podemos fazer isso tanto com um único arquivo quanto com todos eles

### Estados de um arquivo
Com tudo isso, concluímos que um arquivo dentro do GIT pode estar em 3 possíveis status:

- <mark style="background: #FFB86CA6;">Working</mark>
	Aqui estão os arquivos que você está editando no momento. Se você altera um arquivo, ele fica diferente da última versão registrada no Git, mas ainda não está pronto para ser salvo definitivamente.

- <mark style="background: #FFB86CA6;">Staging</mark>
	Quando você usa `git add`, o arquivo entra na área de preparação (_staging_). Isso significa que ele está pronto para ser incluído no próximo commit, mas ainda não foi salvo no histórico do Git.

- <mark style="background: #FFB86CA6;">Commit</mark>
	Quando você executa `git commit -m "mensagem"`, o arquivo é salvo no histórico do repositório. Agora ele faz parte da versão oficial do projeto e pode ser compartilhado com outros desenvolvedores.

**Como se fosse revisar antes de entregar**: você escreve uma redação (working), escolhe os parágrafos bons (staging), e então entrega oficialmente (commit).

**Como fazer um prato com vários ingredientes**: você separa os ingredientes (staging), depois monta o prato (commit). Isso evita jogar tudo na panela de uma vez e perder o controle do sabor.

**Situação mostrando o porque da sequência:**
Imagine que você fez 3 tipos de mudanças:

- Corrigiu um bug.    
- Adicionou um novo recurso.
- Reformulou comentários e indentação.

Se você fizesse um único commit com tudo isso junto, ele ficaria confuso: difícil de revisar, difícil de reverter uma parte específica, e sem um histórico claro. Com a staging area, você pode:

```bash
git add arquivo_bugfix.py 
git commit -m "Corrige bug X"  

git add novo_recurso.py 
git commit -m "Adiciona recurso Y"  

git add script_comentarios.py 
git commit -m "Melhora legibilidade do código"`
```

### Git Reset
Este comando tem três modos principais: **soft**, **mixed** e **hard**, cada um com um impacto diferente no histórico do repositório, na área de staging e no diretório de trabalho.
`git reset` modo e versão 

- <mark style="background: #FFB86CA6;">Soft</mark>
	**Move o HEAD** para um commit anterior, mas mantém as mudanças na área de staging.
	**Preserva** os arquivos modificados e prontos para commit.
	**Útil quando** você quer refazer um commit sem perder as alterações.

- <mark style="background: #FFB86CA6;">Mixed (padrão)</mark>
	**Move o HEAD** para um commit anterior e **limpa a área de staging**.
	**Mantém** as mudanças no diretório de trabalho, mas você precisa adicionar ao staging dnv
	**Útil quando** você quer reorganizar as mudanças antes de um novo commit.

- <mark style="background: #FFB86CA6;">Hard</mark>
	**Move o HEAD** para um commit anterior e **descarta todas as mudanças** no diretório de trabalho e na área de staging.
	**Perigoso**, pois **não há recuperação** das alterações descartadas.
	**Útil quando** você quer voltar completamente a um estado anterior sem manter modificações.

### Comandos
`clear`
`cd` diretório
`dir`
`init`
`git status`
`git add` arquivo
`git rm --cached` arquivo
`git commit` -m "**mensagem**"

`git diff`
`git rm` arquivo
`git restore --staged` arquivo
	caso for removido por um comando no git ficando então no estado de **deleted**
`git restore` arquivo
`git log`
	Pode ser utilizado o `git log --oneline` para trazer um histórico mais simplificado
	Assim como também temos um histórico mais detalhado `git log -p`

### Branches
No Git, as _branches_ (ramificações) <mark style="background: #FFF3A3A6;">são como linhas de desenvolvimento paralelas</mark> que permitem trabalhar em diferentes versões de um projeto sem afetar o código principal. Elas são essenciais para organizar e gerenciar alterações de código de forma eficiente. Aqui estão algumas operações comuns com branches:

- Para criar uma nova branche
	- `git branch` **nome-da-branch**
	- Ou se quiser criar e já quiser mudar para essa branch:
		`git checkout -b` **nome-da-branch**
- 
- Mudar para outra branch
	- `git checkout` **nome-da-branch**
	- Em versões mais recentes do GIT:
		`git switch` **nome-da-branch**
- 
- Para ver todas as branches no repositório:
	- `git branch`
	- Para listar também branches remotas:
		`git branch -r`
- 
- Caso precise renomear uma branch:
	- `git branch -m` **novo-nome**
- 
- Para poder excluir uma branch:
	- Se a branch não foi mergeada e deseja deletá-la (padrão):
		`git branch -d` **nome-da-branch**
	- Se quiser forçar uma exclusão:
		`git branch -D` **nome-da-branch**
- 
- Para fazer a fusão de branches (o famoso Merge)
	- Para fundir ao código principal (geralmente main)
		1. `git checkout main`
		2. `git merge` **nome-da-branch**
	- Outra forma, mantendo o histórico de commits mais limpo
		1. `git checkout` **nome-da-branch**
		2. `git rebase main`

#### Git Alias
No entanto, há como fazer <mark style="background: #BBFABBA6;">atalhos personalizados</mark> para cada comando
```shell
#Para criar o atalho
git config alias.nome "comando original" 

#Exemplo
git config alias.log1 "log --oneline"

#Normalmente fica salvo na sua máquina, mas pode também ser salvo para todos do projeto
git config --global alias.log1 "log --oneline"
```

### Observações / Dicas
- Alterações no nome do arquivo
	O Git não entende as alterações dos nomes de seus arquivos. Para ele, um arquivo sumiu e apareceu outro totalmente desconhecido. Por isso é utilizado o comando `git mv`

- Alteração da mensagem do commit
	Para fazer essa alteração precisamos criar um novo commit, mas especificando o que será alterado, no caso, a mensagem do commit
	`git commit -m` "mensagem" `--amend`

- O que é **HEAD**?
	HEAD é um **ponteiro especial** que indica **qual é o commit atual** (ou seja, onde você está no histórico do projeto). Em geral, ele aponta para o último commit da branch ativa.
## GitHub
GitHub é uma plataforma baseada na web que expande as funcionalidades do Git, permitindo que desenvolvedores hospedem, compartilhem e gerenciem código de maneira centralizada. Ele facilita a colaboração entre equipes por meio de **pull requests**, onde membros podem revisar e discutir mudanças antes de implementá-las.

### Criando o seu Repository
Para que se tenha uma comunicação entre o Git e o GitHub (o famoso push) é necessário indicar alguns comandos no terminal indicados pelo site ao criar um novo repositório do GitHub
![[Pasted image 20250613191941.png]]
```ad-attention
title: Segurança
collapse: closed
Após esse processo, o próprio terminal vai solicitar que você se identifique com seu nome de usuário e senha, que no caso é o Token gerado em... 

Configurações`>`Configurações do desenvolvedor`>`Tokens de acesso pessoal`>`Fichas`>`Gerar

```

### Relacionamento
- Push de outras Branches
	`git push --all`

- O interessante é que você pode fazer alterações nos arquivos e realizar um na própria main commit ou até mesmo criar outra branch pelo próprio GitHub... o famoso **Pull**
	`git pull`

[^1]:  <mark style="background: #FFB8EBA6;">Arquivo no modo Untracked</mark>:  Modo comum quando se inicia o GIT, em que se houver uma alteração nestes arquivos os dados ainda não serão salvos, pois não foi feito um **snapshot** (cópia exata para versionamento)
