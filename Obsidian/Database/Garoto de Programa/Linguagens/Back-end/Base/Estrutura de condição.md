A Estrutura de Condição é usada em programação para avaliar situações específicas e executar comandos com base em um teste lógico. Ela permite que o código tome decisões conforme condições pré-definidas

## [[Linguagem Python]]
### IF...Else...Elif
O uso do `if` em um programa em Phyton visa verificar se determinada ação é verdadeira e executar o bloco de código contido em seu escopo
#### IF
Basicamente é feita da seguinte forma: 
```python
media = 7
if media > 6.9:
	print ("Você foi aprovado")
```

#### if/else
Já o uso o `if/else` fará com que uma das ações sejam executadas, já que se a condição dentro do `if` não for verdadeira, será executado o código contido no `else`.
```python
media = 7
if media < 6.9:
	print ("Você foi reprovado")
else:
	print ("Você foi aprovado")
```

#### if/else/elif
O uso de `if/elif/else` serve para quando mais de uma condição precisar ser verificada. Vimos anteriormente que utilizamos o `if` para testar se uma condição é verdadeira, porém, quando precisamos verificar uma segunda condição utilizamos o `elif` e adicionamos a condição a ser testada.
```python
if idade < 0: 
	print("Idade inválida.") 

elif idade < 12: 
	print("Você é uma criança.") 

elif idade < 18: 
	print("Você é um adolescente.") 

elif idade < 30:
	print("Você é um jovem adulto.") 

elif idade < 50: 
	print("Você é um adulto.")

else: 
	print("Você é um idoso.")
```

### Switch
 A variável switch segue a mesma lógica de um "SE.OU" (no Excel) na qual é apresentado diversos possíveis casos/possibilidades, e o que deve ser feito.

```c
switch (expressão) { 

case valor1: 
// Bloco de código executado se a expressão for igual a valor1 
break; 

case valor2: 
// Bloco de código executado se a expressão for igual a valor2 
break; 
// ... pode haver mais casos

default: 
// Bloco de código executado se nenhum dos casos for correspondente 
break; }
```

## [[Linguagem C]]
### Switch
 A variável switch segue a mesma lógica de um "SE.OU" (no Excel) na qual é apresentado diversos possíveis casos/possibilidades, e o que deve ser feito.

```c
switch (expressão) { 

case valor1: 
// Bloco de código executado se a expressão for igual a valor1 
break; 

case valor2: 
// Bloco de código executado se a expressão for igual a valor2 
break; 


// ... pode haver mais casos

default: 
// Bloco de código executado se nenhum dos casos for correspondente 
break; }
```

## [[Macros e VBA]]
### IF...Else
A estrutura  é ideal para cenários onde há poucas condições a serem avaliadas ou quando as condições não seguem um padrão claro. Ela permite fazer verificações sequenciais e tomar decisões com base em resultados booleanos ( ou ). Por exemplo:

```vb
Sub ExemploIfElseIfAndOrNot()
	Dim idade As Integer
	Dim salario As Double
	Dim resultado As String
	
	idade = 25
	salario = 3000
	
	If Not (idade < 18) And idade <= 65 Then
		
		If salario > 2500 And salario <= 5000 Then
			resultado = "Você tem uma faixa etária adequada ao seu salário"
		ElseIf salario > 5000 Then
			resultado = "Você tem uma faixa etária adequada salário é alto."
		Else
			resultado = "Você tem uma boa faixa etária, salário é baixo."
		End If
		
	ElseIf idade < 18 Then
		resultado = "Você é menor de idade."
	ElseIf Not (idade > 65) Then
		resultado = "Você está na faixa etária para aposentadoria."
	Else
		resultado = "Idade inválida."
	End If
	
	MsgBox resultado
End Sub
```

### Select Case
Select Case (**Selecione Caso**) é mais eficiente e legível quando há múltiplos valores ou intervalos a serem avaliados, especialmente se eles estiverem relacionados a uma única variável ou expressão. Em vez de várias condições , o  avalia apenas uma vez o valor da expressão e distribui os fluxos conforme os casos definidos

