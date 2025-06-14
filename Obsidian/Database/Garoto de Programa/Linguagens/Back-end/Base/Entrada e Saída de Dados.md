---
aliases:
  - Sequencia de Scape
cssclasses:
---

Os programas de computador são sistemas que processam dados. A tarefa de um programa de computador é receber dados, processar essas informações e entregar esses dados processados.
## [[Linguagem C]]
#### Especificadores de formato
O especificadores de formato são utilizados nas funções de entrada e saída em C, como printf e scanf, para lidar com as diversas especificações existentes. Podendo então, formatar a saída, e interpretar a entrada de dados. Exemplos são:

```gdscript
%d - para números inteiros  
%f - para números de ponto flutuante (com casas decimais)  
%lf- para números de ponto flutuante duplamente precisos (double)  
%c - para caracteres  
%s - para sequência de caracteres
```
---
#### Printf
Esta função escreve na tela o texto existente em seus parenteses  
#### Sequência de Scap
\a - Toca um bipe (alarme sonoro padrão do sistema)
\b - Backspace (tab invertido)
\n - Quebra linha
\t - Tabulação horizontal (pular um certo conteúdo)
\r - Retorna ao início da linha
\0 - Caractere nulo (Fim)
\y - Tabulação vertical (pular um número de linhas)

É como se o Scap substituisse o que vem após a vírgula
```c
printf("Oi, tudo bem? tenho 6 anos e programo.\n")

printf("Valor inteiro: %d.\n", 10)
printf("Valor real: %f.\n", 3.141516)
printf("Valor real com apenas duas casas: %.2f.\n", 3.14)
printf("Valor inteiro: %d.\n", 10)
printf("Dados de texto: %s.\n", testando)
```
---
#### Scanf
O `scanf` é uma função da linguagem de programação C utilizada para ler dados de entrada a partir do teclado (ou de outras fontes de entrada padrão). A função `scanf` lê a entrada do usuário e a armazena em variáveis conforme o formato especificado.
```c
int main() { 

int idade; 
float altura; 
char nome; 

// Lê um inteiro, um float e uma string do teclado 
printf("Digite sua idade: "); 
scanf("%d", &idade); 
printf("Digite sua altura em metros: "); 
scanf("%f", &altura); printf("Digite seu nome: "); 
scanf("%s", nome); 

// Exibe os valores lidos 
printf("Idade: %d\n", idade); 
printf("Altura: %.2f\n", altura); 
printf("Nome: %s\n", nome); 

return 0; }
```
---
## [[Linguagem Python]]
A entrada e saída de dados em Python são essenciais para a comunicação entre o programa e o usuário, além da manipulação de arquivos e interações com outras fontes de dados.

### Entrada de Dados
Python permite diversas formas de entrada de dados, dependendo do contexto e da necessidade do programa. Aqui estão algumas das mais comuns
>Entrada via teclado
>Entrada via arquivos
>Entrada via banco de dados
>Entrada via API (requisição WEB)

#### Entrada via teclado
Esse tipo de entrada é realizada pelo usuário via teclado utilizando a instrução **"input()"**. Essa função suspende o fluxo de execução do programa e aguarda que o usuário digite um valor no console, juntamente com o **prompt** que é uma mensagem opcional que aparece na tela antes do usuário digitar algo. Exemplo:
```python
nome = input("Digite seu nome: ")
print("Olá,", nome)
```

#### Entrada via arquivos
A manipulação de dados em Python é uma das tarefas mais comuns e poderosas da linguagem, especialmente em ciência de dados, análise estatística e automação de processos. Python oferece diversas bibliotecas para facilitar essa tarefa, tornando a manipulação de dados eficiente e intuitiva


### Saída de Dados
A saída de dados permite exibir informações ao usuário ou registrar resultados.


**Saída de dados**
As mensagens dirigidas ao usuário (que serão apresentadas durante e ao final do processamento) utilizam o comando **"print"**. Nessa função, podemos usar o parâmetro `sep` (abreviação de "separator") que controla o texto que será usado para separar os valores exibidos. Por padrão, o valor de `sep` é um espaço (`' '`), mas podemos definilo fazendo da seguinte forma

```python
print("maçã", "banana", "laranja")
print("maçã", "banana", "laranja", sep=",")

#Saída 1:
maçã banana laranja

#Saída 2:
maçã,banana,laranja

```

#### Sequência de escape
A função print() possui códigos especiais, chamados sequência de escape, que são combinações de caracteres iniciadas com o sinal de barra invertida (\\) e algum outro caractere. Segue as principais combinações de caracteres:

| Sequência | Descrição                                                                         |
| --------- | --------------------------------------------------------------------------------- |
| \n        | Quebra de linha                                                                   |
| \t        | Insere uma tabulação (geralmente equivale a 4 ou 8 espaços).                      |
| \b        | Remove o caractere anterior na string (equivalente a apertar "Backspace").        |
| \v        | Insere uma tabulação vertical, que pode variar dependendo do sistema de exibição. |
| \\"       | Insere uma aspa dupla em uma string (o mesmo serve para aspa simples).            |
| \\\       | Insere uma barra invertida (`\`) na string.                                       |
| \0        | Caractere nulo                                                                    |
| \a        | Beep de alerta                                                                    |

```python
#Quebra de linha (\n)
print("Primeira linha\nSegunda linha") #Saída:
Primeira linha
Segunda linha

#Tabulação (\t)
print("Nome:\tMaria") #Saída:
Nome: Maria

#Backspace (\b)
print("Olá, Mund\bdo") #Saída: 
Olá, Mundo

#Aspas duplas (\")
print("Ele disse: \"Olá!\"") #Saída:
Ele disse: "Olá!"

#Barra invertida (`\\`)
print("Caminho do arquivo: C:\\Users\\Maria") #Saída:
Caminho do arquivo: C:\Users\Maria

#Tabulação vertical (`\v`)
print("Linha 1\vLinha 2") #Saída pode variar, mas geralmente é:
Linha 1
	Linha 2
```
## [[JavaScript]]

#### Id
Saída de dados Por "id"  
document.getElementById("id").innerHTML = "Meu primeiro texto<b>JS</b>";  
Dessa forma ele vai escrever um texto usando um id para formatação  
getElementById - Para mencionar um id do HTML  
innerHTML - "imprimir no html"  
#### Write
Pela função de escrita  
document.write("Texto aleatório");  
#### Alert
Pela função alert  
alert(Alguma coisa);  
#### Log
Pelo log  
console.log("Como se fosse um alert só que mais silencioso ")

## [[Macros e VBA]]

**Entrada de Dados**
A entrada de dados é feita via teclado pelo usuário por meio de uma box de texto. Essa função suspende o fluxo de execução do programa e aguarda que o usuário digite um valor na box. 
Para fazer uma box de input é necessário usar o comando: **InputBox("Descrição")** que deve ser atribuido a uma variável. Segue um exemplo:
```vb
Variavel = InputBox("Descrição")
```
