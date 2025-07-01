Um DER é o desenho gráfico do Modelo Entidade Relacionamento que tem comno resultado as ligações entre tabelas e seus relacionamentos de forma mais prática e visual, melhorarando o fluxo de trabalho e a manutenção dos sistemas de banco de dados.
## Entidade
As entidades podem ser representadas por um retângulo. Uma entidade representa um objeto ou conceito do mundo real que possui uma existência independente e que pode ser identificado de forma única. Pode ser uma pessoa, lugar, evento ou qualquer coisa que você queira armazenar informações. **Exemplo**: Em um sistema de gerenciamento de biblioteca, entidades podem ser `Livro`, `Usuário`, `Empréstimo`.
## Relacionamento
Para representar os relacionamentos no DER, a figura utilizada é o losangulo. Um relacionamento descreve como duas ou mais entidades estão associadas entre si. Ele define a interação entre as entidades. **Exemplo**: No mesmo sistema de biblioteca, um relacionamento pode ser `Empréstimo`, que conecta as entidades `Livro` e `Usuário`.
## Cardinalidade
A cardinalidade especifica o número de instâncias de uma entidade que podem estar associadas a uma instância de outra entidade. Ela define a natureza do relacionamento em termos de quantidade.

- Relacionamento um para um (1 1);
	- Exemplo: Cada `Usuário` tem um `Cartão de Biblioteca`.

- Relacionamento um para n (1 n);
	- Um `Usuário` pode emprestar vários `Livros`

- Relacionamento n para n (n n);
	- Exemplo: Vários `Usuários` podem emprestar vários `Livros`.

## Exemplo
![[Pasted image 20241118172605.png]]