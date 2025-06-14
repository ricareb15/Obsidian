## Propriedades
As propriedades permitem acessar ou modificar características e conteúdos de um intervalo de células. Aqui estão as mais utilizadas:

### Dados e conteúdo
`Value` Retorna ou define o valor contido no intervalo.
```vb
Range("A1").Value = "Teste"
```

`Text` Retorna o texto visível na célula (o que é exibido na planilha).
```vb
MsgBox Range("A1").Text
```

`Formula` Retorna ou define a fórmula contida no intervalo.
```vb
Range("A1").Formula = "=SOMA(B1:B10)"
```

---
### Aparência e Formatação:
`Font` Manipula características da fonte (como tamanho, cor e estilo).
```vb
Range("A1").Font.Bold = True
```
>`Bold` - Determina se o texto é em negrito
>`Italic` - Define se o texto está em itálico
>`Name` - Especifica o nome da fonte (ex.: "Arial")
>`Size` - Determina o tamanho da fonte
>`Color` - Especifica a cor da fonte

`Interior` Define a cor de fundo da célula.
```vb
Range("A1").Interior.Color = RGB(255, 0, 0) ' Vermelho
```

---
### Estrutura do Intervalo:

`Rows` **/** `Columns` Retorna os objetos de linhas ou colunas do intervalo.
```vb
MsgBox Range("A1:A10").Rows.Count 'Conta o número de linhas
```

`EntireRow` **/** `EntireColumn`: Referencia a linha ou coluna inteira de um intervalo.
```vb
Range("A1").EntireRow.Delete
```

`Address` Retorna o endereço do intervalo.
```vb
MsgBox Range("A1").Address
```

`End` Move até o último valor ou célula contígua em uma direção.
```vb
Range("A1").End(xlDown).Select
```

---

## Metodos
Os métodos permitem realizar ações específicas no intervalo de células. Aqui estão os principais:

#### Manipulação de Dados e Células

`Clear` **/** `ClearContents` **/** `ClearFormats`:
Limpa valores, conteúdo ou formatação de células.
```vb
Range("A1").ClearContents
```


`Copy` **/** `PasteSpecial` **/** `Cut`:
Realiza ações de cópia, colagem especial ou recorte.
```vb
Range("A1").Copy Destination:=Range("B1")
```


`Delete`: Exclui células ou intervalos.
```vb
Range("A1").Delete
```


`Insert`: Insere novas células ou intervalos.
```vb
Range("A1").Insert Shift:=xlDown
```

---
#### Navegação e Seleção

`Select`: Seleciona o intervalo.
```vb
Range("A1").Select
```

`Activate`: Ativa a célula específica.
```vb
Range("B1").Activate
```

**`End`**  Move para a última célula na direção especificada (como pressionar **Ctrl + seta** no Excel). Você pode usar direções como `xlDown`, `xlUp`, `xlToLeft`, `xlToRight`.
```vb
Exemplo: `Range("A2").End(xlDown)`
```

**`Offset`**  
Retorna um intervalo deslocado em relação ao intervalo original.

```vb
Range("A1").Offset(1, 0) 'Desloca para uma célula abaixo
```



---
#### Cálculos e Fórmulas

- `Calculate`: Recalcula as fórmulas no intervalo.
```vb
Range("A1:B10").Calculate
```

---
#### Pesquisa e Substituição

`Find`: Procura por um valor no intervalo.
```vb
Dim cel As Range
Set cel = Range("A1:A10").Find("ValorProcurado")
If Not cel Is Nothing Then MsgBox cel.Address
```

`
`Replace`: Substitui valores no intervalo.
```vb
Range("A1:A10").Replace What:="Antigo", Replacement:="Novo"
```

---
#### Mesclagem e Desmesclagem

`Merge`: Mescla um intervalo de células em uma única célula.
```vb
Range("A1:B2").Merge
```

**`UnMerge`**: Desfaz a mesclagem de células.
```vb
Range("A1:B2").UnMerge
```
