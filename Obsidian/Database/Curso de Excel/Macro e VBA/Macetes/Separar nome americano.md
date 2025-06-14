Em empresas multinacionais os cadastros de clientes / funcionarios são realizados com uma formatação diferente. Os nomes por exemplo, é invertida a posição do nome com o sobrenome. Para resolver isso, podemos prepar um coódigo VBA que pode formatar da maneira que queremos.

```vb
Sub format_text
	
	Dim linha As Long
	Dim ultima As Long
	
	'Conta quantas linhas tem na tabela a partir de A1
	ultima = Range("A1").End(xlDown).Row
	
	Dim qntLetra As Integer
	Dim nome As String
	Dim resultado As String
	
	For linha = 2 To ultima
		
		'Encontrando a posição da vírgula
		qntLetra = InStr(1, Range("A" & linha).Value, ",")
```