Para remover as células duplicadas basta acessar: "Dados" & "Remover duplicatas". Ou utilizar a seguinte fórmula  
A1 = Ricardo  
B1 = Rodrigo  
C1 = Ricardo  
=SE(CONT.SE(A$1:C$1;$A$1)>1; "DUPLICADO"; "") 
