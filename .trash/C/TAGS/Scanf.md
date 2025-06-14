Linguagem: #C 
Assunto: #tags 

O `scanf` é uma função da linguagem de programação C utilizada para ler dados de entrada a partir do teclado (ou de outras fontes de entrada padrão). A função `scanf` lê a entrada do usuário e a armazena em variáveis conforme o formato especificado.

```gdscript
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