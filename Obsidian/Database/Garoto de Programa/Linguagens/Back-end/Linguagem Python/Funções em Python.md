As funções em Python são blocos de código reutilizáveis que ajudam a organizar e modularizar programas. Elas são essenciais para evitar repetição de código, melhorar a legibilidade e facilitar a manutenção.

A função `def` em Python é usada para **definir funções**. Ela permite criar blocos de código reutilizáveis que podem ser chamados em diferentes partes do programa.

```python
def soma(a, b): 
	return a + b 

resultado = soma(3, 5) 
print(resultado) 
# Saída: 8
```

### Exemplo

```python
# Este programa retorna os parcelamentos iguais através da entrada de dados como:
#1. o valor do pagamento a vista
#2. Número de parcelamento (número de meses) (n)
#3. Juro do financiamento ou taxa do banco por mês (i)

# Considerando a fórmula de juros compostos: M = C (1 + i)^n

#Um subprograma (procedimento) : mensagens de abertura
def mensagens():
    print("***************************************")
    print(" bem vindo da Sistema de Financiamento ")
    print("***************************************")

#Um subprograma (função)para calcular termo comum : (1+i)^n
def termoComum(N_meses,taxa):
    resultado = 1.0 #acumulador
    expressao = 1 + taxa/100
    for i in range(N_meses):
        resultado *= expressao
    return resultado

#Um subprograma (função) para calcular os parcelas iguais
def calcularParcelamentos(Pgavista,termo,taxa):
    par_iguais = Pgavista*((termo*taxa/100)/(termo -1))
    return par_iguais

#Um subprograma (procediemento) para mostrar os resultados
def mostrarResultados(par_iguais,N_meses,Pgavista):
    print(f"As parcelas iguais será R$ {par_iguais:.2f}")
    total_pago = par_iguais * N_meses
    print(f"O valor total será pago R$ {total_pago:.2f}")
    juro_pago = total_pago - Pgavista
    print(f"O juro será pago R$ {juro_pago:.2f}")

#Programa principal
    
mensagens()
#entrada de dados
Pgavista = float(input("Informe o valor a vista : R$ "))
N_meses = int(input("Quantos meses gostaria de pagar ? "))
taxa = float(input("Qual é a taxa do banco por mês ? "))
#operações de calculo
termo = termoComum(N_meses,taxa)
par_iguais = calcularParcelamentos(Pgavista,termo,taxa)
#mostrar os resultados
mostrarResultados(par_iguais,N_meses,Pgavista)

input("Finalizando o sistema !")
```