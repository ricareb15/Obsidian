`=EXT.TEXTO(célula ; núm_inícial ; Qnt_caracters)`
Utilizado para selecionar específicos caracteres dentro da célula.  
A1 = 440.abc.SSD  
=EXT.TEXTO(A1;1;3) 440  
=EXT.TEXTO(A1;5;3) abc  
=EXT.TEXTO(A1;9;3) SSD  
Célula; Posição para iniciar contagem ; Quanto contar  

#### EXT.TEXTO + LOCALIZAR
`=EXT.TEXTO(célula ; Iníciar quando() ; Qnt_caracters)`
Bom para usar em nomes americanos, por exemplo:  
A1 = Lima, Ricardo 
=EXT.TEXTO(A1 ; LOCALIZAR( "," ; A1 ; 1)+2 ; 1000) Ricardo  
=EXT.TEXTO(A1 ; 1 ; LOCALIZAR ( "," ; A1 ; 1)-1) Lima  