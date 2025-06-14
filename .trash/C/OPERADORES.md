### Operadores
Atribuição (=)  
  
Aritméticos  
Soma (+)  
Subtração (-)  
Multiplicação (*)  
Divisão (/)  
Módulo (%)
(resto da divisão)
[[Adc; Sub; Div; Mult; %]]

Lógicos  
a == b Avalia se a é realmente igual a b  
a > b Avalia se a é maior que b  
a < b Avalia se a é menor que b  
a >= b Avalia se a é maior ou igual a b  
a <= b Avalia se a é menor ou igual a b  
  
Funções lógicas  
a E b são verdadeiros (&&)  
a OU b são verdadeiros (||)  
a É DIFERENTE DE b (!)

```gdscript
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