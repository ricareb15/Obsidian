Numa breve definição, memória é um dispositivo capaz de armazenar informações e, quando solicitado, fornecê-las. A memória eletrônica começou a ser viabilizada a partir da ideia de programa armazenado, elaborada por Von Neumann. Até então, havia a possibilidade de armazenamento das informações em dispositivos que não eram eletrônicos, como fita de papel.

O **ENIAC**, um dos primeiros computadores digitais, já usava o conceito de memória. Usando as válvulas, componente que tem um tamanho considerável em relação aos componentes utilizados atualmente, por este motivo que o ENIAC ocupava grande espaço para comportar sua estrutura.

## Memória RAM
Atualmente, o acesso à memória de forma aleatória, conhecida como memória **RAM** (_Random Acess Memory_), ainda é largamente usada no armazenamento de informações que estão sendo executadas. As memórias evoluíram e tornaram-se <mark style="background: #FFB86CA6;">cada vez menores</mark> com capacidade de memória <mark style="background: #FFB86CA6;">cada vez maior</mark>. Alguns problemas ainda são encontrados, como velocidade de acesso e resposta, no entanto as pesquisas continuam no sentido de melhorar estas características.

A RAM é a memória principal de um computador, basicamente formada por conjuntos de **[^1]transistores** e **[^2]capacitores** combinados que acabam formando uma estrutura chamada **Flip Flops**. 

Este tipo de memória tem como característica a vantagem de <mark style="background: #FFB86CA6;">ser lida e escrita</mark> pela **CPU** trabalhando com os dados de forma temporária, por isso serve para acessar e “trabalhar” dados ao invés de armazena-los. No entanto, quando a máquina é desligada, ele perde suas informações.

Se o computador for composto de pouca memória RAM, então a concorrência pelo seu uso será inevitável. O aplicativo que queremos executar será carregado para a memória RAM, no entanto algum outro aplicativo deverá deixar a memória para que este ocupe um espaço. Este controle é feito pelo sistema operacional, que decide, por algumas técnicas implementadas, qual aplicativo deixará a memória volátil para que o outro aplicativo ocupe este espaço. Este processo de liberar espaço na memória RAM para carregar outro aplicativo de uma memória não volátil é chamado de “_swap_” e quanto mais swaps ocorrerem, mais lenta ficará a execução dos programas.
### Memória SRAM
Pelo nome, já conseguimos concluir que é um modelo de memória com o processo RAM. A sigla significa _Static Random Acess Memory_, ou memória estática de acesso aleatório.

A **SRAM** é constituída por um circuito, com alguns transistores e o modelo não precisa de atualização constante para manter os dados ativos, o famoso “_refresh”._ Essa característica faz a memória ser muito mais rápida e econômica do que o modelo **DRAM**. Sendo indicadas para sistemas onde a velocidade e performance são os itens principais.

Porém tem algumas <mark style="background: #FFF3A3A6;">desvantagens</mark> como: 

- Alto custo de produção 
	devido a necessidade de utilizar mais transistores para funcionar.

- Transistores ocupam mais espaço
	O que acaba reduzindo a capacidade máxima da memória.

- Robustez de componentes
	Por conta da memória ser muito maior, acaba ocupando espaço demais nos chips. 

Todas as desvantagens da SRAM são efeito dos da necessidade de <mark style="background: #FFF3A3A6;">muitos transistores</mark>.
### Memória DRAM
Agora vamos falar sobre o **DRAM** (_Dynamic Random Acess Memory_) também conhecida como <mark style="background: #FFF3A3A6;">"memória dinâmica de acesso remoto"</mark>. Os projetistas de memória reduziram o número de elementos por bit, <mark style="background: #FFF3A3A6;">menos transistores</mark>, assim economizaram área do chip para criar a DRAM. Como resultado, a produção de DRAM é mais barata do que a SRAM.

Por ter sua quantidade de componentes menor e mais espaço no chip, é indicada para sistemas onde o baixo custo e a quantidade de memória são mais vantajosos do que a velocidade. Mas, são amplamente encontradas como memória principal devido ao baixo custo, sendo economicamente mais viáveis.

Por ter um custo reduzido, são muito utilizadas como memória principal em computadores, placas de vídeo (chamadas memórias gráficas), dispositivos portáteis e consoles de videogame. É usada em produtos de alto consumo e atualização constante, por serem mais baratos.

A conclusão simples que podemos chegar é que a DRAM é uma versão atualizada e mais moderna que a SRAM. Foi criada para reduzir custos e tornar mais acessível a tecnologia. Mesmo com desvantagens, a criação da DRAM acelerou o desenvolvimento tecnológico da computação.

