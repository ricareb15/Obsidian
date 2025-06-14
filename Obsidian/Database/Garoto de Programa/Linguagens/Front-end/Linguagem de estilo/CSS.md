### Existem três formas de linkar de utilizar o css
#### Inline
Utilizado "style" diretamente nas tags do HTML  
```gdscript
<body>  
<h1 style="color: purple; font-size: 15px> Teste  
</h1>  
</body>
```

#### Interno
Estilizando o código dretamente no head do HTML utilizando a tag "style"  
Lembrando que os atributos selecionados... vão valer para todas as tags.
```
<head>  
<style>  
h1{  
color: blue;  
font - family: Arial, sans - serif  
}  
</style>  
</head> 
```

#### Externo  
Quando o CSS fica em um arquivo próprio em .css  
Lincando-o assim, no head  
```
<link rel="stylesheet" href="xxx" 
``` 
rel - Tipo de link (que no caso é a estilização)  
href - Onde está localizado o arquivo (caminho/nome)

Classe - .xxx
Id - # xxx

### Display
[[Linguagens/Front-end/HTML/Display/Flex]]
### Cor
[[Cor]]