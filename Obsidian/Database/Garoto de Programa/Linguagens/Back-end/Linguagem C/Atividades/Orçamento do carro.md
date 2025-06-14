```gdscript
#include <stdio.h>  
int main() {  
  
#define DIAS_NO_MES 30  
  
char tipo[30];  
int quantidade;  
float Consumo_por_km;  
float km_por_dia;  
float preco_por_litro;  
int num_veiculos;  
float consumo_por_dia;  
float consumo_por_mes;  
float custo_por_mes;  
  
printf("Quantos tipos de veículos deseja cadastrar");  
scanf("%d", &num_veiculos);  
  
printf("\n--- Dados do veiculo ---\n")  
printf("Digite o tipo de veículo");  
scanf("%s", &tipo);  
  
printf("Digite a quantidade de veículos");  
scanf("%d", &quantidade);  
  
printf("Digite o consumo de combustível por quilomentro (em litros");  
scanf("%f", &consumo_por_km);  
  
printf("Digite a quantidade de KMs rodados por dia");  
scanf("%s", &km_por_dia);  
  
printf("Digite o preço estimado por litro de combustível (em R$)");  
scanf("%f", &preco_por_litro);  
  
consumo_por_dia = consumo_por_km * km_por_dia * quantidade;  
consumo_por_mes = consumo_por_dia * DIAS_NO_MES;  
custo_por_mes = consumo_por_mes * preco_por_litro;  
  
printf("\n---- Resultado para o %s ----\n" , tipo);  
printf("Quantidade de veículos: %d\n"), quantidade;  
printf("Consumo diário por veículo: %.2f litros por KM\n", consumo_por_km);  
printf("Total de KMs por dia: %.2f KM\n", km_por_dia);  
printf("Consumo total de combustível por dia: %.2f litros\n", consumo_por_dia);  
printf("Consumo total de combustível por mes", consumo_por_mes);  
printf("Custo estimado por mes: R$%.2f\n", custo_por_mes);  
  
return 0;  
}
```