## Memória Secundária
Se desligarmos o computador, as informações que estão armazenadas na memória RAM são perdidas. Portanto, temos que gravar os trabalhos que estamos desenvolvendo em algum local onde poderemos resgatá-los quando for preciso. Existem vários tipos de armazenamento secundário que são divididos em três grupos:

---
### Armazenamento magnético
No armazenamento magnético, os dados são gravados de forma semelhante, mesmo que os dispositivos tenham formatos diferentes. Os meios magnéticos de armazenamento são cobertos de partículas minúsculas de ferro que, quando estimuladas por uma corrente elétrica, formam um campo magnético semelhante a um imã.

O problema com este tipo de armazenamento está no transporte e no local onde serão guardados, pois não podem ficar expostos próximos a imãs e qualquer situação onde possa ser criado um campo magnético, como é o caso de transporte em metrô e fios de alta tensão.

```ad-summary
title: Exemplos
collapse: closed
- Disquetes (pouquíssimo utilizados atualmente)
- Discos Rígidos
- Fitas magnéticas

```

---
### Armazenamento óptico
Com o passar do tempo, conforme a quantidade de dados foi crescendo, houve a necessidade de desenvolver meios de armazenamento cada vez mais compactos e com maior poder de armazenamento. Uma das soluções foi gravar as informações em CD/DVD.

Para gravar dados em CD/DVD usa-se a técnica de armazenamento óptico, que oferece precisão altíssima através do feixe de luz. Desta forma consegue-se representar um bit no menor espaço possível, ou seja, em um feixe de luz concentrado, em que toda a energia da luz é alinhada na mesma direção, permitindo que seja focalizada com uma precisão máxima uma área muito pequena.

![[Pasted image 20250513163046.png]]

Conforme podemos ver na figura 8, os CDs têm quatro camadas. A maior parte do material corresponde ao policarbonato (99%), o restante (1%) divide-se em uma camada refletiva, uma de proteção e por último, a camada que decora o disco, que se define como etiqueta. A camada refletora, geralmente composta de prata, armazena as informações no CD em forma de plataforma ou depressão. O ponto que reflete a luz do sensor de laser é a plataforma e o ponto que dispersa a luz é chamado de depressão. Com esta técnica, os valores binários são armazenados no CD.

A diferença entre um CD-R e um CD-RW, está em um material a mais, adicionado entre a camada de policarbonato e a camada protetora, que consiste em uma tinta que permite que o laser modifique os dados gravados

```ad-summary
title: Exempos
collapse: closed
| Tipo de Disco                | Capacidade de Armazenamento                        | Tipo de Laser           | Uso Comum                       |
| :--------------------------- | -------------------------------------------------- | ----------------------- | ------------------------------- |
| CD (Compact Disc)            | Até 700 MB                                         | Laser vermelho (780 nm) | Música, dados simples           |
| DVD (Digital Versatile Disc) | Até 4,7 GB (camada única) ou 8,5 GB (dupla camada) | Laser vermelho (650 nm) | Filmes, software, jogos         |
| Blu-ray                      | Até 25 GB (camada única) ou 50 GB (dupla camada)   | Laser azul <br>(405 nm) | Filmes em alta definição, jogos |

```

---
### Armazenamento de memória Flash.
A memória flash é uma forma de memória não volátil com armazenamento contínuo, mesmo sem fonte de energia. Ela permite reescritas em nível de byte e exclusões de blocos de dados.

A memória Flash utiliza um tipo especial de transistor chamado <mark style="background: #FFF3A3A6;">transistor de porta flutuante</mark>. Esses transistores armazenam elétrons para representar informações digitais como "0" e "1".

Quando um <mark style="background: #FFF3A3A6;">elétron é aprisionado</mark> na porta flutuante, a célula de memória é considerada como **0**.  
Quando <mark style="background: #FFF3A3A6;">não há elétron aprisionado</mark>, a célula de memória é considerada como um **1**.

O processo de gravação e apagamento ocorre por meio da aplicação de tensões elétricas para modificar a carga dos transistores. A gravação é feita em unidades chamadas páginas, enquanto o apagamento acontece em blocos inteiros, o que pode tornar essa operação mais lenta em comparação com a escrita.

```ad-summary
title: Exemplos
collapse: closed
- Pen Drives
- Smartphones
- Câmeras digitais
- Videogames
- Tablets
- Cartões SD.
- Cartões de memória flash

```

---


##
[^1]: **Transistor**: Atua como um interruptor, controlando o fluxo de eletricidade para o capacitor. Ele determina se um bit será armazenado ou não.

[^2]: **Capacitor**: Armazena a carga elétrica, representando os valores "0" ou "1". Como essa carga se dissipa com o tempo, a memória precisa ser constantemente "recarregada" para manter os dados.
