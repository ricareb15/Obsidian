Estruturas de repetição são artifícios das linguagens de programação para executar um determinado bloco de código por uma certa quantidade de vezes, seja ela definida (utilizando o for) ou a partir de uma condição (utilizando o while).
## [[Linguagem Python]]
### While
Do inglês "enquanto", ela permite a repetição de um bloco de código enquanto uma determinada condição for verdadeira (por um certo número de vezes ou até uma condição seja atingida). 
Por isso é utilizado a **Variável contadora**, ela deve ser inicializada antes do comando e ser incrementada ou decrementada dentro do bloco de instrução.

Nesse exemplo é utilizado uma variável contadora, que incrementa o seu valor a cada execução
```Python
cont = 1

while cont<=3:
	print (str(cont) +'a execução do laço')
	cont+=1

**SAÍDA**
1a execução do laço
2a execução do laço
3a execução do laço
```

Nesse exemplo é utilizado uma variável contadora, que decrementa o seu valor a cada execução
```Python
cont = 5

while cont>=1:

print('Imprimindo', (5-cont+1), 'mensagem')
cont-=1

**SAÍDA**
Imprimindo 1 mensagem
Imprimindo 2 mensagem
Imprimindo 3 mensagem
Imprimindo 4 mensagem
Imprimindo 5 mensagem
```
#### continue
O comando `continue` interrompe o fluxo de execução do laço de repetição. Porém, ele avança para a próxima execução do loop
```Python
cont = 1
while cont<10
	cont+=1
	if(cont%2==1)
		continue
	print(cont)
```
#### break
O comando `break`, quando utilizado dentro de um laço de repetição, serve para interromper a repetição, encerrando a execução do loop e, em seguida, saltando para a linha de código imediatamente após o bloco de instruções do laço
```Python
cont = 1
while True:
	print (str(cont)+"a execução do while")
	cont+=1

	if (cont>3):
		break

print ("Execução do while acabou")

**SAÍDA**
1a execução do while
2a execução do while
3a execução do while
Execução do while acabou
```


---

### For...in
Diferente do while, o `for` executará um determinado bloco de código por um número definido de vezes. Esta estrutura é muito útil quando já sabemos a quantidade de vezes que precisamos executar determinado bloco de código.
```python
for i in range(1, 10):
    print(i)

**SAÍDA**
1
2
3
4
5
6
7
8
9
```
```ad-important
collapse: closed
Se fizessemos uma tradução literal do comando, atradução seria:
**Para cada i, no intervalo de 1 até 10**

```

#### Introdução
Agora, para que possamos entender bem essa estrutura de repetição vamos conversar um pouquinho... Primeiramente, vamos trabalhar com o exemplo: **For `x` in `y`**  

##### O que pode ser substituído por `x`?
`x` é uma **variável** que recebe cada elemento da coleção `y`. Ele pode ser qualquer nome de variável que faça sentido no contexto. Alguns exemplos:

- Nomes genéricos: `i`, `j`, `k`, `n`, `elem`.
- Nomes descritivos: `nome`, `idade`, `cidade`, `item`, `valor`.
- Variáveis compostas: `chave, valor` (em caso de dicionários ou desempacotamento).

##### O que pode ser substituído por `y`:
`y` são os elementos, ou seja, a coleção de dados que será percorrida pelo laço. Exemplos comuns incluem:

- **Listas**: `[1, 2, 3]`, `['a', 'b', 'c']`.
- **Tuplas**: `(4, 5, 6)`.
- **Dicionários**: `{"nome": "Ricardo", "idade": 28}`.
    - Para percorrer apenas as chaves: `meu_dicionario.keys()`.
    - Para percorrer apenas os valores: `meu_dicionario.values()`.
    - Para percorrer pares chave-valor: `meu_dicionario.items()`.
    
- **Strings**: `"Python"` (percorre cada caractere).
- **Range**: `range(1, 10)` (intervalo de números).
- **Conjuntos (sets)**: `{7, 8, 9}`.

##### Exemplos
```python
#Com uma lista
for item in [1, 2, 3]:
    print(item)

#Com uma String
for letra in "Python":
    print(letra)

#Com um Dicionário
for chave, valor in {"nome": "Ricardo", "idade": 28}.items():
    print(f"Chave: {chave}, Valor: {valor}")

#Com uma String
for caracter in "python":
	print(caracter)

#Com um Range
for numero in range(1, 5):
    print(numero)

```

#### Atividades

##### Quantidade de caracteres em frase
Se quisermos contar quantas caracteres existem em uma frase, podemos usar a função `for`, juntamente com uma variável, para a contagem de caracteres. Dentro da estrutura do comando for, a cada letra que ele percorre na frase, a variável `qntLetras` é incrementada, isto é, acrescida uma inidade para seu valor. Pode-se dizer que essa variável é uma **variável contadora**.

```Python
frase = "A ligeira raposa marrom ataca o cão preguiçoso"

qntLetras = 0

for letra in frase:
	qntLetras += 1

print("A frase possui" + str(qntLetras) + "Letras.")

**Saída**
# A frase possi 47 letras.
```

