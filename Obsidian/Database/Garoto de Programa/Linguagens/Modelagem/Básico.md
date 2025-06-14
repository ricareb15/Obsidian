Aqui vão algumas regras que são utilizadas por todos os tipos de diagramas

## Visibilidade dos Membros
Representamos a visibilidade dos atributos e operações e das operações usando os modificadores de acesso a seguir:
- + Público
- \# Protegido
- - Privado
- ~ Pacote
- / Derivado

## Relacionamentos entre Classes
Um relacionamento é uma conexão entre itens. Existem vários tipos de relacionamentos possíveis entre classes. Em que cada uma possui representações gráficas espec:

### Tipos de relacionamento
No Diagrama de Classes da UML, <mark style="background: #FFF3A3A6;">as classes se conectam</mark> através de diferentes tipos de relacionamentos. Isso mostra como os objetos interagem e se organizam dentro do sistema. 

As setas são a **navegabilidade**, que <mark style="background: #FFF3A3A6;">identifica o sentido em que as informações são transmitidas </mark>entre os objetos das classes relacionadas (relacionamento unidirecional). Contudo a navegabilidade <mark style="background: #FFF3A3A6;">não é obrigatória em um diagrama</mark> (relacionamento bidirecional) representado por uma linha (sem ponta)

Os principais tipos de relacionamento são:
#### Dependência
Uma classe precisa da outra para funcionar corretamente, mas <mark style="background: #BBFABBA6;">não há um vínculo forte</mark>.
Para fazer essa ilustração é utilizada seta com traço tracejada. Exemplo:
```ad-example
title: Exemplo
collapse: closed
`Classe A` depende da `classe B`

![[Pasted image 20250515123926.png]]

```

#### Associação
Relacionamento mais forte que a dependência, indica que a classe mantém uma referência a outra classe ao longo do tempo. As associações podem conectar mais de duas classes
```ad-example
title: Exemplo
collapse: closed
`Classe A` tem uma `Classe B`

![[Pasted image 20250515131234.png]]

```

#### Ternária
Esse é um tipo de associação em que <mark style="background: #BBFABBA6;">objetos de três classes se conectam entre si</mark>. Para representar esse ponto de conexão ou convergência entre as classes envolvidas, utilizamos um losango na notação do diagrama. Na prática, podemos ter associações `n-áreas` em que infinitas classes podem se associar por meio deste losango
```ad-example
title: Exemplo
collapse: closed

![[Pasted image 20250515131654.png]]

```

#### Agregação
Relacionamento mais específico do que a associação. Indica que uma classe é um contêiner (Departamento) ou uma coleção de outras classes. As classes  contidas não dependem do contêiner (Instrutor). Assim quando o contêiner é destruído, as classes continuam existindo
```ad-example
title: Exemplo
collapse: closed
- **Departamento** - Se caracteriza como contêiner pois além de poder estar ligada com a classe "Instrutor", ela também pode estar ligada com "Diretor", "Coordenadora", etc...

- **Instrutor** - Caso o departamento seja extinto o "Instrutor" continua exercendo sua função, e o mesmo acontexe com o classe do "Departamento"

`Classe A` possui uma `Classe B`
(apenas possui, e não "precisa")

![[Pasted image 20250515135441.png]]

```

#### Composição
Variação mais específica da agregação, este relacionamento indica uma dependência de ciclo de vida amis forte entre elas, em que quando um contêiner é destruído, seu conteúdo também é
```ad-example
title: Exemplo
collapse: closed
`Classe A` faz parte da `classe B`

![[Pasted image 20250515140510.png]]

```

#### Generalização / Especialização
Relacionamento entre itens gerais (superclasses / classes-mãe) e tipo mais específicos desses itens (subclasses/ classes-filha). Representando a herança entre as classes. Inclusive muitas das vezes a classe filha herda propriedades da classe mãe
```ad-example
title: Exemplo
collapse: closed
`Classe A` é um tipo de `Classe B`

![[Pasted image 20250515140916.png]]

```

#### Associativa
São produzidas quando ocorrem associações com multiplicidade muitos (\*) em todas as extremidades. No geral, existem atributos ("Atuação") da associação que não podem ser armazenadas em nenhuma das classes envolvidas ("Ator" e "Filme").
```ad-example
title: Exemplo
collapse: closed

![[Pasted image 20250515142044.png]]

```

### Multiplicidade
A multiplicidade é usada para determinar o <mark style="background: #FFF3A3A6;">número mínimo e o número máximo</mark> de objetos envolvidos na associação de cada lado, e também pode especificar o <mark style="background: #FFF3A3A6;">nível de dependência</mark>.
```ad-summary
title: Tabela
collapse: closed

| Multiplicidade | Significado                                                        |
| :------------: | ------------------------------------------------------------------ |
|     `0..1`     | **Opcional**: Numero mínimo e máximo na quantidade de objetos      |
|     `1..1`     | **Obrigatório**: Um objeto se relaciona com um da outra associada. |
|     `0..*`     | **Qualquer quantidade**: No mínimo um e no máximo muitos           |
|      `*`       | **Muitos**: Não se sabe ao certo a quantidade                      |
|     `1..7`     | **Exemplo**: No mínimo um deve se relacionar com apenas sete       |
|      `n`       | **Número fixo**: Deve haver exatamente "n" instâncias              |


```

Vale lembrar que não é obrigatório colocar multiplicidade no diagrama