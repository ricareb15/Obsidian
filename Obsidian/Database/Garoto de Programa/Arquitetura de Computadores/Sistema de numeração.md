Um sistema de numeração<mark style="background: #FF5582A6;"> é um sistema de representação de números</mark>, que define como os algarismos e símbolos são utilizados para formar números. Cada sistema de numeração possui uma base, que indica o número de símbolos utilizados, e um sistema de organização dos símbolos para representar diferentes valores.

## Decimal
Já estamos acostumados como o Sistema Decimal, onde utilizamos os símbolos **0, 1, 2, 3, 4, 5, 6, 7, 8, 9** para representar  os números. <mark style="background: #FFB86CA6;">Chamamos esse sistema de base 10 porque ele utiliza 10 símbolos diferentes para representar todos os números</mark>. Vou te mostrar porque é chamado de base 10. Imagine o número **347**. Fazendo uma abstração, esse número tem uma estrutura oculta de centena, dezena e unidade. Para gera esse número, o que acontece por baixo dos panos é algo assim: 

1. Primeiro pegamos **3** x **100** = **300**, 
2. depois pegamos **4** x **10** = **40** e 
3. por fim **7** x **1** = **7**, 
4. Onde somando tudo gera o número **347.** 

Agora veja que interessante. <mark style="background: #FFB86CA6;">Utilizando a base 10</mark>, a representação é a mesma, veja:

1. Fazemos **3** x **10²** = **300**,
2. Depois **4** x **10¹** = **40**
3. e por fim **7** X **100** = **7** Lembrando que 100 = 1

## Binário
No sistema binário, <mark style="background: #FFB86CA6;">é base 2</mark> porque você só tem o <mark style="background: #FFB86CA6;">Zero (0)</mark> e o <mark style="background: #FFB86CA6;">Um (1)</mark> para fazer as combinações para representar os valores. Como usa apenas os símbolos 0 e 1, é mais fácil de ser representado por circuitos eletrônicos, como já explicamos em artigos anteriores.

### Conversão
Para você compreender como esse sistema funciona, vamos pegar o número decimal **10** e transformar em Binário. A regra é a seguinte: você vai <mark style="background: #FFF3A3A6;">dividindo o número por 2</mark>, separando sempre o seu resto e continuando a dividir o seu quociente <mark style="background: #FFF3A3A6;">até que ele seja menor que 2</mark>. Aí você pega os restos dessas divisões por 2, de baixo para cima (do último para o primeiro). Esse conjunto de retos em zeros e uns, vão compor a representação em binário. Veja o exemplo:

![[Pasted image 20250507063425.png]]

## Hexadecimal
Como você pode perceber, no sistema binário são necessários muitos dígitos para representar números relativamente pequenos, o que dificulta o trabalho das pessoas que programam os computadores. 

Para solucionar este problema usa-se frequentemente o sistema de numeração hexadecimal. Vem do hexa=6 e deci=10, sistema numérico de **base 16**. Ele vai de <mark style="background: #FFB86CA6;">0 à 10</mark> e utiliza <mark style="background: #FFB86CA6;">A,B,C,D,E e F</mark> que representam **10,11,12,13,14** e **15** respectivamente.