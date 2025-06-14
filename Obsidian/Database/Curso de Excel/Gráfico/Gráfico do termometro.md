![[Pasted image 20250104180001.png]]  ![[Pasted image 20250104180105.png]] ![[Pasted image 20250104180205.png]]

Este gráfico muda de cor de acordo com o valor
Siga o passo a passo para criar este tipo de gráfico:

1. É necessário criar a lógica de cada cor para o gráfico se basear
2. Vermelho: =SE(A1 <= 30%; A1; NÂO.DISP())
3. Amarelo: =SE(E(A1 > 30%; A1 <= 70%; A1; NÂO.DISP()))
4. Verde: =SE( A1 > 70%; A1; NÂO.DISP())
5. Insira um gráfico de colunas com base nas fórmulas que acabamos de fazer
6. É necessário formatar cada série, com verde, amarelo e vermelho.
7. Tirar fundo e contorno do gráfico
8. Adicionar a imagem do termometro, clicar com botão direito e "trazer para frente"
9. Posicionar termometro sem fundo em cima do grágico e fazer ajustes
10. Dando assim o efeito do termometro
11. Para adicionar a porcentagem na parte inferior é necessário ir em "inserir" > "texto" > "caixa de texto"