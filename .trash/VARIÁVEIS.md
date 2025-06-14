Linguagem: #C 

### Introdução
Podemos pensar na memória do computador como um grande armário cheio de gavetas, as variáveis são as gavetas e, para uma melhor organização, cada uma possui uma etiqueta indicando o tipo de material que pode ser guardado nela. E a classificação do que pode ser guardada nela é definido pelo tipo de variável. Existem 5 tipos:
```
int: Números inteiros  
char: Letras, caracteres, dados alfanuméricos  
float: Números reais com precisão simples, ocupa 4 bytes na memória  
double: Números reais com precisão dupla , ocupa 8 bytes na memória  
void: Vazio
```

Além dos tipos, existem em C os modificadores de tipo:
```
short: Diminui o espaço em memória reservado para uma variável  
long: Aumenta o espaço em memória reservado para uma variável  
unsigned: indica que a variável será guardada sem sinal  
signed : Indica que a variável será armazenada com sinal
```

### Especificadores de formato
O especificadores de formato são utilizados nas funções de entrada e saída em C, como printf e scanf, para lidar com as diversas especificações existentes. Podendo então, formatar a saída, e interpretar a entrada de dados. Exemplos são:

```gdscript
%d - para números inteiros  
%f - para números de ponto flutuante (com casas decimais)  
%lf- para números de ponto flutuante duplamente precisos (double)  
%c - para caracteres  
%s - para sequência de caracteres
```

### Constantes
Seguem o mesmo conceito das variáveis. Mas como o próprio nome diz "constantes" servem para definir valores que nunca vão ser alterados (data de nascimento do usuário por exemplo)
[[Orçamento do carro]]
