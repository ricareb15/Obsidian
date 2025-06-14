## Nova coluna
Para criar uma nova coluna é necessário seguir o passo a passo a seguir:
>1. Ferramenta de tabela
>2. Nova coluna
```ad-summary
title: Imagem
collapse: closed

![[Pasted image 20250401182341.png]]

```

### DAX
(Data Analysis Expressions) é uma linguagem de fórmulas projetada para trabalhar com dados em modelos tabulares. Ele permite criar medidas, colunas calculadas e tabelas que ajudam a realizar cálculos e análises avançadas de dados.

Leve em consideração que quanto mais dessa linguagem você usar, mais pesado ficará seu arquivo, o recomendado é sempre fazer o tratamento dos dados pelo por uma Macro no Excel ou **Power Query**  
#### [[Operadores]]
>Operadores Aritméticos
>Operadores de Comparação
>Concatenação de Texto

---
#### [[Funções - DAX]]
Refere-se ao processo de resumir ou calcular valores com base em um conjunto de dados. Isso é usado em modelos de dados para criar medidas e cálculos personalizados.
##### Básicas
>`SUM` - Soma os valores de uma coluna
>`AVERAGE` - Calcula a média dos valores de uma coluna
>`MIN` - Retorna o menor valor de uma coluna
>`MAX` - Retorna o maior valor de uma coluna
>`COUNT` - Conta o número total de valores em uma coluna, incluindo valores duplicados
>`DISTINCTCOUNT` - Conta o número de valores únicos em uma coluna
##### Interativas
>`SUMX` - Retorna a soma de uma expressão avaliada para cada linha da tabela
>`AVERAGEX` - Calcula a média dos resultados de uma expressão avaliada para cada linha
>`MINX` - Retorna o menor resultado de uma expressão avaliada para cada linha
>`MAXX` - Retorna o maior resultado de uma expressão avaliada para cada linha
##### Lógicas
>`COUNTROWS` - Conta o número de linhas em uma tabela
>`COUNTA` - Conta o número de valores não vazios em uma coluna
##### Texto
>`CONCATENAR` - Usado para unir dois elementos
>`UPPER` - Converte todo o texto para letras maiúsculas.
>`LOWER` - Converte todo o texto para letras minúsculas.
>`SUBSTITUTE` - Substitui partes específicas de um texto por outro valor especificado
>`LEN` - Retorna o número de caracteres (incluindo espaços).
>`MID` - Extrai uma parte do texto por um índice inicial e no número de caracteres definidos
##### Relacionamento
>`RELATED` - Permite trazer um valor de uma tabela que está conectada por meio de um relacionamento, um ID por exemplo. 
##### Datas
>`YEAR` - Apresenta o ano do dado fornecido
>`MONTH` - Apresenta o mês do dado fornecido
>`DATE` - Apresenta o dia do dado fornecido
>`FIRSTDATE` - Traz o primeiro dia de um conjunto de dados
>`LASTDATE` - Traz o último dia de um conjunto de dados
```ad-hint
title: DATEADD
collapse: closed

Essas funções são usadas para calcular o dia/mês/ano tanto **próximo** quanto **anterior**, a partir de um contexto de filtro.


### Exemplo
Por exemplo, calcular o valor total das vendas da "Aline" depois de uma semana

Valor Soma = **CALCULATE**(**SUMX**(Vendas, Vendas[Quantidade] * Vendas[Preço Unitário]), Vendas[Vendedor = "Aline"), **DATEADD**(Vendas[Datas], 7, MONTH)

### Importante
Elas são especialmente úteis para análises temporais, como fazer análise do próximo dia ou mês de uma data específica em um relatório.

A funções depende da existência de uma tabela de datas adequadamente configurada (normalmente chamada de tabela de calendário) e vinculada ao seu modelo.


```

`PREVIOUSDAY`
`PREVIOUSMONTH`
`PREVIOUSYEAR`

---
#### Medidas
Siga o seguinte raciocínio: Suponhamos que na nossa base de dados nós precisamos cálcular os **ganhos da empresa**. E no banco de dados disponível temos o **preço dos produtos** e a **quantidade vendida** por funcionário.

Neste caso, podemos criar uma nova coluna com **agragação** de multiplicação pois vai criar um dado estável onde será calculado quanto o vendedor teve de ganho com este produto 

E em seguida podemos fazer uma **medida**, que soma os ganhos de todos os funcionários, totalizando os ganhos da empresa. Mas o interessante das medidas é que elas são dinâmicas, ou seja, no nosso dashboard se quisermos saber os ganhos de apenas um funcionário (apertando em um botão no dashbard por exemplo), os dados serão rapidamente atualizados 
```ad-note
title: Passo a Passo
collapse: closed

As medidas são normalmente criadas em novas tabelas
1. No Power BI
2. Ferramentas da tabela
3. Nova tabela
4. Nova medida

```


---

#### [[Estrutura de condição]]
A Estrutura de Condição é usada em programação para avaliar situações específicas e executar comandos com base em um teste lógico. Ela permite que o código tome decisões conforme condições pré-definidas
>`IF`
>`AND`
>`OR`
>`SWITCH`
>`CALCULATE`