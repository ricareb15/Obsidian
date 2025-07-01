## Linguagem DDL
Temos, então, que a DDL compõe o SQL e é utilizada na modelagem e no desenvolvimento de banco de dados para a definição de estruturas de dados como colunas, tabelas, linhas e índices.

- `CREAT TABLE` - Usada para definir uma nova tabela usando a seguinte instrução:
	- Exemplo:
		`CREAT TABLE` **Tabela** (
			id-aluno CHAR(20)
			nome CHAR(20)
			login CHAR(20)
			idade INTEGER
			media REAL) 
---
- `DROP TABLE` - Remove a tabela do banco de dados
	- Incluindo todos os dados e a definição da tabela. **Cuidado**, ao usar esse comando, **tudo será apagado permanentemente** e só poderá ser recuperado caso haja um backup.
	- Exemplo
		`DROP TABLE` **Tabela**;
---
- `ALTER TABLE` - Responsável pela edição da estrutura de uma tabela 
	- É tipo o “faz-tudo” quando você precisa <mark style="background: #ABF7F7A6;">modificar a estrutura de uma tabela</mark> depois que ela já foi criada. Ele é muito útil porque permite ajustar a tabela conforme novas necessidades vão surgindo, sem precisar recriá-la do zero.
	- Adicionar coluna
		`ALTER TABLE` nome_da_tabela
		`ADD` nova_coluna `TEXT`;
	- Remover coluna
		`ALTER TABLE` nome_da_tabela
		`DROP COLUMN` nova_coluna;
---
- `TRUNCATE` - Deleta os dados de uma tabela
	- É usado para <mark style="background: #FFB86CA6;">remover rapidamente todos os dados de uma tabela</mark>, mas sem apagar a estrutura da tabela. Ele é tipo um "limpa tudo" sem dó, mas mais eficiente do que o `DELETE` quando se trata de grandes volumes.
	- Exemplo:
		`TRUNCATE TABLE` tabela;
	- Cuidados:
		Não ativa gatilhos (`TRIGGER`) em alguns bancos.
		Não pode ser revertido com `ROLLBACK` em muitos sistemas.
		Muito mais rápido que `DELETE`, mas menos flexível.
---
- `RENAME` - Renomear objetos no banco
	- Como tabelas, colunas ou índices. O uso exato varia um pouco conforme o banco.
	- Exemplo:
		`ALTER TABLE` antigo_nome 
		`RENAME TO` novo_nome;

## Linguagem DML
A linguagem DML nasce para respaldar o contexto de manipulação de dados em bancos de dados, principalmente em sistemas de informação que fazem consulta em bancos de dados relacionais por meio de SGBDs. As principais funções são:

- `INSERT` Faz a inserção de tuplas (linhas) na tabela
	- Exemplo:
		`INSERT`
		`INTO` (id-aluno, nome, login, idade, media) 
		`VALUES` (53688, "Smith", "smith@ee", 18, 3,2)
	- Repare que os valores seguem respectivamente a ordem das colunas indicadas.
--- 
- `SELECT` - Para realizar consultas em um banco de dados SQL
	- Exemplo - Para consultar colunas específicas
		`SELECT` **coluna1**, **coluna2**
		`FROM` **tabela**;
	
	- Exemplo2 - Para consultar todas as colunas
		`SELECT` * `FROM` **tabela**;
---
- `DELETE` - Podemos excluir tuplas usando este comando
	- Exemplo
		`DELETE`
		`FROM` **tabela**
		`WHERE` A.nome = "Smith"
--- 
- `UPTADE` - Pode ser utilizado para alterar os valores da tabela
	- Exemplo
		`UPTADE` **tabela**
		`SET` **tabela**.idade = **tabela**.idade + 1
		`WHERE` **tabela**.id-aluno = 53688
	
	- Exemplo2 - Também podemos apaga-los
		`UPDATE` **tabela**
		`SET` coluna = `NULL`;
		`WHERE` id = 2;
---
#### `JOIN`
Traduzindo do inglês o verbo <mark style="background: #FFF3A3A6;">juntar</mark>, é considerado parte do uso da **DML** mesmo que tecnicamente não seja um comando isolado como `SELECT` ou `UPDATE`. Usado para <mark style="background: #FFF3A3A6;">combinar dados de duas ou mais tabelas</mark> com base em uma relação entre elas — geralmente através de uma coluna comum, como uma chave primária e uma chave estrangeira.

Muito recorrente em casos em que há uma tabela sobre os dados do usuário, e também outra tabela que fala sobre os serviços, destacando o usuário que a está contratando. Certamente é usada uma **ID** em ambos os casos. Então se a ID trata da mesma coisa em ambos os casos, elas são iguais, e é pra isso que serve o `JOIN`

Exemplo de aplicação:
```SQL
SELECT *
FROM nome
JOIN serviço
  ON nome.usuario_id = serviço.contratante_id;
```

