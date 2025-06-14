Um banco de dados é um conjunto de valores e arquivos que se relacionam entre si e demostram um cadastro de pessoas, vendas, produtos, etc. A atividade pertinente a qualquer área de uma organização requer um poder grande de armazanemento de informações, ordenação, busca e direção. Com toda a certeza, a velocidade é importante e sempre levada em consideração, mas os outros pilares precisam ser garantidos. Esses pilares são:
#### Atomicidade
A atomicidade é responsável por garantir que uma trasação seja gravada com sucesso e garantida ou é realizado o rollback de toda transação para que o banco de dados retorne ao estado anterior daquela transação. A famosa regra do "tudo ou nada", ou toda a transação é salva com sucesso no banco ou toda a transação é decartada. 
#### Isolamento
Este pilar representa a independência de cada transação no sistema de gerenciamento de banco de dados. Cada transação é unica e independente. Imagine que exista apenas uma unidade de um produto em estoque e dois clientes realizam a compra desse item no mesmo segundo, como resolver? Por sorte, por se tratar de duas transações isoladas e independentes o problema foi resolvido rapidamente, garantindo a transação que for processada em primeiro lugar.
#### Concistência
As regras de um sistema sempre devem ser respeitadas para que o sistema de gerenciamento tenha atendido suas características de base. Isso inclui, por exemplo, que o tipo de valor inserido seja correto em relação ao tipo de seu atributo (VARCHAR, INT, DATE, etc). O tal do "Dado certo no local esperado"
#### Durabilidade
Quando uma transação é finalizada, seus dados estão a salvo de qualquer modificação. Somente outra transação pode modificar os dados . Assim os dados ficam protegídos

### Tipos de banco de dados
Com toda essa introdução sobre os sitemas de banco de dados, vamos abordar agora, quais são os tipos de banco de dados disponíveis e suas características e usos pelos divesos tipos de aplicações e corporações

- MySQL
- MariaDB
- Microsoft SQLServer
- PostgreSQL
- Oracle
- MongoDB
### Tipos de chave

#### Chave primária (PK)
A chave primária é um campo que é definido como único e não pode repetir-se naquela tabela. Como por exemplo a chave primária para a tabela "cliente" pode-se usar o CPF que é um número único por pessoa.

#### Chave secundária (FK)
A chave estrangeira ocorre quando pegamos um atributo que é uma chave primária em outra tabela. Seguindo a mesma lógica da tabela "cliente", quando formos fazer a tabela de "vendas" podemos usar a chave estrangeira em "CPF_cliente" para que o sistema por meio deste, consiga buscar as informações do cliente.

#### Chave Composta (?)

#### Dependências funcionais
As tabelas de banco de dados devem seguir uma regra para que fiquem livres de dados incorretos ou duplicados. Para garantir essa regra, foram definidas as dependências funcionais, que ocorrem quando um valor `A` depende de um valor `B`, ou seja, uma coluna depende de outra coluna da mesma tabela. As dependências funcionais se dividem em três:

---
##### Dependência funcional total
Quando houver uma chave primária concatenada, isto é, duas ou mais colunas são a chave primária de uma tabela, as demais colunas dependerão exclusivamente dessa ligação para que possam ser inseridas corretamente. Exemplo:

- Tabela Item/Venda
- `CodVenda PRIMARY KEY`
- `CodProduto PRIMARY KEY`
- `Qtd`

Repare que a coluna quantidade vai depender totalmente da chave primária concatenda ``Item/Venda``

---
##### Dependência funcional parcial
Ocorre quando um item da tabela depende de uma parte da chave primária concatenada da tabela, e não da chave toda. Exemplo:

- Tabela Item/Venda
- `CodVenda PRIMARY KEY`
- `CodProduto PRIMARY KEY`
- `Qtd`
- `PrecoProduto`

A `PrecoProduto` depende do valor da coluna `CodProduto`, que daz parte da chave primária da tabela Item/Venda. Portanto `PrecoProduto` depende parcialmente da chave primária concatenada da tabela.

---
##### Dependência funcional transitiva
Acontece quando uma coluna da tabela depende de outra coluna da tabela que não é chave dessa tabela. Exemplo:

-  Tabela Item/Venda
- `CodVenda PRIMARY KEY`
- `CodProduto PRIMARY KEY`
- `Qtd`
- `PrecoProduto`
- `TotalParcial`

A coluna `TotalParcial` depende do resultado da multiplicação das colunas `Qtd` por `PrecoProduto` e essas colunas não são chave da tabela.
### Tipos de dados
No momento de codificação da tabela, é necessário atribuir o tipo de dado que a coluna relacionada poderá receber. Qualquer coisa diferente disso será descartada pelo próprio banco de dados, que não aceitará a inserção. São elas:

| Tipo            | Descrição                               | Exemplo       |
| --------------- | --------------------------------------- | ------------- |
| INT ou INTERGER | Recebe apenas números inteiros          | 45002         |
| VARCHAR         | Recebe caractéres alfanumericos         | João da Silva |
| DATE            | Recebe apenas datas válidas             | 01/01/2024    |
| TIME            | Recebe apenas valores expressos em hora | 16:54         |
| BOOL ou BOLEAN  | Recebe apenas 0 e 1; Para True e False  |               |

### Linguagem SQL
Para realizar a inserção, remoção, edição ou qualquer outra atividade com os dados que irão ou estão no banco de dados, é necessária uma interação por meio da [[Linguagem SQL]] (Linguagem de Consulta Estruturada)