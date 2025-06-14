---
aliases:
  - Application
---
Os objetos de "**Alta Hieraquia**" no VBA pode interagir e modificar comandos de várias categorias. Ele atua como um "supervisor" global, ajustando configurações ou controlando o comportamento do ambiente do aplicativo.

## Aplication
O objeto `Application` no VBA pode interagir e modificar comandos de várias categorias que mencionei anteriormente. Ele atua como um "supervisor" global, ajustando configurações ou controlando o comportamento do ambiente do aplicativo.

### [[Application - Interação com o Usuário]]
>`Application.UserName` - Para exibir ou modificar o nome do usuário.
>`Application.DisplayAlerts` - Para suprimir ou exibir alertas

### [[Application - Manipulação de Objetos]]
Propriedades e métodos que interagem diretamente com elementos do ambiente, como pastas de trabalho, planilhas, intervalos, gráficos, etc.
>`Application.Workbooks`
>`Application.ActiveSheet`
>`Application.Charts`

### [[Application - Manipulação de Dados]]
Métodos que manipulam ou auxiliam no processamento de informações, como cálculos e funções.
>`Application.WorksheetFunction` – Para usar funções nativas do Excel no VBA.
>`Application.Calculation` – Para controlar o cálculo manual ou automático.

### [[Application - Controle de Interface]]
Propriedades que ajustam a aparência ou estado do aplicativo.
>`Application.WindowState` – Para maximizar, minimizar ou restaurar a janela.
>`Application.ScreenUpdating` – Para ativar ou desativar a atualização da tela 
>(melhorando o desempenho.)

### [[Application - Controle de Fluxo e Erros]]
Métodos usados para informar o progresso ou capturar informações durante a execução de Macro.
>`Application.StatusBar` – Para exibir mensagens de status.
>`Application.OnTime` – Para agendar a execução de uma macro.

### [[Application - Automação e Execução]]
Propriedades e métodos usados para executar macros ou controlar funcionalidades de alto nível.
>`Application.Run` – Para chamar outras macros.
>`Application.Quit` – Para fechar o aplicativo.

Será q atualiza?
