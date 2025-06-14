## Listas
Utilizamos listas quando precisamos trabalhar com muitos valores relacionados, pois elas permitem que se mantenham diversos dados juntos, crie um código mais intuitivo e execute métodos e operações em vários valores de uma só vez. O primeiro item na lista está no índice 0, o segundo no índice 1 e assim por diante.

**Mutáveis**: Você pode alterar, adicionar ou remover elementos após a criação.
**Ordenadas**: Os elementos mantêm a ordem em que foram adicionados.
**Duplicação**: Aceita valores duplicados
**Sintaxe**: Usam colchetes `[]`.
### Impreção na tela
```python
rr [1, 2, 3, 4, 5, 6, 7]

rr[0]
\\ Saída: 1
#Contagem inicia no zero

rr[1]
\\ Saída: 2
#Posição 1

rr[-1]
\\ Saída: 7
#Posição negativa

rr[0:4]
\\ Saída: [1, 2, 3, 4]
#conjunto de índices

rr[0:4] + [4:7]
\\ Saída: [1, 2, 3, 4, 5, 6, 7]
#Soma de conjunto de índices (metade + metade)

rr[:4]
\\ Saída: [1, 2, 3, 4]
#Se não indicar início o conjunto começa no primeiro valor

rr[:4] + [4:]
\\ Saída: [1, 2, 3, 4, 5, 6, 7]
#Vale também para o final

rr[0:4] + [4:-1]
\\ Saída: [1, 2, 3, 4, 5, 6]
#Negativo limita o tamanho do conjunto
```
### Métodos
As listas em Python possuem uma ampla gama de métodos que ajudam na manipulação de seus elementos. Aqui estão alguns dos mais úteis:

- **Apend**
	Adiciona outros elementos a lista
 
 - **Clear**
	Deleta todos os elementos de uma lista

- **Extend**
	Adiciona diversos valores à lista

- **Copy**
	Para adicionar os ELEMENTOS de uma lista e não sua referência (se eu alterar dados do "rick" a "lista" não vai sofrer alteração)

- **Count**
	Conta quantas vezes tal elemento está presente na lista

- **Index**
	Fala em qual posição está determinado número

- **Insert**
	Adiciona tal valor em tal posição

- **Pop**
	Para excluir o último valor da lista ou o especificado 

- **Remove**
	Remove tal valor da lista  

- **Sort**
	Para ordenar em ordem crescente

- **Reverse**
	Para ordenar em ordem decrescente

- **Sum**
	Soma todos os valores da sua lista
##### Exemplo
```python
lista = [1, 2, 4, 5, 5]
rick = [6, 7, 8]

lista.append(6)
print(list) // 1, 2, 3, 4, 5, 5, 6

lista.clear()
print(list) // 

lista.extend(6, 7, 8)
print(list) // 1 2 3 4 5 5 6 7 8

lista.copy(rick)
print(list) // 1 2 3 4 5 5 6 7 8

lista.count(5)
2

lista.index(1)
0

lista.insert(0, -1) // -1 1 2 3 4 5 5

lista.pop(5)
1 2 3 4 5

lista.remove(5) // 1 2 3 4 5
```

## Tuplas
Por outro lado, também armazenam coleções ordenadas de elementos, mas são imutáveis. Isso significa que, uma vez criada, a tupla não pode ser modificada. Essa característica torna as tuplas ideais para dados que devem permanecer constantes, como coordenadas ou configurações.

**Imutáveis**: Uma vez criadas, não podem ser alteradas.
**Ordenadas**: Os elementos mantêm a ordem em que foram adicionados.
**Duplicação**: Aceita valores duplicados
**Sintaxe**: Usam parênteses `()`.
```python
minha_tupla = (1, 2, 3, 4)
```

### Métodos
Embora sejam poucos, esses métodos são práticos para analisar dados armazenados em tuplas.

- **count(`minha_tupla`)**
	Conta quantas vezes um determinado elemento aparece na tupla.

- **index(`minha_tupla`)**
	Retorna o índice do primeiro elemento correspondente ao valor especificado.

## Dicionários
Já os dicionários são estruturas que armazenam pares de chave e valor. Cada chave deve ser única e imutável, enquanto os valores podem variar em tipo e ser repetidos. Dicionários são úteis para associar informações relacionadas, como nomes e idades, ou categorias e itens. Eles são representados com chaves e são muito eficientes para buscas rápidas de valores associados às chaves.

**Mutáveis**: Você pode alterar, adicionar ou remover pares de chave-valor após a criação.
**Não ordenados** (em versões anteriores ao Python 3.7): A ordem dos elementos não é garantida.
**Duplicação**: Aceita valores duplicados
**Sintaxe**: Usam chaves `{}` e pares de chave-valor.
```Python
#Criando
meu_dicionario = {'chave1': 'valor1', 'chave2': 'valor2'}`

#Adicionando chave
meu_dicionario["chave3"] = "Valor3"
```

### Métodos
Esses métodos são muito úteis para manipular os dados armazenados nos dicionários, tornando-os ideais para gerenciar coleções de informações relacionadas.

- **Keys**
	Para obter todas as chaves

- **Values**
	Para obter todos os valores.

- **Items**
	Para acessar os pares chave-valor.

- **Update**({chave: valor})
	Para adicionar ou atualizar um par chave-valor.

- **Pop**(chave) 
	Para remover um elemento com base na chave especificada.

- **Clear**()
	Para apagar todos os itens do dicionário.

- **popItem()**
	Remove e retorna o último par chave-valor do dicionário
### Exemplos
```python

# Criando um dicionário exemplo
meu_dicionario = {
    "nome": "Ricardo",
    "idade": 28,
    "cidade": "São Paulo"
}

# Usando o método keys() para obter todas as chaves
print("Chaves:", meu_dicionario.keys())

# Usando o método values() para obter todos os valores
print("Valores:", meu_dicionario.values())

# Usando o método items() para obter pares chave-valor
print("Itens:", meu_dicionario.items())

# Usando get() para acessar o valor de uma chave sem erro caso a chave não exista
print("Nome:", meu_dicionario.get("nome"))
print("Estado:", meu_dicionario.get("estado", "Não especificado"))  

# Adicionando ou atualizando um par chave-valor com update()
meu_dicionario.update({"estado": "São Paulo"})
print("Atualizado:", meu_dicionario)

# Removendo um item com pop()
idade_removida = meu_dicionario.pop("idade")
print("Idade removida:", idade_removida)
print("Dicionário após remoção:", meu_dicionario)

# Limpando o dicionário com clear()
meu_dicionario.clear()
print("Dicionário após clear():", meu_dicionario)

```