## Manipulação de Números
Estas funções ajudam em cálculos matemáticos e transformações numéricas

`Abs` - Retorna o valor absoluto de um número
```vb
MsgBox Abs(-5) 'Resultado: 5
```

---

`Sqr` - Retorna a raiz quadrada
```vb
MsgBox Sqr(16) 'Resultado: 4
```

---

`Round` - Arredonda um número para um número específico de casas decimais
```vb
MsgBox Round(3.14159, 2) 'Resultado: 3.14
```

---

`Int` - Retorna apenas a parte inteira do número.
```vb
MsgBox Int(3.9) 'Resultado: 3
```

---

`Fix` - Similar ao `Int` , mas lida de maneira diferente com números negativos.
```vb
MsgBox Fix(-3.9) 'Resultado: -3
```

---

 - Gera um número aleatório entre 0 e 10

## Manipulação de Texto

`Left` - Para obter uma parte de uma cadeia de caracteres (string), começando do lado esquerdo 
```vb
Left(string, length)
```
`string` - A cadeia de caracteres da qual você quer extrair parte do texto
`length` - O número de caracteres que você deseja pegar, começando da esquerda

---

`Right` - Extrai caracteres do final (direita) de uma string
```vb
Right(string, length)
```
`string` - A cadeia de caracteres da qual você quer extrair parte do texto
`length` - O número de caracteres que você deseja pegar, começando da esquerda

---

`Mid` - Extrai caracteres de qualquer posição na string, começando por onde você especifica
```vb
Mid(string, start, [length])
```
`string` - A cadeia de caracteres da qual você quer extrair parte do texto
`start` - A posição inicial (baseada em 1).
`length` - O número de caracteres que você deseja pegar, começando da esquerda

---

`Len` - Obtém o comprimento total (número de caracteres) de uma string
```vb
Len(string)
```

---

`Split` - Quebra o texto a partir de um delimitador expecíficado. Em seguida, você pode atribuir as partes deste texto á uma variável
```vb
Split(string, delimitador)

'Exemplo
Nome = Split(nomeCompleto, " ")
Nome(1) 'Resultado: Ricardo
Nome(2) 'Resultado: Lima
Nome(3) 'Resultado: de
Nome(4) 'Resultado: Souza
```

`InStr` - Usada para localizar a posição de um caractere ou conjunto de caracteres em um texto
```vb
InStr([start], string1, string2, [compare])
```

**"start"** (opcional): A posição inicial para a pesquisa (padrão é 1).
**"string1"**: A string principal onde a pesquisa será feita.
**"string2"**: A substring que você está procurando. (até onde)
**compare**  (opcional): Determina o tipo de comparação (binária ou textual).

```ad-example
collapse: closed

```vb
A1 = Ricardo Lima

InStr(1, Range(A1).value, " ") 
'Resultado: Posição do primeiro espaço
```


