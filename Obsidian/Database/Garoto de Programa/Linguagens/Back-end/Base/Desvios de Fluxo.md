### GoTo
O comando `GoTo` é um dos comandos de desvio de fluxo em VBA. Ele permite que você desvie a execução do seu código para uma linha específica identificada por um rótulo. Aqui está um exemplo simples de como usar o comando `GoTo`:
```vb
Sub ExemploGoTo()
    Dim valor As Integer
    valor = 5

    If valor > 0 Then
        GoTo Positivo
    Else
        GoTo Negativo
    End If

Positivo:
    MsgBox "O valor é positivo."
    Exit Sub

Negativo:
    MsgBox "O valor é negativo ou zero."
End Sub
```

### Call
No VBA, o comando "Call" é utilizado para chamar sub-rotinas e funções. Embora o uso do "Call" seja opcional na maioria dos casos, ele pode ajudar a aumentar a legibilidade do código. Aqui está um exemplo simples para ilustrar como ele funciona:

```vb
Sub valorTexto()
	texto = " estuda VBA"
End sub

Sub Nicole()
	Dim nome As String
	Dim sobrenome As strin
	
	nome = "Nicole"
	sobrenome = "Almeida"
	
	Call valorTexto
	
	MsgBox nome & sobrenome & texto
End sub
```

Percebe-se no exemplo, que existem dois "sub" separados um do outro. Para chamar o valor da variável que está no primeiro "sub" é necessário usar o respectivo comando.

O interessante é que esse comando consegue puxar o valor da variável de outro módulo