### MsgBox
Essa função permite mostrar mensagens ao usuário e obter retornos baseados em botões que ele clica. Muito utlizado para informar um erro ou dar um aviso ao usuário

![[Pasted image 20250218195826.png]]

#### Parâmetros
**Prompt** (obrigatório)
>O texto a ser exibido na caixa de mensagem. Pode ter até 1024 caracteres.
>Exemplo: `"Deseja salvar o arquivo?"`.

**Buttons** (Opcional):
Define os botões, ícones e tipo de mensagem exibidos na caixa.
>**vbOK** Exibe apenas o botão "OK".
>**vbCancel** Exibe os botões "OK" e "Cancel".
>**vbAbort** Exibe os botões "Abort", "Retry" e "Ignore".
>**vbRetry** Exibe os botões "Retry" e "Ignore".
>**vbIgnore** Exibe os botões "Ignore" e "Retry".
>**vbYesNo** Exibe os botões "Yes" e "No".
>**vbYesNoCancel** Exibe os botões "Yes", "No" e "Cancel".
>**vbRetryCancel** Exibe os botões "Retry" e "Cancel".

**Title** (Opcional):
>Especifica o título da janela da mensagem.
>Exemplo: `"Confirmação"`.

**Verificando resposta do usuário**
```vb
Dim resposta As Integer
resposta = MsgBox("Deseja salvar?", vbYesNo + vbQuestion, "Confirmar")

If resposta = vbYes Then
	MsgBox "Você escolheu SIM."
Else
    MsgBox "Você escolheu NÃO."
End If
```

Exemplo:
```vb
'Simples
Sub mensagemSimples()
	MsgBox "Boa noite!"

'Com célula
Sub mensagemRange()
	'Range significa a célula
	MsgBox Range("B10")
	
	'Cells também serve para identificar uma célula
	MsgBox Cells(1, 2)
	'(Linha x , Coluna x)

'Célula de outra guia
Sub mensagemRange_2()
	'Caso precise resgatar uma célula de outra guia
	MsgBox Sheets("Guia x"). Range("B10")

'Célula + texto
Sub unirMensagen()
	'Caso precise juntar dois conteúdos
	MsgBox "O texto da célula B10 é" & Range("B10")

'Quebra de linha
Sub quebrarMensagen()
	'Utiliza "vbCrLf" ou "Chr(13 ou 10)" caso precise quebrar a linha
	MsgBox "Boa" & vbCrLf & "noite!"

'MsgBox de Erro
Sub mensagemCritica_1()
	MsgBox "Atenção! Erro ao executar", vbCritical, "título"

'Lógica MsgBox de Erro
Sub logicaErro()
	Dim nota As Integer
	nota = 10
	
	If nota > 10 Then
		MsgBox "Erro! Nota não pode ser maior que 10!", vbCritical, "título"
	
	Else
```
```ad-seealso
title: Considerações
collapse: closed

**[[Alta Hierarquia|Application]].UserName** permite acessar ou alterar o nome do usuário registrado no aplicativo do Microsoft Office
```

### InputBox
Permite solicitar ao usuário que insira um valor ou texto
Exibindo uma caixa com um campo de texto para entrada.
É útil para capturar informações simples diretamente do usuário.
Exemplo:
```vb
Dim nome As String
nome = InputBox("Qual é o seu nome?", "Entrada de Dados")
MsgBox "Olá, " & nome & "!"
```

### UserForms
Os **UserForms** são janelas personalizáveis que você pode criar no editor de VBA. Eles permitem maior controle sobre a interface e interatividade.

- Interface mais profissional e interativa.
- Permite validação de dados, botões múltiplos e design sob medida.


### Função `Application.InputBox`
Uma alternativa ao `InputBox`, mas com mais flexibilidade, como a opção de selecionar intervalos diretamente na planilha para responder o campo de texto da caixa

```vb
Dim rng As Range
Set rng = Application.InputBox("Selecione um intervalo:", Type:=8)
MsgBox "Você selecionou " & rng.Address
```
O parâmetro `Type:=8` indica que o usuário deve selecionar um intervalo de células.