##### `LEFT JOIN`
O interessante é que esse tipo de junção só é feito se as condições (de `ON`) forem verdadeiras. Se acontecer da tabela de usuários estar desatualizada ou o mesmo não ter nenhum serviço contratado a linha não será contabilizada.
```ad-important
title: Ilustração
collapse: closed

![[SQL.gif]]

```

Por isso o SQL nos permite burlar isso por meio de um comando chamado `LEFT JOIN` em que podemos combinar duas tabelas e manter as linhas que não "corresponderam".
```ad-important
title: Ilustração
collapse: closed

![[left-join.gif]]

A primeira e a última linhas têm valores correspondentes de `c2`. As linhas do meio não correspondem. O resultado final manterá todas as linhas da primeira tabela, mas omitirá a linha não correspondente da segunda tabela.

![[Captura de tela 2025-06-19 001929.png]]
Supondo que no esquerdo seriam pessoas que são de São Paulo
E no direito pessoas que são de Guarulhos
As que não são de Guarulhos (0) não deixam de ser de São Paulo
Se não usassemos essa nova função elas não apareceriam
```

## DQL (Data Query Language)
É um subconjunto de SQL focado na recuperação de dados de um banco de dados. Especificamente, abrange a `SELECT` instrução, que é usada para consultar e extrair informações armazenadas em tabelas de banco de dados. Embora frequentemente agrupada com comandos DML (Linguagem de Manipulação de Dados), a DQL se distingue por seu propósito de ler dados em vez de alterá-los.

### Usados com `SELECT`
- `WHERE` -  Usado para restringir os resultados da consulta
	- O interessante é que você pode fazer essa restrição usando operadores de comparação 
	- Exemplo:
		`SELECT` * `FROM` **tabela**
		`WHERE` **coluna** `>` **8**
---
- `ORDER BY` - Podemos classificar os resultados em ordem alfabética ou numérica.
	- Ordem alfabética
		`SELECT` * `FROM` **tabela**
		`ORDER BY` **coluna**;
	
	- Ordem numérica
		- Crescente
			`SELECT` * `FROM` **tabela**
			`WHERE` **coluna** `>` **8**
			`ORDER BY` **coluna** `DESC`;
		
		- Decrescente
			`SELECT` * `FROM` **tabela**
			`WHERE` **coluna** `>` **8**
			`ORDER BY` **coluna** `ASC`;
---
- `AS` - Usada para dar um _alias_ (apelido) a uma coluna ou tabela.
	- O nome pode ser o que você quiser... Dês de que esteja em aspas simples ( **' '** )
	- As colunas não são renomeadas na tabela. Elas aparecem apenas no resultado.
	- Exemplo: 
		`SELECT` **coluna** `AS` **'novo_nome'** 
		`FROM` **tabela**
---
- `DISTINCT` - Ele filtra todos os valores duplicados na(s) coluna(s) especificada(s).
	- Exemplo:
		`SELECT DISTINCT` **coluna**
		`FROM` **tabela**;
---
- `LIMITE` - Permite especificar o número máximo de linhas que o conjunto de resultados terá.
	- Exemplo
		`SELECT` * `FROM` **tabela**
		`LIMIT` **10**;
---
- `CASE` - Nos permite criar diferentes saídas. É a maneira do SQL lidar com a lógica `if-then`
	- Cada `WHEN`testa uma condição e o `THEN` nos dá a string se a condição for verdadeira.
	- Caso precise o `ELSE` nos dá a string se _todas_ as condições acima forem falsas.
	- A `CASE` declaração deve terminar com `END`.
	
	- Exemplo
		- Se a classificação for acima de 8, então é Fantástico.
		- Se a classificação for acima de 6, então é Mal Recebido.
		- Caso contrário, evite a todo custo
		
		- `SELECT` **coluna**,
			- `CASE`
				`WHEN` **coluna(nota)** > 8 `THEN` **'Fantastic'**
				`WHEN` **coluna(nota)** > 6 `THEN` **'Poorly Received'**
				`ELSE` 
			- `END AS` **'novo_nome'**
		- `FROM` **tabela**;
#### `GROUP BY`
É uma cláusula que se atribui ao `SELECT` para <mark style="background: #ABF7F7A6;">organizar dados idênticos em grupos</mark>.
Por exemplo, podemos querer saber a média de avaliações do IMDb para todos os filmes a cada ano. Podemos calcular cada número por meio de uma série de consultas com diferentes `WHERE`.
```ad-todo
title: Exemplo
collapse: closed


```SQL
SELECT AVG(imdb_rating)
FROM movies
WHERE year = 1999;

SELECT AVG(imdb_rating)
FROM movies
WHERE year = 2000;

