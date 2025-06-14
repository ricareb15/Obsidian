O objeto `Sheets` é extremamente poderoso para gerenciar várias planilhas em automações e macros. Ele funciona como uma porta de entrada para realizar praticamente qualquer tarefa com as folhas de uma pasta de trabalho.

### Propriedades
**Count**
Retorna o número total de planilhas e gráficos no workbook.
`MsgBox Sheets.Count`

**Item**
Você pode acessar uma planilha pelo índice ou pelo nome
`Sheets(1).Name = "Primeira Planilha"`

### Método
**Add**
Adiciona uma nova planilha ou gráfico.
`Sheets.Add After:=Sheets(Sheets.Count)` 'Adiciona ao final

**Delete**
Exclui uma ou mais planilhas.
`Sheets("Planilha3").Delete`

**Copy**
Copia uma planilha para um novo local ou workbook.
`Sheets("Planilha1").Copy After:=Sheets(Sheets.Count)`

**Move**
Move uma planilha para outro local ou workbook.
`Sheets("Planilha1").Move Before:=Sheets(1)`
