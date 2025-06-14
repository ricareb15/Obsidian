## Linguagem DDL
Temos, então, que a DDL compõe o SQL e é utilizada na modelagem e no desenvolvimento de banco de dados para a definição de estruturas de dados como colunas, tabelas, linhas e índices.

**Suas principais funções são:**
- `CREATE` - Cria tabelas no banco de dados.
- `DROP` - Exclui tabelas ou outros objetos do banco.
- `ALTER`

**Também podem ser usadas:**
- `CREATE INDEX` Cria um novo índice em uma tabela
- `CREATE DOMAIN` Cria um tipo de dados definidos pelo usuário
- `ALTER INDEX` Altera o índice de uma tabela
- `DROP INDEX` Exclui um índice existente em uma tabela

**Também foram adicionados:**
- `TRUNCATE`
- `RENAME`

---
### CREAT TABLE
A instrução `CREAT TABLE` é usada para definir uma nova tabela usando a seguinte instrução:
```SQL
CREAT TABLE Alunos (
	id-aluno CHAR(20)
	nome CHAR(20)
	login CHAR(20)
	idade INTEGER
	media REAL) 
```

```ad-important
collapse: closed


| id-aluno | nome | loigin | idade | media |
| -------- | ---- | ------ | ----- | ----- |
|          |      |        |       |       |


```


---
### DROP TABLE
Esse comando remove a tabela do banco de dados, incluindo todos os dados e a definição da tabela. **Cuidado**, pois ao usar `DROP TABLE`, **tudo será apagado permanentemente** e não poderá ser recuperado a menos que haja um backup.

```SQL
DROP TABLE Cadastro;
```

---
### ALTER TABLE (ADD)
Para adicionar colunas a uma tabela existente no banco de dados usando SQL você pode utilizar o comando `ALTER TABLE`. Exemplo:

```sql
ALTER TABLE nome_da_tabela
ADD nova_coluna tipo_de_dados;
```
### INSERT
As tuplas são inseridas usando-se o comando `INSERT` Na qual podemos inserir uma única tupla na tabela Alunos, como segue:
```SQL
INSERT
INTO (id-aluno, nome, login, idade, media) 
VALUES (53688, "Smith", "smith@ee", 18, 3,2)
```
****Saída****

| id-aluno | nome  | loigin   | idade | media |
| -------- | ----- | -------- | ----- | ----- |
| 53688    | Smith | smith@ee | 18    | 3,2   |
Opcionalmente, podemos omitir a lista de nomes de coluna na cláusula INTO e listar os valores na ordem apropriada, mas é considerado boa prática ser explícito quanto aos nomes de coluna

---
### ALTER TABLE (DROP)
Para excluir colunas de uma tabela no banco de dados usando SQL, você pode usar o comando `ALTER TABLE` junto com `DROP COLUMN`. Exemplo:

```sql
ALTER TABLE nome_da_tabela
DROP COLUMN 
```

--- 
### SELECT
Para realizar consultas em um banco de dados SQL e buscar as tuplas (linhas de dados) de uma tabela, você deve usar o comando **`SELECT`**.

```SQL

SELECT <colunas> FROM <tabela>;
--Para consultar colunas específicas

OU

SELECT * FROM <tabela>;
--Para consultar todas as colunas
```

---

## Linguagem DML
A linguagem DML nasce para respaldar o contexto de manipulação de dados em bancos de dados, principalmente em sistemas de informação que fazem consulta em bancos de dados relacionais por meio de SGBDs. As principais funções são:

- INSERT (Inserir dados)
- SELECT (Selecionar o dado)
- UPDATE (Atualizar o dado)
- DELETE (Deletar o dado)

#### DELETE
Podemos excluir tuplas usando o comando `DELETE`. Podemos excluir todas as tuplas de Alunos com nome igual a Smith, usando o comando:
```SQL
DELETE
FROM Alunos A
WHERE A.nome = "Smith"
```
****Saída****

| id-aluno | nome  | loigin   | idade | media |
| -------- | ----- | -------- | ----- | ----- |
| 53688    | Smith | smith@ee | 18    | 3,2   |

--- 

#### UPTADE
Podemos modificar os valores de coluna em uma linha existente usando o comando `UPTADE`. Por exemplo
```SQL
UPTADE Alunos A 
SET A.idade = A.idade + 1, A.media = A.media - 1
WHERE A.id-aluno = 53688
```
****Saída****

| id-aluno | nome  | loigin   | idade | media |
| -------- | ----- | -------- | ----- | ----- |
| 53688    | Smith | smith@ee | 19    | 2,2   |

---
