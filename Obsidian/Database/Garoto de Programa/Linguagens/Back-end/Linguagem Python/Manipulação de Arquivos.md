A manipulação de dados em Python é uma das tarefas mais comuns e poderosas da linguagem, especialmente em ciência de dados, análise estatística e automação de processos. Python oferece diversas bibliotecas para facilitar essa tarefa, tornando a manipulação de dados eficiente e intuitiva.

## Modos de abertura de arquivo
Eles definem como o arquivo será manipulado, como se fosse um tipo de "licença" para definir como o arquivo será manipulado. Aqui estão os principais modos:

- **`"r"` (read)** 
	Abre o arquivo apenas para leitura. Se o arquivo não existir, ocorre um erro.

- **`"w"` (write)**
	Abre para escrita, mas **sobrescreve** o conteúdo do arquivo. Se o arquivo não existir, ele será criado.

- **`"a"` (append)**
	Abre para adicionar conteúdo ao final do arquivo sem apagar o existente.

- **`"x"` (exclusive creation)**
	Cria um novo arquivo, mas falha se ele já existir.

- **`"r+"` (read/write)**
	Permite leitura e escrita no mesmo arquivo.

## Funções
Python oferece diversas funções para manipulação de arquivos, permitindo leitura, escrita, edição e remoção de dados. O módulo embutido `open()` é a base para lidar com arquivos.

### Abertura e fechamento de arquivos
```python
#Abrindo um arquivo para leitura 
arquivo = open("#exemplo.txt", "r") 

# Fechando o arquivo após o uso 
arquivo.close()
```
```ad-info
collapse: closed

`open`("**endereço do arquivo**", **Modo de abertura**)

```

### Leitura de arquivos
```python
with open("exemplo.txt", "r") as arquivo: 
	conteudo = arquivo.read() # Lê todo o conteúdo 
	
	print(conteudo) 

arquivo.readline() # Lê apenas uma linha  

arquivo.readlines() # Retorna uma lista com todas as linhas do arquivo
```
### Escrita em arquivos
```python
with open("exemplo.txt", "w") as arquivo: # 'w' sobrescreve o conteúdo 
	
	arquivo.write("Olá, mundo!") 	


with open("exemplo.txt", "a") as arquivo: # 'a' adiciona conteúdo ao final
	
	arquivo.write("\nNova linha adicionada.")
```
```ad-note
title: Anotação
collapse: closed
Lembrando que você pode utilizar das [[Entrada e Saída de Dados|Sequencia de Scape]] para formatar o texto do jeito que quiser na hora de escrever.

Ao fazer uma lista em um arquivo txt por exemplo, é interessante fazer uma quebra de linha após cada item (**exemplo**: `texto\n`). Desta forma, organizando a lista. 

```

### Removendo arquivos
```python
import os
os.remove("exemplo.txt") #Para deletar arquivos

os.rmdir("exp_pasta.txt") #Para remover pastas
```

## Complemento
Muitas das vezes estas funções podem acabar não funcionando se o arquivo não existir.
Para isso, é possível utilizar de uma estrutura de condição para validar a existência do arquivo.
```python
import os

if os.path.exists("exemplo.txt"):
	os.remove("exemplo.txt")
else :
	print("Arquivo não existe")

```