##### Cálculo de média
Um exemplo clássico é o algoritmo para o cálculo de uma média, que a variável `soma` vai aumentando seu valor a cada interação do comando `for`, sempre se somando com o valor da variável de interação do comando `for`. A variável `soma` é uma **variável acumuladora**.
```python
dados = [1, 3, 5, 8, 10, 2]

soma = 0
qnt = 0

for valor in dados
	soma += valor
	qnt += 1

print(soma)
print(qnt)

media = soma / qnt

print(media)

**Saída**
# 29
# 6
# 4,83333333333
```

##### Procura do número primo
É possível usar o comando `for` para criar um algoritmo que busque os números primos dentro de um intervalo de valores. No exemplo, o primeiro comando for percorre uma lista de 20 números iniciada em 0, que é produzida pelo comando `range`. O segundo comando for faz o teste de divisão com todos os números pra ver se existe resto de divisão 
```python
numPrimos = []

for numero in range(20):
	div = 0
	for divisor in range(1, numero + 1):
		if (numero % divisor) == 0
			div += 1
	if div == 2:
		numPrimos.append(numero)

print(numPrimos)

**Saída**
# [2, 3, 5, 7, 11, 13, 17, 19]

```


### Else
O Python também permite adicionar o comando `else` depois de uma estrutura de repetição, seja ela um `for` ou um `while`. Este `else` serve para executar um determinado bloco de código imediatamente após a estrutura de repetição finalizar:
#### While/Else
```python
gastos 0 
valor_gasto 0 
while gastos < 1000:
	valor gasto int(input("Digite o valor do novo gasto: "))
	gastos = gastos + valor_gasto
else:
	print("Você gastou demais!") 
print(gastos)

**SAÍDA**
Digite o valor do novo gasto: 300 
Digite o valor do novo gasto: 500 
Digite o valor do novo gasto: 200 
Você gastou demais! 
1000
```

#### For/Else
```python
for i in range(1, 10):
	print(1)
else:
	print("fim do loop")

**SAÍDA**
1
2
3
4
5
6
7
8
9
fim do loop
```

## [[Linguagem C]]

## [[Macros e VBA]]
### Introdução
Existem várias estruturas de repetição. São elas
>Do e Loop
>While
>For

Nos exemplos, o objetivo é construir uma estrutura que análise célula a célula de uma lista e pinte as células que o usuário procura
![[Pasted image 20250221193324.png]]

![[Estrutura de repetição.xlsm]]

### Do e Loop
Estrutura
```vb
Sub dowhile()
Dim contador As Integer

contador = 0

Do
	MsgBox "Olá"
	contador = contador + 1
	
	if contador = 5 Then
		Exit Do
	End if
Loop

```

Exemplo
```vb
Sub estruturaRpt()

'Desliga os movimentos feitos na planilha na hora da execução
Application.ScreenUpdating = False

Dim numProcurado As Integer
Dim i As Integer
Dim procurando As Integer

i = 2
numProcurado = Range("D5")
Do

procurando = Cells(i , 1)

'Se usássemos procurando ao invés de cells
'Faríamos algo como: "If procurando = 0"
'Mas o númeo da lista pode ser um 0
If cells(i , 1) = "" Then
	Exit sub
End If

If numProcurado = procurando Then
	
	'A célula é selecionada
	Cells(i , 1).Select
	
	'O objeto - que está selecionado - modifique o interior
	With Selection.Interior
		.Color = RGB(x , x , x)
	End With
End If

i = i + 1
Loop
Application.ScreenUpdating = True

End Sub
```
### While
```vb
Sub while1()
Dim contador As Integer

contador = 0

While contador < 5
	Msgboc contador
	contador = contador + 1
Wend

End sub

```
### For
Diferente do while, o `for` executará um determinado bloco de código por um número definido de vezes. Esta estrutura é muito útil quando já sabemos a quantidade de vezes que precisamos executar determinado bloco de código.

Estrutura
```vb
Sub for1()
Dim i As Integer

'Tradução: Meu i começa no 1 até o 10
For i = 1 To 10
	Msgbox i
Next

'Conta de 2 em 2
For i = 2 To 20 Step 2 
	MsgBox "Número: " & i
Next

'Regridi a contagem
For i = 20 To 1 Step -1 
	MsgBox "Número: " & i
Next


 ```
Meu *i* começa no **1** até o **10**

```ad-example
title: Exemplo
collapse: closed

```vb
Sub buscaSabor()

'Desliga os movimentos feitos na planilha na hora da execução
Application.ScreenUpdating = False

Dim i As Integer
Dim procurado As String
Dim total As Integer
Dim buscando As String

procurado = Range()

'Selecione a primeira célula da lista
Rannge("A1").Select

'Poderia fazer da seguinte forma: Range ("a1:a5").Select
'Mas caso houvesse um novo item na lista ele não selecionaria 
'De onde está selecionado - para baixo (até último) - Selecione tudo
Range(selection, selection.End(xlDown)).Selection

'Conte tudo que está selecionado
total = selection.Count

'(2 To total) caso não queira conferir o cabeçalho
For i = 1 To total
	buscando = Cells(i, 1)
	
	If buscando = procurado Then
		Cells(i, 1).Select
		
		With selection.interior
		.Color = RGB(x , x , x)
		
	End With
Next

Application.ScreenUpdating = True

End Sub
```
> Neste exemplo o código procura uma célula específica (ou pode ser um dado) em uma lista e a pinta destacando-a

