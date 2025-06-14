
```gdscript
#include <stdio.h>
#include <stdlib.h>
Int main () 
{
}
return(0)
```

Linha 1 & 2 - # include <stdio.h>  
Diz ao computador para usarmos as bibliotecas <stdio.h> e <stdlib.h>. Neste arquivo existem declarações de funções úteis para entrada e saída de dados. Está biblioteca já pronta, permite que o programador envoque propriedades/comandos que são utilizados para mostrar ao usuário "o que está acontecendo no programa"

Linha 3 - Int main () {código}
Todos os programas em C precisam dessa declaração.
Caso você trabalhe com números no código é preciso da declaração de retorno (exp: "return=0").  
Caso contrário (não utilizar números) é preciso usar o "Int main (void)" na linha 2

Linha 4 - system("pause")
Para que se possa usar uma pausa após o programa terminar de ser executado é preciso usar a função "system("Pause");"  
Junto da biblioteca: # include <stdlib.h>  
Porém, isso cria uma vulnerabilidade no seu código. Motivo? Não sei

Linha 5 - return(0)
### Dicas
- Todas as linhas escritas devem ser finalizadas com ";"  
- Comentários são feitos com /* Exemplo 1 */ ou //Exemplo 2  
- "&" é utilizado pelo "scanf" para dar comando de "armazenar" o que foi lido  
- "\n" - Quebra a linha para fazer um parágrafo. Muito utilizado no "printf"
- Sempre compliar após qualquer alteração

#### Nome das pastas
- Nunca use números  
- Evite começar o nome de variáveis com letra maiúscula  
- Não use caractéres especiais  
- Evite nomear variáveis que dificultem a leitura (N ; B ; A1; Etc...)  
- Se tiver mais de uma palavra, inicie a segunda com maiúscula. Ou utilize underline.  
- Não use pontuação