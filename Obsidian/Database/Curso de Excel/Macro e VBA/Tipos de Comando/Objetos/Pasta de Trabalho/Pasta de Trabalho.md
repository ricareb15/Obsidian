## [[Workbook]]
O objeto **Workbook** em VBA é extremamente versátil, permitindo que você automatize tarefas no Excel e manipule pastas de trabalho de várias formas.

Um detalhe desse tipo de objeto é que ele não é definido em uma "Macro" pois não é algo que é desativado ou ativado com o tempo mas sim integrada ao arquivo

### Abertura e Fechamento
`Workbook_Open`
Executar código automaticamente quando um arquivo é aberto

`Workbook_BeforeClose`
Executado antes de a pasta de trabalho ser fechada 
(permite cancelar o fechamento).

`Workbook_AfterSave`
Acionado após a pasta ser salva.

`Workbook_BeforeSave`
Executado antes de a pasta ser salva 
(permite cancelar o salvamento).

### Alteração de Foco
`Workbook_Deactivate`
Desativa a plhanilha quando o usuário muda para outra
pasta de trabalho ou aplicativo no Excel

`Workbook_Active`
Acionado quando a pasta de trabalho se torna ativa


Worksheet
- Representa uma planilha dentro de um workbook. Exemplo: `Sheets("Sheet1")`, `ActiveSheet`
- Propriedades: `Name`, `Cells`, `Range`, `UsedRange`
- Métodos: `Activate`, `Delete`, `Copy`