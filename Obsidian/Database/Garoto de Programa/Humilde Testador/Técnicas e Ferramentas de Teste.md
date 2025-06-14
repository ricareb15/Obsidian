Ações com procedimento para chegar a um determinado resultado com foco na qualidade do software. Apoia testers e desenvolvedores para construir melhores testes. Ferramentas são aplicações que suportam as técnicas, e agilizam os testes durante todo o desenvolvimento do produto. Elas apoiam os profissionais que estão trabalhando na qualidade.

A combinação entre técnica e ferramenta permite que o preocesso de testes seja ágil e performático. Sendo necessário primeiro conhecer a técnica para depois identificar a ferramenta

## Qual testar primeiro?

- **Pergunta 1**
	Qual o grau de impacto se ocorrer indisponibilidade da funcionalidade?

- **Pergunta 2**
	Qual é a probabilidade de acontecer problemas na funcionalidade base do sistema?

- **Pergunta 3**
	Qual o prazo (urgência) que precisamos ou teremos para resolver se ocorrer um problema


### Heurísticas
"Processos que ocorrem naturalmente na mente do ser humano. Elas ajudam a solucionar problemas e tomar decisões em condições de incertezas, substituindo a forma complexa de fazer algo, por outra mais simples e ainda assim trazer resultados satisfatórios."
**~Gabriel Santos**

Fazendo um simples resumo, isso nada mais é do que extrair de um problema (algo complexo), soluções simples e aplicáveis que não resolvem totalmente o problema, mas contribuem na sua solução. Ao lavar o banheiro por exemplo, ao executar essa tarefa você não pensa em uma linha de produção complexa para lavar da forma mais rápida possível, apenas vai executando as pequenas tarefas até ter concluído totalmente o serviço.

#### Heurística ALTER FACE
Julio Lima por exemplo, trabalha com teste de qualidade de aplicações WEB e criou 7 princípios que o ajudam na hora de testar uma grande interface

- Ativação 
	Se os elementos que precisam de interação estão funcionando com êxito

- Layers
	Se elementos que subscrevem uns aos outros estão funcionando com êxito

- Timing
	Tempo necessário para executar as ações

- Princípio da exclusão
	Quando algum elemento da frente acaba subscrevendo outro de trás 

- Removível
	Quando algum objeto que deveria ser "fechável" não fecha

- Flutuante
	Quando o elemento não acompanha a barra de rolagem

- Alcançável
	Quando tenho vários elementos de uma lista, mas sua caixa de visão não cabe todos

- Colisão
	Quando os contêiners (por exemplo) colidem uns com os outros 

- Expansão

## Partição de equivalência & Análise do valor limite
As técnicas de partição de equivalência e análise do valor limite são fundamentais nos testes de qualidade de software, pois ajudam a reduzir o número de casos de teste sem comprometer a eficácia da verificação.
### Partição de Equivalência
Essa técnica consiste em <mark style="background: #FFF3A3A6;">dividir os dados de entrada do sistema em grupos ou partições</mark>, onde os valores dentro de cada grupo devem ser tratados de forma semelhante pelo software. A ideia é que, ao testar um valor de cada grupo, seja possível presumir que os demais valores desse mesmo grupo terão o mesmo comportamento. Isso reduz o número total de testes necessários sem perder cobertura.

Por exemplo, se um formulário exige que o usuário insira um número entre **1 e 100**, podemos definir três partições de equivalência:

- Números abaixo de 1 (**valores inválidos**)
- Números entre 1 e 100 (**valores válidos**)
- Números acima de 100 (**valores inválidos**)

Ao testar pelo menos um número de cada grupo, conseguimos validar o comportamento esperado sem precisar testar **todos** os valores possíveis

### Análise do Valor Limite
Essa técnica complementa a partição de equivalência e <mark style="background: #FFF3A3A6;">foca nos extremos das partições</mark>, já que erros costumam ocorrer nesses limites. Em vez de testar apenas valores dentro de uma faixa, a análise do valor limite se concentra nos pontos críticos.

Usando o mesmo exemplo do formulário com números de **1 a 100**, os valores a serem testados seriam:

