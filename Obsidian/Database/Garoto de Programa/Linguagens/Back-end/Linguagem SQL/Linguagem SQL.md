<mark style="background: #FF5582A6;">Para realizar a inserção, remoção, edição ou qualquer outra atividade com os dados que irão ou estão no banco de dados</mark>, é necessária uma interação por meio da Linguagem SQL (Linguagem de Consulta Estruturada). Ela que cria a ponte necessária entre o que precisa ser feito e o banco de dados efetivamente

Os **SGBDs** são softwares que tem como foco definir, manipular e acessar banco de dados, organizando seu funcionamento estrutural com objetivo de evitar inconsistências, desnormalização e redundâncias. Assim, temos conjuntos de dados (bancos de dados) sendo gerenciados por sistemas gerenciadores de bancos de dados (os SGBDs). Dentre vários SGBDs, podemos destacar: **MySQL**, **Access**, **PostgreSQL**, **Oracle**, etc.

Para implementar, então, a gestão sobre o banco de dados, é necessário a utilização do SQL ou de outra linguagem para banco de dados; no caso, o SQL é o mais difundido e, por meio dele, as transações no bando de dados podem ser realizadas

Os bancos de dados vão apresentar três representações de abstração no momento da sua modelagem (nível físico, nível lógico, e nível visão). Dentro desse contexto, no nível físico (nível mais baixo de representação), temos a descrição de armazenamento dos dados, temos a forma como os dados estão fisicamente armazenados.

No nível lógico, temos quais dados estão armazenados e seus relacionamentos, ou seja, quais relações existem entre os dados; logo, temos aqui, a representação da estrutura lógica dos dados.

Por fim, temos o nível visão, no qual é apresentada uma abstração dos dados na forma pela qual eles são vistos pelo usuário do sistema de gerenciador de banco de dados.

---
## [[Ramificações SQL]]
Para operar essas três estruturas, temos a linguagem SQL, que foi dividida em quatro ramificações:

- **DDL** (Data Definition Language)
	Essa linguagem é usada para definir e estruturar o banco de dados, criando e modificando.
	- `CREATE` - Cria tabelas no banco de dados.
	- `DROP` - Exclui tabelas ou outros objetos do banco.
	- `ALTER` - Adicionar colunas a uma tabela existente

- **DML** (Data Manipulation Language)
	Essa é usada para manipular os dados dentro do banco
	- `INSERT` - Inserir dados
	- `UPDATE` - Atualizar o dado
	- `DELETE` - Deletar o dado
	- `JOIN` - Combinar e manipular dados de duas ou mais tabelas.

- **DQL** (Data Query Language)
	Usado na consulta e recuperação de dados.
	- Comuns usados com **SELECT** 
		- `WHERE` - Usado para restringir os resultados da consulta
		- `ORDER BY` - Podemos classificar os resultados em ordem alfabética ou numérica.
		- `GROUP BY ` - Organizar dados idênticos em grupos
		- `HAVING` - Permite que você filtre quais grupos incluir e quais excluir.
	- Operadores de comparação: `=`, `<>`, `>`, `<`, `>=`, `<=`
    - Operadores lógicos: 
	    - `AND` - Combinar várias condições em um WHERE
	    - `OR` - Executa se qualquer condição for verdadeira
	    - `NOT`
    - Operadores de padrão: 
	    - `LIKE` - Compara valores semelhantes
	    - `IN`
	    - `BETWEEN` - Filtrar um certo intervalo de dados
	    - `IS NULL` - Indica valores desconhecidos ou nulos
    - Operadores de conjunto:
	    - `UNION` - Empilha um conjunto de dados de uma tabela em cima de outra
	    - `INTERSECT`
	    - `EXCEPT`

- **DCL** (Data Control Language)
	É usada para gerenciar permissões e controle de acesso ao banco de dados.
	- `GRANT` - Concede permissões a um usuário
	- `REVOKE` - Remove permissões concedidas.

- **Funções Agregadas**
	As consultas SQL não acessam apenas dados brutos, elas também podem executar cálculos nos dados brutos para responder a perguntas específicas sobre dados.
	- `COUNT( )` - conte o número de linhas
	- `SUM( )` - a soma dos valores em uma coluna
	- `MAX( )` - Maior valor
	- `MIN( )` - Menor valor
	- `AVG( )` -  A média dos valores em uma coluna
	- `ROUND( )` - Arredondar os valores na coluna

---
## Conjunto de tabelas
Para armazenar dados de forma eficiente, muitas vezes distribuímos informações relacionadas em várias tabelas.

Por exemplo, imagine que administramos uma empresa de revistas onde os usuários podem ter diferentes tipos de assinaturas para diferentes produtos. Assinaturas diferentes podem ter muitas propriedades diferentes. Cada cliente também teria muitas informações associadas.

Muitas dessas informações seriam repetidas. Se o mesmo cliente tiver várias assinaturas, o nome e o endereço desse cliente serão informados várias vezes. Se o mesmo tipo de assinatura for solicitado por vários clientes, o preço e a descrição da assinatura serão repetidos. Isso tornará nossa tabela grande e incontrolável.

Então, podemos dividir nossos dados em três tabelas:
1. Conteria apenas as informações necessárias para descrever o que foi pedido
	- ID do pedido
	- ID do cliente
	- ID da assinatura
	- Data de compra
---
2. Conteria as informações para descrever cada tipo de assinatura
	- ID da assinatura
	- Descrição
	- Preço por mês
	- Duração da assinatura
---
3. Conteria as informações de cada cliente
	- ID do cliente
	- Nome do cliente
	- Endereço
---
### [[Diagrama de Entidade e Relacionamento (DER)]]
Um DER é o desenho gráfico do Modelo Entidade Relacionamento que tem como resultado as ligações entre tabelas e seus relacionamentos de forma mais prática e visual, melhorando o fluxo de trabalho e a manutenção dos sistemas de banco de dados.