SELECT AVG(imdb_rating)
FROM movies
WHERE year = 2001;
```

Felizmente, há uma maneira melhor! Nós podemos usar:
```ad-todo
title: Exemplo
collapse: closed

```SQL
SELECT year,
AVG(imdb_rating)
FROM movies
GROUP BY year
ORDER BY year;
```

Projeto Code Cademy
```ad-todo
title: Exemplo
collapse: closed
```SQL
SELECT price, COUNT(*) 
FROM fake_apps
GROUP BY price;
```
```ad-example
title: Saída
collapse: closed
![[Pasted image 20250618171026.png]]

```

O interessante é que o `GROUP BY` nos permite referenciar as colunas através de números.
- `1`a primeira coluna é selecionada
- `2`a segunda coluna é selecionada
- `3`a terceira coluna é selecionada
- Exemplo:
	`SELECT ROUND(`**nota**`)`,
	   `COUNT(`**nome**`)`
	`FROM` **provas**
	`GROUP BY` **1** (nota)
	`ORDER BY` **1** (nota);
---
#### `HAVING`
Além de poder agrupar dados usando `GROUP BY`, o SQL também permite que você filtre quais grupos incluir e quais excluir.

Por exemplo, imagine que queremos ver quantos filmes de diferentes gêneros foram produzidos a cada ano, mas só nos importamos com anos e gêneros com pelo menos 10 filmes.

Não podemos usar `WHERE` aqui porque <mark style="background: #ABF7F7A6;">não queremos filtrar as linhas, queremos filtrar grupos</mark>.
É aqui que `HAVING` entra. Ele, inclusive, é muito semelhante a `WHERE`. Na verdade, todos os tipos de `WHERE` que você aprendeu até agora podem ser usados ​​com `HAVING`.

Dessa forma... Quando queremos limitar os resultados de uma consulta com base nos valores das linhas individuais, usamos `WHERE`. Quando queremos limitar os resultados de uma consulta com base em uma propriedade agregada, usamos `HAVING`.

```ad-info
title: Exemplo
collapse: closed
Supondo que você queira saber qual material em estoque tem mais do que três unidades...

```SQL
SELECT produtos, COUNT(*)
FROM mercado
GROUP BY produtos
HAVING COUNT(*) > 3;
```
### Operadores de comparação
Usados para comparar valores e retornar um resultado booleano `True` ou `False`

| Operador | Descrição      | Exemplo |
| -------- | -------------- | ------- |
| =        | Igual a        | A = B   |
| <>       | Diferente de   | A <> B  |
| !=       | Diferente de   | A != B  |
| <        | Menor que      | A < B   |
| >        | Maior que      | A > B   |
| <=       | Menor ou igual | A <= B  |
| >=       | Menor ou igual | A >= B  |
### Operadores lógicos
- `AND` - Muito útil para combinar várias condições em um WHERE
	- Exemplo
		`SELECT` * `FROM` **tabela**
		`WHERE` **coluna** `BETWEEN` **1990** `AND` **1999**
		`AND` **coluna** = **'texto'**;
---
- `OR` - Ocorre a filtração se qualquer condição for verdadeira
	- Exemplo:
		`SELECT` * `FROM` **tabela**
		`WHERE` **coluna** > **2014**
		`OR` **coluna** = **'texto'**;
---
### Operadores de padrão
- `LIKE` - Pode ser um operador útil quando você deseja comparar valores semelhantes.
	- Operador especial usado com `WHERE` para procurar um padrão específico em uma coluna.
	- Exemplo
		A tabela contém dois filmes com títulos semelhantes, 'Se7en' e 'Seven'.Como poderíamos selecionar todos os filmes que começam com "Se" e terminam com "en" e têm exatamente um personagem no meio?
		
		`SELECT` * `FROM` **tabela**
		`WHERE` **coluna** `LIKE` **'Se_en'**;
	
	- O sinal de porcentagem `%` é outro caractere curinga que pode ser usado com `LIKE`
		- `'A%'`- Corresponde a todos os filmes cujos nomes começam com a letra '**A**'
		- `'%a'`- Corresponde a todos os filmes que terminam com '**a**'
		- `'%man%'` - Corresponde a todos os filmes que tenha essa palavra em seu nome
			Não diferencia maiúsculas de minúsculas. "Batman" e "Homem de Aço" aparecerão no resultado da consulta acima.
		- Exemplo:
			`SELECT` * `FROM` **tabela**
			`WHERE` **coluna** `LIKE` **'A%'**;
---
- `BETWEEN` - Filtrar um conjunto de dados entre um intervalo de dados determinados
	- Exemplo:
		Esta instrução filtra o conjunto de resultados para apenas filmes do ano de 1990 até 1999
		`SELECT` * `FROM` **tabela** 
		`WHERE` `BETWEEN` **1990** `AND` **1999**;