- O menor valor válido (**1**)
- O maior valor válido (**100**)
- Um valor logo abaixo do limite inferior (**0**)
- Um valor logo acima do limite superior (**101**)

Testar esses valores ajuda a identificar falhas que podem ocorrer nos pontos de transição, como erros de comparação (`<=` em vez de `<`, por exemplo).

Ambas as técnicas são amplamente utilizadas em testes de software porque aumentam a eficiência dos testes e ajudam a encontrar falhas de forma mais rápida e sistemática. Você já aplicou alguma dessas técnicas em seus testes?

## Pairwise
A técnica pairwise, também conhecida como teste de pares, é um método de teste que busca <mark style="background: #FFB86CA6;">reduzir o número de combinações de testes sem comprometer a eficácia da verificação</mark>. Ela se baseia na ideia de que muitas falhas são causadas pela interação entre duas variáveis específicas, em vez de um conjunto mais amplo de fatores.

Quando um software tem várias **variáveis de entrada**, testar todas as combinações possíveis pode ser inviável devido ao grande volume de possibilidades. O Pairwise ajuda a otimizar isso, garantindo que todas as combinações possíveis de **pares de variáveis** sejam cobertas pelo menor número de testes possível.

A técnica **Pairwise** otimiza os testes, reduzindo o número de combinações necessárias para garantir a cobertura de todas as **duplas de variáveis**. A lógica por trás desse método é que a maioria dos defeitos surge da interação entre dois fatores, e não de múltiplas variáveis combinadas.
### Exemplo
- Suponha que temos duas variáveis
	- **Forma de pagamento**: Cartão, Boleto, Pix
	- **Tipo de conta**: Básica, Premium

- Sem Pairwise, teríamos **3 × 2 = 6** combinações possíveis:
	1. Cartão – Básica
	2. Cartão – Premium
	3. Boleto – Básica
	4. Boleto – Premium
	5. Pix – Básica
	6. Pix – Premium

- Com Pairwise, poderíamos otimizar para **apenas 3 testes**, garantindo que cada opção de pagamento e tipo de conta sejam testados em combinação ao menos uma vez:
	1. Cartão – Básica
	2. Boleto – Premium
	3. Pix – Premium

Essa lógica se aplica a sistemas mais complexos, garantindo eficiência e mantendo a cobertura de pares.

### [Ferramenta](https://github.com/robsonagapito/python-pairwise)
Projeto para ajudar na elaboração de projetos de testes utilizando a técnica de pairwise desenvolvida em Python
Aula: [Link](https://www.youtube.com/watch?v=iGnDMln-3No&ab_channel=4ALLTests)

## CRUD
A técnica **CRUD** é um princípio fundamental na qualidade e testes de software, focado nas operações essenciais de manipulação de dados. CRUD<mark style="background: #FFB86CA6;"> representa as quatro operações básicas de um sistema que interage com um banco de dados</mark>:

>**Create (Criar)** – Inserção de novos registros no banco de dados.
>**Read (Ler)** – Recuperação de dados existentes.
>**Update (Atualizar)** – Modificação de registros já armazenados.
>**Delete (Excluir)** – Remoção de registros do banco de dados.

A técnica CRUD é usada para garantir que essas operações básicas funcionem corretamente, sejam seguras e estejam alinhadas aos requisitos do sistema. Para validar a qualidade do CRUD, os testes podem envolver:

✔ **Testes Funcionais**
	Verificam se cada operação (criação, leitura, atualização e exclusão) está sendo executada corretamente.  
✔ **Testes de Integridade dos Dados** 
	Garantem que a inserção, alteração e remoção de informações não causem inconsistências no banco.  
✔ **Testes de Segurança**
	Avaliam se apenas usuários autorizados conseguem executar operações CRUD, evitando falhas como exclusão indevida de dados.  
✔ **Testes de Performance** 
	Checam a eficiência da leitura e escrita de dados, garantindo tempos de resposta adequados.  
✔ **Testes de Regressão** 
	Asseguram que mudanças no código não afetam negativamente as operações CRUD.

Essa técnica é amplamente aplicada em sistemas que dependem de bancos de dados, garantindo a confiabilidade das informações e a experiência do usuário.