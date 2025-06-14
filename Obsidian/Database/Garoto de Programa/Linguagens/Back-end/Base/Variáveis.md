Os dados que utilizamos nos programas de computadores precisam ser armazenados na memória do computador. A memória é como um grande armário cheio de gavetas, usando essa analogia, as gavetas seriam as variáveis que possuem nomes e um tamanho que representam seu tipo.

---
### [[Linguagem C]]

#### Dicas
Evite começar com letras maiúsculas e números.
Não utilize caracteres especiais, como: "" , ( )
Evite variáveis como **a**, **b**, **n1**, **n2**, pois isso só tende a dificultar a interpretação do código.
Se a variável tem mais de uma palavra, utile uma letra maiúscula ou underline.
Não coloque sinais de pontuação na sua variável.

---
#### Tipos

| Nome   | Característica                                               | Exemplo |
| ------ | ------------------------------------------------------------ | ------- |
| int    | Números inteiros                                             |         |
| char   | Letras, caracteres, dados alfanuméricos                      |         |
| float  | Números reais com precisão simples, ocupa 4 bytes na memória |         |
| double | Números reais com precisão dupla , ocupa 8 bytes na memória  |         |
| void   | Vazio                                                        |         |

---
#### Modificadores de tipo
Além dos tipos, existem em C os modificadores de tipo:

| Nome     | Função                                                  |
| -------- | ------------------------------------------------------- |
| short    | Diminui o espaço em memória reservado para uma variável |
| long     | Aumenta o espaço em memória reservado para uma variável |
| unsigned | Indica que a variável será guardada sem sinal           |
| signed   | Indica que a variável será armazenada com sinal         |

---
#### Especificadores de formato
O especificadores de formato são utilizados nas funções de entrada e saída em C, como printf e scanf, para lidar com as diversas especificações existentes. Podendo então, formatar a saída, e interpretar a entrada de dados.
[[Especificadores de formato]]

---
#### Constantes
Seguem o mesmo conceito das variáveis. Mas como o próprio nome diz "constantes" servem para definir valores que nunca vão ser alterados (data de nascimento do usuário por exemplo)
[[Database/Eniac/Back-end/Linguagem C 1/ATIVIDADES/Orçamento do carro]]

---
### [[Linguagem Python]]
Utilizar variáveis em Python é extremamente simples, você não necessita definit o tipo de variável na declaração, como em outras linguagens. Basta fazer a atribuição do valor, e a linguagem define diretamente o tipo.

**Exemplo de declarações de variáveis válidas**
- x = 10
- nome = "Maria"
- Area_do_quadrado = Base * Altura
- CATETO2 = 200.345

**Nomes das variáveis**
- Começar com uma letra ou sublinhado
- Não começar com um dígito
- Ter no máximo 256 caracteres
- Letras, dígitos, sublinhados e cifrões podem ser inseridos
- Não conter espaços e símbolos matemáticos

**Exemplo de declarações de variáveis NÃO válidas**
- 20Casal = 300
- Nome de Familia = "Torres"
---
#### Tipos

| Nome            | Abreviação | Característica                                               | Exp                             |
| --------------- | ---------- | ------------------------------------------------------------ | ------------------------------- |
| Inteiros        | int        | Números inteiros, positivos ou negativos, sem casas decimais | 25                              |
| Ponto Flutuante | float      | Números reais, que incluem casas decimais                    | 1.75                            |
| String          | str        | Sequências de caracteres, usadas para representar texto      | "Maria"                         |
| Booleanos       | bool       | Valores lógicos que podem ser `True` ou `False`              | True                            |
| Listas          | list       | Coleções ordenadas e mutáveis de itens                       | [[Estrutura de Dados]] |
| Tuplas          | tuple      | Coleções ordenadas e imutáveis de itens                      | [[Estrutura de Dados]] |
| Dicionários     | dict       | Coleções de pares chave-valor, mutáveis                      | [[Estrutura de Dados]] |
| Conjuntos       | set        | Coleções não ordenadas de itens únicos                       | [[Estrutura de Dados]] |
#### Funções
##### Função "len"
A função `len()` em Python é usada para obter o comprimento (ou número de itens) de um objeto. Ela pode ser aplicada a diferentes tipos de objetos, como listas, strings, tuplas, dicionários, entre outros.
Exemplo: 
```python
minha_string = "Ricardo"
minha_lista [1, 2, 3, 4]

#para contagem de caracteres
>>> print(len(minha_string))
\\ Saída: 5

>>> print(len(minha_lista))
\\ Saída 4

#E também para revelar valor das posições
>>> print(minha_string[3])
\\ Saída: a
```
\#7
### [[JavaScript]]

>**Var**
>Qualquer tipo de informação 

>**Let**
>Só poderá ter uma nova declaração dentro de um bloco { }  

>**Const**
>Nunca poderá ter uma nova declaração

### [[Macros e VBA]]

#### Tipo de acesso
Em VBA, existem alguns tipos de acesso que você pode definir para variáveis, funções e procedimentos:

