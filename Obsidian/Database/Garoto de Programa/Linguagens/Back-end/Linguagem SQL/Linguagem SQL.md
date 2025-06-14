Para realizar a inserção, remoção, edição ou qualquer outra atividade com os dados que irão ou estão no banco de dados, é necessária uma interação por meio da [[Linguagem SQL]] (Linguagem de Consulta Estruturada). Ela que cria a ponte necessária entre o que precisa ser feito e o banco de dados efetivamentente

Os SGBDs são softwares que tem como foco definir, manipular e acessar banco de dados, organizando seu funcionamento estrutural com objetivo de evitar inconsistências, desnormalização e redundâncias. Assim, temos conjuntos de dados (bancos de dados) sendo gerenciados por sistemas gerenciadores de bancos de dados (os SGBDs). Dentre vários SGBDs, podemos destacar: MySQL, Access, PostgreSQL, Oracle, etc.

Para implementar, então, a gestão sobre o banco de dados, é necessário a utilização do SQL ou de outra linguagem para banco de dados; no caso, o SQL é o mais difundido e, por meio dele, as transações no bando de dados podem ser realizadas

Os bancos de dados vão apresentar três representações de abstração no momento da sua modelagem (nível físico, nível lógico, e nível visão). Dentro desse contexto, no nível físico (nível mais baixo de representaçãpo), temos a descrição de armazenamento dos dados, temos a forma como os dados estão fisicamente armazenados.

No nível lógico, temos quais dados estão armazenados e seus relacionamentos, ou seja, quais relações existem entre os dados; logo, temos aqui, a representação da estrutura lógica dos dados.

Por fim, temos o nível visão, no qual é apresentada uma abstração dos dados na forma pela qual eles são vistos pelo usuário do sistema de gerenciador de banco de dados.

## [[Ramificações SQL]]
Para operar essas três estruturas, temos a linguagem SQL, que foi dividida em quatro ramificações:

- **DDL** (Data Definition Language)
	Essa linguagem é usada para definir e estruturar o banco de dados, criando e modificando.
	- `CREATE` - Cria tabelas no banco de dados.
	- `DROP` - Exclui tabelas ou outros objetos do banco.
	- `ALTER`

- **DML** (Data Manipulation Language)
	Essa é usada para manipular os dados dentro do banco
	- `INSERT` - Inserir dados
	- `SELECT` - Selecionar o dado
	- `UPDATE` - Atualizar o dado
	- `DELETE` - Deletar o dado

- **DTL** (Data Transaction Language)
	É usada para gerenciar transações no banco de dados.
	- `BEGIN` - Inicia uma transação.
	- `COMMIT` - Confirma as mudanças feitas em uma transação
	- `ROLLBACK` - Desfaz mudanças, retornando ao estado anterior

- **DDL** (Data Control Language)
	É usada para gerenciar permissões e controle de acesso ao banco de dados.
	- `GRANT` - Concede permissões a um usuário
	- `REVOKE` - Remove permissões concedidas.

---

### Diagrama de Entidade e Relacionamento (DER)
Um DER é o desenho gráfico do Modelo Entidade Relacionamento que tem comno resultado as ligações entre tabelas e seus relacionamentos de forma mais prática e visual, melhorarando o fluxo de trabalho e a manutenção dos sistemas de banco de dados.
#### Entidade
As entidades podem ser representadas por um retângulo. Uma entidade representa um objeto ou conceito do mundo real que possui uma existência independente e que pode ser identificado de forma única. Pode ser uma pessoa, lugar, evento ou qualquer coisa que você queira armazenar informações. **Exemplo**: Em um sistema de gerenciamento de biblioteca, entidades podem ser `Livro`, `Usuário`, `Empréstimo`.
#### Relacionamento
Para representar os relacionamentos no DER, a figura utilizada é o losangulo. Um relacionamento descreve como duas ou mais entidades estão associadas entre si. Ele define a interação entre as entidades. **Exemplo**: No mesmo sistema de biblioteca, um relacionamento pode ser `Empréstimo`, que conecta as entidades `Livro` e `Usuário`.
#### Cardinalidade
A cardinalidade especifica o número de instâncias de uma entidade que podem estar associadas a uma instância de outra entidade. Ela define a natureza do relacionamento em termos de quantidade.

- Relacionamento um para um (1 1);
	- Exemplo: Cada `Usuário` tem um `Cartão de Biblioteca`.

- Relacionamento um para n (1 n);
	- Um `Usuário` pode emprestar vários `Livros`

- Relacionamento n para n (n n);
	- Exemplo: Vários `Usuários` podem emprestar vários `Livros`.

#### Exemplo

![[Pasted image 20241118172605.png]]