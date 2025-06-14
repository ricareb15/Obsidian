```gdscript
#include <stdio.h>  
#include <stdlib.h>  
int main() {  

int Num1, Num2, sub, som;  
printf("Digite o primeiro numero\n");  
scanf("%d\n", &Num1);  
  
printf("Digite o segundo numero\n");  
scanf("%d\n", &Num2);  
  
sub = Num2-(Num2-Num1);  
som = Num1+(Num2-Num1);  
  
printf("O primeiro numero se transforma em %d\n", sub);  
printf("O segundo numero se transforma em %d\n", som);  
system("pause");  
return 0;  
}
```