**O Power Pivot** é uma tecnologia de modelagem de dados que permite criar modelos de dados, estabelecer relações e criar cálculos. Com o Power Pivot, você pode trabalhar com grandes conjuntos de dados, criar relações extensas e criar cálculos complexos (ou simples), tudo em um ambiente de alto desempenho e tudo dentro da experiência familiar do Excel.

### Como Habilitar?
Siga o passo a passo a seguir para habilitar o power pivot no seu Excel:

1. Arquivo
2. Opções
3. Suplementos
4. (Na caixa de seleção na parte inferior)
5. Selecionar "Suplementos COM"
6. Clicar em "Ir"
7. Selecionar a opção do Power Pivot
8. Clicar em "OK"

### Relacionamentos
Neste caso o relacionamento será necessário para fazermos meio que um PROCV entre as guias. Exemplo: Guia Produto & Guia Venda.

No Excel, poderiamos fazer normalmente uma multiplicação entre: 
_valor unitário + qnt_vendas = valor_total_.  
Mas ao invés disso, podemos usar uma ferramenta muito importante do Power Pivot que são os seus relacionamento.
Para fazer um relacionamento é muito simples:

1. Já dentro do Power Pivot
2. Vá em "Exibição do diagrama"
3. Percebe-se que as guias estrão divididas em quagrados no diagrama
4. Puxe uma linha entre as colunas que deseja fazer o relacionamento

Após fazer o relacionamento, voltamos para a exibição padrão ("Exibição do diagrama" para "Exibir dados) para que assim, possamos separar uma coluna que recebera o resultado desse relacionamento e fará o cálculo do total das vendas da seguinte forma:

1. Selecionar coluna
2. No campo de fórmula escreva...
3. =RELATED(==Coluna da outra tabela com valores do produto==) * Quantidade(==Na própria tabela==)

### Problemas

#### Itens Conjuntos (Tabela Dinâmica)
Análise o seguinte problema: 
Você tem em suas mãos, uma tabela dinâmica feita pelo Power Pivot que possui a quantidade de vendas feitas de cada produto por cada vendedor
![[Pasted image 20250218174723.png]]

**Após uma conversa com o chefe, quantos fogões foram vendidos por ano, por cada vendedor**

Solução:
 1. Clique em "Análise de Tabela Dinâmica"
 2. Clieque em "Campos, Itens e Conjuntos"
 3. "Cria conjunto a partir de itens da coluna"
 4. Dê um nome para o conjunto (Fogão)
 5. Exclua os outros itens desnecessários
 6. Deixe apenas os anos em sequência (2024; 25; 26; ...)

![[Pasted image 20250218175440.png]]

Resultado:
![[Pasted image 20250218175523.png]]

![[Problema - Itens Conjuntos.xlsx]]
### Fontes
Para dar uma revisada assita a esse [Vídeo do YouTube](https://youtu.be/ZHvtU7j52dM?si=HxzGdZtAyHT6dJW7)
>Medidas
>KPIs
>Funções

### Não aprendi
Funções
>CALCULATE
>SUM
>SUMX
>CONTAINS
>ISBLANK
>IF
>ISEVEN