Exemplo (Dia da Semana)
```vb
Dim diaSemana As String

diaSemana = "Segunda-feira"

Select Case diaSemana
    Case "Segunda-feira"
        MsgBox "Início da semana. Foco total!"
    Case "Sexta-feira"
        MsgBox "Sextou! Hora de relaxar."
    Case "Sábado", "Domingo"
        MsgBox "É fim de semana! Aproveite!"
    Case Else
        MsgBox "Dia comum de trabalho ou estudo."
End Select

```

Exemplo (Números) - **Is**
```vb
Dim numero As Integer

numero = InputBox("Digite um número entre 1 a 10")

Select Case numero
	
	Case 1 To 5
		MsgBox "Você digitou entre 1 e 5"
		
	Case 6, 7, 8
		MsgBox "Você digitou entre 6 e 8"
		
	Case 9 To 10
		MsgBox "Você digitou entre 9 e 10"
		
	Case Is > 10
		MsgBox "Você digitou um número maior que 10"
		
	Case Else
		MsgBox "Número fora do padrão"
	
End Select
```

Exemplo (MsgBox)
```vb
Dim resultado As VbMsgBoxResult
resultado = MsgBox ("Escolha uma das opções a seguir:", vbYesNoCancel)

Select Case resultado
	
	Case vbYes
		MsgBox "Você clicou em SIM"
		
	Case vbNo
		MsgBox "Você clicou em NÂO"
		
	Case vbCancel
		MsgBox "Você clicou em CANCELAR"
		
	
End Select
```

Exemplo (texto)
```vb
Dim texto As String
texto = InputBox ("Digite uma palavra")

Select Case True
	
	'Avalia se há
	Case texto Like "*a*"
		MsgBox "Tem a letra A na frase"
		
	Case Else
		MsgBox "Não encontramos a letra A"
```

## [[Power BI]]
### IF
O uso do `if` visa verificar se determinada ação é verdadeira e executar o bloco de código contido em seu escopo. 

Diferente dos outros programas e linguagens, este `IF` não possui tem estruturas para utilizar `Else`. Caso precise de duas condições utile uma condição dentro da outra. Exemplo:

1 [Nome da nova coluna] = IF( [sheet(coluna)] >= 6, "Aprovado(a)", "Reprovado(a)" 

### AND
Esta também é uma função de condição, onde você pode adicionar várias condições, em que, se alguma delas for verdadeira, o retorno será verdadeiro `True` ou falso `False`.

Para fazer várias condições, podemos seguir a mesma ideia do `IF`, só colocar as condição umas dentro das outras. 

1 [Nome da nova coluna] = AND( [sheet(coluna)] >= 6, [sheet(coluna)] = "Artes " 

### OR
Esta também é uma função de condição, onde você pode adicionar várias condições, em que, se alguma delas for verdadeira, o retorno será verdadeiro `True` ou falso `False`.

Para fazer várias condições, podemos seguir a mesma ideia do `IF`, só colocar as condição umas dentro das outras. 

1 [Nome da nova coluna] = OR( [sheet(coluna)] >= 6, [sheet(coluna)] = "Artes "

### SWITCH
Neste tipo de condição você pode definir os resultados possíveis de uma coluna e definir o que será apresentado para cada um. Exemplo:
1 [Nome da nova coluna] = SWITCH( [sheet(coluna)],
		[Resultado possível], Apresentação,
		[Resultado possível], Apresentação,
		[Resultado possível], Apresentação,
		[Resultado possível], Apresentação,
		Apresentação caso não hája um resultado que não foi definido 

---
### CALCULATE
É utilizado para fazer cálculos integrado a filtros. Além disso é considerado uma função lógica pois permite aplicar condições e mudar o contexto de filtro.

Por exemplo, calcular o valor total das vendas apenas de uma coluna

Valor Soma = CALCULATE(SUMX(Vendas, Vendas[Quantidade] * Vendas[Preço Unitário]), Vendas[Categoria] = "Produto")
