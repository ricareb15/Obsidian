### Operadores de Atribuição
Servem para atribuir valores a variáveis.

| Operadores | Descrição            | Exemplo | Resultado |
| :--------: | -------------------- | ------- | --------- |
|     =      | Atribui um valor     | A = 10  | A = 10    |
|     +=     | Incrementa e atribui | A += 2  | A = A + 2 |
|     -=     | Decrementa e atribui | A -= 2  | A = A - 2 |

---
### Operadores Aritméticos 
São usados para realizar cálculos matemáticos.

| Operador | Descrição     | Exemplo   |
| :------: | ------------- | --------- |
|    +     | Adição        | 3 + 2 = 5 |
|    -     | Subtração     | 5 - 3 = 2 |
|    *     | Multiplicação | 4 * 2 = 8 |
|    /     | Divisão       | 8 / 2 = 4 |
|    %     | Resto divisão | 8 % 3 = 2 |
|    *     | Exponenciação | 2 ^ 3 = 8 |
```ad-example
title: Exemplo
collapse: closed


```c
#include <stdio.h>  
int main() { 

int primeiroN;  
int segundoN;  
int conta;  
int numero;
int resto; 
  
printf("Digite o primeiro número: \n");  
scanf("%d",&primeiroN);  
  
printf("Digite o segundo número: \n");  
scanf("%d",&segundoN);  
  
printf("A soma é: %d\n", primeiroN + segundoN);  
  
printf("A subtração é: %d\n", primeiroN - segundoN);  
  
printf("A multiplicação é: %d\n", primeiroN * segundoN);  
  
printf("A divisão é: %d\n", primeiroN / segundoN); 

printf("Digite o numero: ");  
scanf("%d", &numero); 

resto=numero%2;  

printf("Resto divisao: %d\n", resto);  
system("Pause"); 

return 0
}
```

---
### Operadores relacionais 
| Operador | Descrição      | Exemplo |
| :------: | -------------- | ------- |
|    ==    | Igualdade      | A = B   |
|    <>    | Diferente      | A <> B  |
|    <     | Menor que      | A < B   |
|    >     | Maior que      | A > B   |
|    <=    | Menor ou igual | A <= B  |
|    >=    | Menor ou igual | A >= B  |
|    ≠     | Diferente      | A ≠ B   |

---
### Funções lógicas  
a E b são verdadeiros (&&)  
a OU b são verdadeiros (||)  
a É DIFERENTE DE b (!)

```c
#include <stdio.h>  
#include <stdbool.h>  
int main(void)  
{  
bool p=false, t=true  
printf("a: %d b: %d\n", p,t);  
printf("a && b %d\n", p&&t);  
printf("a||b %d\n", p||t);  
printf("!a %d\n", !p);  
}
```
(no caso, "false" = 0 & "true" = 1)

---
### Ordem de prioridade
1. **
2. * , / , //
3. %
4. + , -
5. Operadores lógicos

---
## [[Macros e VBA]]
### Operadores Aritméticos
São usados para realizar cálculos matemáticos.

| Operador | Descrição       | Exemplo     |
| :------: | --------------- | ----------- |
|    +     | Adição          | 3 + 2 = 5   |
|    -     | Subtração       | 5 - 3 = 2   |
|    *     | Multiplicação   | 4 * 2 = 8   |
|    /     | Divisão         | 8 / 2 = 4   |
|    \     | Divisão inteira | 8 \ 3 = 2   |
|   Mod    | Resto divisão   | 8 Mod 3 = 2 |
|    ^     | Exponenciação   | 2 ^ 3 = 8   |

---
### Operadores de comparação
Usados para comparar valores e retornar um resultado booleano `True` ou `False`

| Operador | Descrição      | Exemplo |
| -------- | -------------- | ------- |
| =        | Igualdade      | A = B   |
| <>       | Diferente      | A <> B  |
| <        | Menor que      | A < B   |
| >        | Maior que      | A > B   |
| <=       | Menor ou igual | A <= B  |
| >=       | Menor ou igual | A >= B  |

---
### Operadores lógicos
São usados para combinar ou inverter expressões booleanas.

| Operador | Descrição                             | Exemplo |
| -------- | ------------------------------------- | ------- |
| And      | `True` se ambas forem verdadeiras     | A And B |
| Or       | `True` se ao menos uma for verdadeira | A Or B  |
| Not      | Inverte o valor lógico                | Not A   |
| Xor      | `True` se somente uma for verdadeira  | A Xor B |

---
### Operadores de concatenação
Usados para unir cadeias de caracteres (strings).

| Operador |          Descrição          |     Exemplo     |
| :------: | :-------------------------: | :-------------: |
|    &     |        Concatenação         | "Olá" & "Mundo" |
|    +     | Concatenação<br>Alternativa |  "123" + "456"  |

---
### Operadores de Atribuição
Servem para atribuir valores a variáveis.

| Operadores | Descrição            | Exemplo | Resultado |
| :--------: | -------------------- | ------- | --------- |
|     =      | Atribui um valor     | A = 10  | A = 10    |
|     +=     | Incrementa e atribui | A += 2  | A = A + 2 |
|     -=     | Decrementa e atribui | A -= 2  | A = A - 2 |

## [[Power BI]]
### Operadores Aritméticos
São usados para realizar cálculos matemáticos.

| Operador | Descrição     | Exemplo                                                          |
| :------: | ------------- | ---------------------------------------------------------------- |
|    +     | Adição        | 1 [**nome da coluna**] = sheet[**coluna1**] + sheet**[coluna2**] |
|    -     | Subtração     | 1 [**nome da coluna**] = sheet[**coluna1**] + sheet**[coluna2**] |
|    *     | Multiplicação | 1 [**nome da coluna**] = sheet[**coluna1**] + sheet**[coluna2**] |
|    /     | Divisão       | 1 [**nome da coluna**] = sheet[**coluna1**] + sheet**[coluna2**] |


---
### Operadores de comparação
Usados para comparar valores e retornar um resultado booleano `True` ou `False`

| Operador | Descrição       | Exemplo                                                           |
| :------: | --------------- | ----------------------------------------------------------------- |
|    =     | Igualdade       | 1 [**nome da coluna**] = sheet[**coluna1**] = "**texto**"         |
|    <>    | Diferente       | 1 [**nome da coluna**] = sheet[**coluna1**] <> sheet**[coluna2**] |
|    <     | Menor que       | 1 [**nome da coluna**] = sheet[**coluna1**] < sheet**[coluna2**]  |
|    >     | Maior que       | 1 [**nome da coluna**] = sheet[**coluna1**] > sheet**[coluna2**]  |
|    <=    | Menor ou igual  | 1 [**nome da coluna**] = sheet[**coluna1**] <= sheet**[coluna2**] |
|    >=    | Menor ou igual  | 1 [**nome da coluna**] = sheet[**coluna1**] >= sheet**[coluna2**] |
|    ==    | Estrito igual a | 1 [**nome da coluna**] = sheet[**coluna1**] == sheet**[coluna2**] |

---
### Concatenação de Texto

| Operador | Descrição                                                      | Exemplo                                                          |
| :------: | -------------------------------------------------------------- | ---------------------------------------------------------------- |
|  **&**   | Use para unir ou concatenar duas ou mais cadeias de caracteres | 1 [**nome da coluna**] = sheet[**coluna1**] & sheet**[coluna2**] |

---
