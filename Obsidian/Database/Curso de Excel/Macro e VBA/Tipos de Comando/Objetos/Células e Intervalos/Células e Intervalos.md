## Range
Este objeto representa uma ou mais células em uma planilha.
Exemplo: `Range("A1:B2")`, `Cells(1, 1)`

### [[Propriedades & Métodos (Range)]]
No objeto `Range` do VBA, existem diversas **propriedades** e **métodos** que podem ser usados para manipular células, intervalos e os dados contidos neles. 
#### Propriedades
Características – Exemplo a cor, a idade e o peso da vaca

**Dados e Conteúdo**
	`Value` -  Retorna ou define o valor contido no intervalo.
	`Text` Retorna o texto visível na célula (o que é exibido na planilha).
	`Formula` Retorna ou define a fórmula contida no intervalo.

**Aparência e Formatação**
	`Font` Manipula características da fonte (como tamanho, cor e estilo).
	`Interior` Define a cor de fundo da célula.

**Estrutura do Intervalo**
	`Rows` **/** `Columns` Retorna os objetos de linhas ou colunas do intervalo.
	`EntireRow` **/** `EntireColumn`: Referencia a linha ou coluna inteira de um intervalo.
	`Address` Retorna o endereço do intervalo.
	`End` Move até o último valor ou célula contígua em uma direção.

#### Métodos
Métodos (ações) – Exemplo comer, dormir e mugir.

**Manipulação de Dados e Células**
	`Clear` **/** `ClearContents` **/** `ClearFormats`: Limpa valores, conteúdo ou formatação de células.
	`Copy` **/** `PasteSpecial` **/** `Cut`: Realiza ações de cópia, colagem especial ou recorte.
	`Delete`: Exclui células ou intervalos.
	`Insert`: Insere novas células ou intervalos.


**Navegação e Seleção**
	`Select`: Seleciona o intervalo.
	`Activate`: Ativa a célula específica.
	**`End`**: Como pressionar **Ctrl + seta** no Excel.
	**`Offset`**: Faz um deslocamento de célula em relação ao original


**Cálculos e Fórmulas**
	`Calculate`: Recalcula as fórmulas no intervalo.


**Pesquisa e Substituição**
	`Find`: Procura por um valor no intervalo.
	`Replace`: Substitui valores no intervalo.

**Mesclagem e Desmesclagem**
	`Merge`: Mescla um intervalo de células em uma única célula.
	**`UnMerge`**: Desfaz a mesclagem de células.

## Cells
Pode usar quase todas as propriedades e métodos do `Range`, porque ele é, na verdade, uma forma de acessar um intervalo de uma única célula (ou um conjunto de células) dentro de uma planilha.
Por exemplo:

```vb
Range("A1").Value = "Olá" ' Usando Range diretamente
Cells(1, 1).Value = "Olá" ' Usando Cells (linha 1, coluna 1)
```
Ambos os comandos acima fazem a mesma coisa! 

O `Cells` é usado para acessar **uma única célula** ou para referenciar células por **números de linha e coluna**. A principal vantagem do `Cells` é trabalhar em loops ou acessos dinâmicos, onde você pode especificar as coordenadas (linha e coluna) numericamente.

O `Range` é mais versátil, pois permite trabalhar com **intervalos específicos**, incluindo múltiplas células ou intervalos nomeados. Ele também aceita endereços diretos, como `"A1:B3"`.

## ActiveCell
É um tipo de **objeto Range** que se refere à célula que está atualmente selecionada ou ativa em uma planilha. O **`ActiveCell`** é um subconjunto do **`Range`**, que é um dos objetos mais comuns em VBA

Também temos outros objetos que fazem esse tipo de referência:

**ActiveSheet**
O **`ActiveSheet`** é um objeto que faz referência à planilha que está atualmente ativa no Excel. Embora não seja um **objeto de célula**, ele é útil quando você quer interagir com a planilha ativa de uma maneira geral, e não com células específicas.
```vb
ActiveSheet.Range("A1").Value 'Acessa a célula A1 na planilha ativa.
```


**ActiveWorkbook**:
O **`ActiveWorkbook`** é o objeto que faz referência ao **livro de trabalho (workbook)** que está atualmente ativo no Excel. Semelhante ao **`ActiveSheet`**, mas no nível do livro de trabalho.
```vb
ActiveWorkbook.Sheets("Sheet1").Range("A1").Value
'Acessa a célula A1 na planilha "Sheet1" do livro de trabalho ativo.
```

## Rows e Columns
Embora **`Rows`** e **`Columns`** não sejam objetos diretamente relacionados a células, eles podem ser usados para referenciar intervalos de células em linhas ou colunas específicas.
```vb
Rows(1) 'Faz referência à primeira linha.
Columns("A") 'Faz referência à coluna A.
```


## UsedRange
O **`UsedRange`** é um objeto de intervalo que se refere ao conjunto de células usadas (preenchidas) em uma planilha. Ele é útil para identificar automaticamente a área de dados em uma planilha.
```vb
ActiveSheet.UsedRange 'Retorna todas as células usadas na planilha ativa.
```


# Diferenças importantes
- **`ActiveCell`** é sempre uma célula única e refere-se à célula que está atualmente selecionada na planilha.
- **`Range`** pode se referir a qualquer intervalo de células e não depende da seleção ou da célula ativa.
- **`Cells`** oferece uma maneira de referenciar células usando índices numéricos de linha e coluna, ao invés de referências de célula tradicionais (como "A1").