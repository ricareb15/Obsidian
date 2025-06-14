Na UML (Unified Modeling Language), os diagramas são divididos em **estruturais** e **comportamentais**, cada um servindo para representar aspectos diferentes de um sistema. Vamos explorar os dois tipos:
## Estruturais
Eles descrevem a organização estática de um sistema, incluindo classes, objetos, componentes e suas relações. Os principais são:
### Diagrama de Classes
O diagrama de classes da UML é <mark style="background: #FFF3A3A6;">utilizado para descrever a estrutura estática</mark> das **classes**, **métodos**, **atributos** e **relações** de um sistema. Basicamente esse tipo de diagrama descreve detalhadamente o que deve estar presente em um sistema em que você esta desenvolvendo
```ad-info
collapse: closed

- **Classe = Ser Humano**
	A classe é como um modelo que define como os objetos serão criados. No nosso caso, vamos chamar a classe de **Pessoa**, que representa qualquer ser humano.

---

- **Atributos = Características da Pessoa**
	Os atributos são as informações que cada pessoa tem. Alguns exemplos:
	
	- Nome
	- Idade
	- Altura
	- Gênero
	
	Cada indivíduo tem suas próprias características, mas todos compartilham esses atributos.

---

- **Métodos = Ações da Pessoa**
	Os métodos são as ações que uma pessoa pode realizar. Alguns exemplos:
	
	- comer( → A pessoa se alimenta.
	- falar() → A pessoa conversa.
	- andar() → A pessoa caminha.
	- trabalhar() → A pessoa realiza um trabalho.

---

- **Objeto da Classe (Instância)**
	É quando estamos tratando de um objeto específico dessa classe
	
	- Nome (Maria, João, Ana…),
	- Idade (25 anos, 30 anos…),
	- Altura (1,75m, 1,80m…),
	- Gênero (Masculino, Feminino…).


```

Esse é um dos diagramas <mark style="background: #FFF3A3A6;">mais importantes e populares</mark> da UML. Além disso, o diagrama de classes serve de base para a criação de outros diagramas mais complexos. Por isso, é fundamental que você aprenda a criar diagramas de classes, pois isso facilitará, futuramente, o desenvolvimento de diagramas mais avançados.

#### Representação
Representamos uma classe usando um diagrama <mark style="background: #BBFABBA6;">dividido em três</mark> compartimentos:

- **Nome** - Inclui o nome e o estereótipo da classe
- **Atributos** - Lista de atributos da classe no formato: `nome:tipo` ou `nome:tipo=valor`
- **Operações** - Lista de métodos da classe no formato: `método(parametros): tipo_retorno`

![[Pasted image 20250515122506.png]]


## Comportamentais
Esses diagramas mostram a dinâmica do sistema, incluindo interações e mudanças ao longo do tempo. Os principais são: