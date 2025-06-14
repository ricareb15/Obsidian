### Fórmula do Excel
As formulas que vamos utilizar no Excel vão ser: 
##### **=CÉL("lin")=LIN()**
- A função `CÉL("lin")` retorna o número da linha da célula ativa (ou seja, a célula onde o cursor está no momento).
- A função `LIN()` retorna o número da linha da célula onde a fórmula está escrita.
- Quando você usa essa fórmula, ela verifica se a linha da célula ativa é a mesma linha onde a fórmula está localizada.
- Resultado: `VERDADEIRO` se as linhas forem iguais, ou `FALSO` se forem diferentes.

##### **=CÉL("col")=COL( )**
- A função `CÉL("col")` retorna o número da coluna da célula ativa.
- A função `COL()` retorna o número da coluna da célula onde a fórmula está escrita.
- Similar ao exemplo anterior, essa fórmula verifica se a coluna ativa é a mesma coluna da fórmula.
- Resultado: `VERDADEIRO` se as colunas forem iguais, ou `FALSO` se forem diferentes.


### Fórmula do VBA
```vb
If application.CutCopyMode = False Then 
	Application.Calculate 
End If 
```

O problema com das fórmula do Excel, é que ela depende de um cálculo dinâmico da função `CÉL("lin")` para retornar o número correto da linha ativa. No entanto, essa fórmula pode não ser recalculada automaticamente em todas as situações, especialmente se houver algum evento, como copiar ou colar, que interfira no estado do Excel.

O trecho de código VBA que você forneceu é útil porque força o Excel a recalcular a planilha apenas quando o modo de corte ou cópia (`CutCopyMode`) está desativado. O comando `Application.Calculate` força um novo cálculo de todas as fórmulas na planilha, garantindo que `CÉL("lin")` seja atualizado corretamente.

### Formatação Condicional
Agora, para que hája a tal mudança de cores é necessário usar a formatação condional:
1. É necessário fazer duas formatações condionais (pra coluna e linha)
2. Selecione toda a área que deseja receber a formatação (tabela)
3. Em "Usar uma fórmula para determinar..." cole as fórmulas