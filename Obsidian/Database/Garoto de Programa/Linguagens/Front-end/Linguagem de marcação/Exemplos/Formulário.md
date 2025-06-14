Estrutura
```gdscript
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>Formulário</title>
</head>
<body>
	
	<form action=""></form>
</body>
</html>
```

### label
Usado para descrever o dado que deve ser inserido
<label for="">Nome</label>

### Input
Para criar uma barra onde possa se inserir os dados
#### Atributos
type="checkbox" - Para criar um check list  
type="radio" - Para criar uma lista com alternativas  
name="xxx" - Criar um grupo nas tags de "radio" e "checkbox" para selecionar apenas 1  
type="text" - Quando os dados forem texto  
type="number" - Quando os dados forem números  
type="password" - Quando os dados forem senhas  
type="checkbox" - Para criar um check list  
<maxlenght/> - Para limitar a quantidade de caracteres  
value="xxx" - Dar nome as tags para facilitar na hora do Java e CSS  
type="submit" value="Enviar" - Botão de enviar  
type="reset" value="Limpar" - Botão para limpar o formulário  
(Nestes dois casos o value é utilizado para inserir o texto dentro do botão)

#CSS 

### Select
Usado para espeço de seleção, onde o usuário escolhe entre as opções.
Dentro dessa tag, é utilizado as "<option/>"