| Tipo      | Propósito                                                                                                                                                   |
| --------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `Public`  | Permite que o elemento seja acessível a partir de qualquer lugar no projeto.                                                                                |
| `Private` | Restringe o acesso ao elemento apenas dentro do módulo, classe ou formulário onde foi declarado.                                                            |
| `Dim`     | Similar a `Private` quando usado no nível do módulo, mas dentro de procedimentos, é usado para declarar variáveis locais.                                   |
| `Static`  | Utilizado para declarar variáveis que mantêm seus valores entre chamadas de procedimento, mas o acesso ainda é restrito ao procedimento onde foi declarado. |
#### Tipo de variável

| Tipos                 | Função                                              | VarType |
| --------------------- | --------------------------------------------------- | :-----: |
| String                | Texto com até 2 bilhões de caractéres               |    8    |
| Integer               | Números inteiros                                    |    2    |
| Byte                  | Valores de 0 a 255                                  |   17    |
| Boolean               | Valores True e False                                |   11    |
| Date                  | Datas                                               |    7    |
| Variant<br>(número)   | Tipo genérico<br>(Aceita núeros com casas decimais) |   36    |
| Variant<br>(caracter) | Tipo genérico                                       |         |
| Object                | Referência a um objeto                              |         |
| Double                | Aceita números com casas decimais                   |         |
##### Object
a função Object é utilizada para retornar uma referência a um objeto. Além disso o comando `Set` é utilizado para atribuir uma referência de objeto a uma variável.. 

```vb
Sub Exemplo_1()
	
	'Cria a variável ws do tipo Worksheet 
	Dim ws As Worksheet
	Dim textoCelula As Object
	
	'textoCelula vira um objeto da célula "Xx" na guia "xxx"
	Set textoCelula = Worksheets("xxx").Range(Xx)
	
	'Atribui uma planilha a essa variável
	Set ws = ThisWorkbook.Sheets("Planilha1")
	
End sub
```

```vb
Sub Exemplo_2()
	
	Dim mudaDados As Object
	Dim celulasSelecionadas As Range
	
	'A planilha 1 é atribuida a esta variável
	Set mudaDados = Planilha1
	
	'O valor da célula que está na planilha 1 deve ser atribuido ao seu nome
	mudaDados.Name = Planilha1.Range("Xx")
	
	Set celulasSelecionadas = Range("Xx:Xx")
	celulasSelecionadas.Active 'Seleciona as células
	celulasSelecionadas.Value = "VBA" 'VBA é atrivuido ao valor das células
	celulasSelecionadas.Clear 'Lima todo o conteúdo de Xx:Xx   
	
End sub
```
O uso do tipo `Object` é apropriado quando a natureza do objeto pode variar ou quando você precisa de flexibilidade adicional. Entretanto, quando o tipo de objeto é conhecido e específico, como no caso de intervalos de células, é recomendável utilizar o tipo específico, como `Range`.

##### VarType
para descobrir o tipo de uma variável ou o tipo de dado contido em uma célula. Para verificar o tipo de dado presente em uma célula.

- **vbEmpty (0)**: A variável não foi inicializada.
- **vbNull (1)**: A variável contém `Null`.
- **vbInteger (2)**: A variável contém um número inteiro.
- **vbLong (3)**: A variável contém um número de tipo `Long`.
- **vbSingle (4)**: A variável contém um número de tipo `Single`.
- **vbDouble (5)**: A variável contém um número de tipo `Double`.
- **vbCurrency (6)**: A variável contém um número de tipo `Currency`.
- **vbDate (7)**: A variável contém uma data.
- **vbString (8)**: A variável contém uma string.
- **vbObject (9)**: A variável contém um objeto.
- **vbError (10)**: A variável contém um erro.
- **vbBoolean (11)**: A variável contém um valor booleano (True ou False).
- **vbVariant (12)**: A variável contém um tipo `Variant`.
- **vbDataObject (13)**: A variável contém um `DataObject`.
- **vbDecimal (14)**: A variável contém um número decimal.
- **vbByte (17)**: A variável contém um número de tipo `Byte`.

```ad-example
title: Exemplo
collapse: closed

```vb
Dim tipo As Integer
Dim valor As Variant

'Suponha que a célula A1 tenha algum valor
valor = Range("A1").Value

'Verifica o tipo de dado presente na célula
tipo = VarType(valor)

```


##### Desafio
**"Insira o tipo de dado correto!"**
Como fazer caso o usuário insira um dado de variável não esperada?
Caso isso aconteça, podemos usar **if**, que confere se dentro da váriavel foi inserido um dado de acordo com seu tipo. Caso o usuário erre o sistema tras um aviso.
```vb
Sub somarRange()
	Dim a As Double
	Dim b As Double
	Dim soma As Double
	
	'O VarType retorna o tipo de variável em forma de número
	tipo = VarType(a)
	If tipo <> 5 then
		MsgBox "Tipo de valores não permitido"
		Exit sub
	End If 
	
	OU 
	
	'IsNumeric() retorna True ou False 
	If IsNumeric(a) <> True And IsNumeric(b) <> True then
		MsgBox "Tipo de valores não permitido"
		Exit sub
	End If


```
