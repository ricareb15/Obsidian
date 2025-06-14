---
aliases:
  - Workbook_Deactive
---
Para utlizar as propriedades do Workbook não é necessário escrevelas, é apenas necessário fazer a alteração no Visual Basic seguindo os passos a seguir:

1. Painel de controle
2. Desenvolvedor
3. Visual Basic
4. ![[Pasted image 20250227180643.png]]
5. ![[Pasted image 20250227180728.png]]
6. Em "Geral" selecione a opção "Workbook"
7. Em "Declaração" selecione o evento que desejar


## Abertura e Fechamento
### Workbook_Open( )
O evento `Workbook_Open` em VBA é usado para executar código automaticamente quando uma pasta de trabalho é aberta. Isso pode ser útil para automatizar tarefas 
Por isso, por padrão, a Microsoft deixa as opções de Macro inicialmente bloqueadas, impedindo que algum código malicioso seja executado no computador. Siga o passo a passo a seguir e a partir disso, o código que for escrito será executado automaticamente

```vb
Private Sub Workbook_Open()
	Dim minhaSenha As String
	minhaSenha = InputBox("Digite sua senha")
	
	If minhaSenha = "123" Then
		msgBox "Bem vindo(a) a planilha!"
	Else
	
		msgbox "Senha inválida, até a próxima"
		Workbooks("NOME DA PLANILHA.xlsm").Close 
Else
```

### Workbook_BeforeClose
O evento **Workbook_BeforeClose** no VBA é disparado antes de uma pasta de trabalho ser fechada. Ele é muito útil quando você deseja executar uma ação específica antes do fechamento, como salvar alterações, exibir uma mensagem para o usuário ou até mesmo cancelar o processo de fechamento.
```vb
Private Sub Workbook_BeforeClose()

	Dim senha As String
	
	senha = InputBox("Digite sua senha para sair")
	
	if senha = "123" Then
	
		'Ativa o botão para fechar a planilha
		Cancel = False
	
	Else
	
		'Desliga o botão para fechar a planilha
		Cancel = True
	
	End If
	
End Sub
```

## Alteração de Foco
### Workbook_Deactive
O evento Workbook_Deactivate (**Desativar**) no VBA é acionado automaticamente sempre que uma determinada pasta de trabalho perde o foco, ou seja, quando o usuário muda para outra pasta de trabalho ou aplicativo no Excel. Esse evento pode ser útil para executar ações específicas antes que uma pasta de trabalho deixe de ser a ativa.

- Você pode configurar a pasta para salvar automaticamente ao ser desativadaVocê
- Pode notificar o usuário sobre pendências, como não esquecer de salvar ou concluir algo antes de sair da pasta


### Workbook_SheetBeforeDoubleClick
O evento Workbook_SheetBeforeDoubleClick (**Folha antes do clique duplo**) no VBA é acionado sempre que o usuário dá um duplo clique em uma célula de qualquer planilha dentro da pasta de trabalho. Ele permite capturar essa ação e executar um código personalizado antes que o Excel entre no modo de edição da célula.


### Workbook_SheetChange
O evento Workbook_SheetChange (**Mudança de Folha**) no VBA é acionado sempre que o conteúdo de uma célula é alterado em qualquer planilha de uma pasta de trabalho. Ele é útil para monitorar mudanças e realizar ações automáticas baseadas nelas, como validação de dados, cálculos adicionais ou atualizações dinâmicas.
```vb
Private Sub Workbook_SheetChange(ByVal Sh As Object, ByVal Target As Range)
	
	'Verifica se a coluna B foi alterada
	If Target.Column = 2 Then
		
		'Deixa somente a primeira letra maiúscula
		Target = StrConv(Target, vbProperCase)
		
	
	'Verifica se a coluna C foi alterada
	ElseIf Target.Column = 3 Then
		
		'Deixa somente a primeira letra maiúscula
		Target = StrConv(Target, vbProperCase)
	End If
	
End Sub
```
```ad-note
title: Glossário
collapse: closed
**Target**
O Target é um parâmetro do evento Workbook_SheetChange que representa a célula ou o intervalo de células que foram alteradas.

**StrConv**
A função StrConv (abreviação de "String Convert") é usada para converter uma cadeia de caracteres para diferentes formatos de texto. No código, ela está sendo usada para formatar o conteúdo da célula.
Outros valores que podem ser usados com **StrConv**:

- `vbUpperCase`: Converte o texto para **letras maiúsculas**.
- `vbLowerCase`: Converte o texto para **letras minúsculas**.

**vbProperCase**
vbProperCase é uma constante utilizada pela função **StrConv**. Ela especifica que o texto deve ser convertido para o formato de "Título", onde somente a primeira letra de cada palavra é maiúscula, e as demais ficam minúsculas.

```


### Workbook_NewSheet
O evento Workbook_NewSheet (**Nova Folha**) no VBA é acionado automaticamente sempre que uma nova planilha é criada dentro da pasta de trabalho. Ele pode ser utilizado para personalizar o comportamento ou realizar ações automáticas toda vez que uma nova planilha é adicionada.
```vb
Private Sub Workbook_NewSheet(ByVal Sh As Object)
	
	If Application.UserName <> "NOME" Then
	 
		Application.DisplayAlerts = False
		sh.Delete
		MsgBox "Somente o usuário Ricardo pode adicionar uma nova guia"
	
	Else
		
		MsgBox "Planilha adicionada com sucesso"
	
	End If
	
End Sub
```
```ad-note
title: Glossário
collapse: closed
**Application.DisplayAlerts**
Este comando faz com que não haja o aviso de que a guia será excluida, por que se não o usuário terá a opção de cancelar

**Sh**
Ele não é exatamente um "comando", mas sim um objeto que faz referência à planilha envolvida no evento. Ele é usado para identificar ou manipular a planilha onde a ação aconteceu.

```


```vb
Private Sub Workbook_NewSheet(ByVal Sh As Object)
	
	'Move todas as novas planilhas para o final da pasta de trabalho
	Sh.Move After:=Sheets(Sheets.Count)
	
	'Move todas as novas planilhas para a primeira posição
	Sh.Move Before:=Sheets(1)
	
	'Adiciona as novas planilhas antes da planilha Ricardo
	Sh.Move Before:=Worksheets("Ricardo")
	
	'Adiciona as novas planilhas depois da planilha Ricardo
	Sh.Move After:=Worksheets("Ricardo")
	
End Sub
```