---
- `NULL` - Indica valores desconhecidos ou nulos
	- Não é possível testar `NULL`valores com operadores de comparação, como `=` e `!=`.Em vez disso, teremos que usar estes operadores: `IS NULL` e `IS NOT NULL`
	- Exemplo:
		`SELECT` **coluna** `FROM` **tabela** 
		`WHERE` **coluna** `IS NOT NULL`;
---
### Operadores de conjunto
- `UNION` - Com ele podem empilhar um conjunto de dados de uma tabela em cima de outra
	- Explicação:
		- Suponha que temos duas tabelas elas têm as mesmas colunas:
			![[Captura de tela 2025-06-20 161009.png]]
			
		- Se combinarmos estes dois com `UNION`
			`SELECT` *
			`FROM` table1
			`UNION`
			`SELECT` *
			`FROM` table2;
			
		- O resultado seria:
			![[Pasted image 20250620161305.png]]
	- Regras:
		- As tabelas devem ter o mesmo número de colunas.
		- As colunas devem ter os mesmos tipos de dados na mesma ordem da primeira tabela.
---
#### `WITH` 
Usado para criar uma **CTE (Common Table Expression)** Ele serve para <mark style="background: #ABF7F7A6;">tornar consultas complexas mais legíveis e organizadas</mark>, especialmente quando você precisa reutilizar subconsultas ou trabalhar com hierarquias.
##### O que é uma CTE?
É como uma <mark style="background: #ABF7F7A6;">tabela temporária nomeada</mark>, definida no início da consulta, que só existe durante a execução daquela instrução. Ela pode ser referenciada como se fosse uma tabela real, mas sem a necessidade de criá-la no banco.
##### Explicação
Vamos analisar o seguinte código:
```sql
WITH cte_Quantidade AS (
SELECT SUM(Quantidade) as Total
FROM InformacoesPedido
GROUP BY ID_Produto)

SELECT AVG(Total) AS quantidade_media_produto
FROM cte_Quantidade;
```

```ad-abstract
title: 🍰 Etapa 1: Criando a “massa” com a CTE
collapse: closed


```sql
WITH cte_Quantidade AS (
    SELECT SUM(Quantidade) as Total
    FROM InformacoesPedido
    GROUP BY ID_Produto
)
```




- `INTERSECT`
- `EXCEPT`


## Palavras chave
No mundo do SQL (Structured Query Language), as _palavras-chave_ são os blocos de construção das instruções que você usa para consultar, modificar e manipular bancos de dados. Você já viu algumas delas, mas vamos explorar outras palavras-chave e cláusulas que, embora sejam menos “famosas”, são super úteis quando você quer escrever consultas SQL mais refinadas.
## Funções Agregadas
As consultas SQL não acessam apenas dados brutos, elas também podem executar cálculos nos dados brutos para responder a perguntas específicas sobre dados. Cálculos realizados em várias linhas de uma tabela são chamados de <mark style="background: #FFB86CA6;">agregados</mark> .

- `COUNT( )` - A maneira mais rápida de calcular quantas linhas há em uma tabela
	- É uma função que recebe o nome de uma coluna como argumento e conta o número de valores não vazios nessa coluna.
	- Exemplo
		`SELECT` `COUNT`**(coluna)**
		`FROM` **tabela**;
--- 
- `SUM( )` - O SQL facilita a adição de todos os valores em uma coluna específica
	- É uma função que recebe o nome de uma coluna como argumento e retorna a soma de todos os valores dessa coluna.
	- Exemplo
		`SELECT SUM`**(coluna)**
		`FROM` **tabela**;
--- 
- `MAX( )` - Retorna o maior valor
	- Recebe o nome de uma coluna como argumento e retorna o maior valor dessa coluna.
	- Exemplo
		`SELECT MAX`**(coluna)**
		`FROM` **tabela**;
--- 
- `MIN( )` - Retorna o menor valor
	- Recebe o nome de uma coluna como argumento e retorna o menor valor dessa coluna.
	- Exemplo
		`SELECT MIN`**(coluna)**
		`FROM` **tabela**;
--- 
- `AVG( )` -  Função para calcular rapidamente o valor médio de uma coluna específica.
	- Recebe um nome de coluna como argumento e retorna o valor médio dessa coluna.
	-  Exemplo
		`SELECT AVG`**(coluna)**
		`FROM` **tabela**;
--- 
- `ROUND( )` - Arredondar os valores na coluna
	- Ele arredonda os valores na coluna para o número de casas decimais especificado por "inteiro" que se refere a quantidade de casas decimais. 
	- Exemplo
		`SELECT ROUND`**(coluna, inteiro)** \
		`FROM` **tabela**;
	- Exemplo2
		Você também pode tratar suas consultas com um arredondamento:
		`SELECT ROUND`(`AVG`(**coluna**), **2**)
		`FROM` **tabela**;
--- 


