## Application.WindowState
O **Application.WindowState** em VBA é uma propriedade útil que permite controlar o estado da janela do Excel. Essa propriedade pode ser usada para maximizar, minimizar ou restaurar a janela principal do aplicativo.

O **Application.WindowState** pode assumir três valores principais, que são definidos pela enumeração `XlWindowState`:

- `xlNormal` (Valor: 0) A janela está no estado "normal" (restaurada), ou seja, nem maximizada nem manimizada.

- `xlMinimized` (Valor: 2) A janela do Excel está minimizada.

- `xlMaximized` (Valor: -4137) A janela do Excel está maximizada.

```vb
Application.WindowState = xlNormal 'Normal
Application.WindowState = xlMinimized 'Maximizar
Application.WindowState = xlMaximized 'Minimizar
```