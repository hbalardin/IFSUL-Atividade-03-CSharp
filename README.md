Aluno: Henrique Balardin
Turma: 4INF
Ano: 2022

# IFSUL-Atividade-03-C#
Atividade de Linguagem de Programação III.

## 1) Faça um programa para calcular o estoque médio de uma peça, sendo que:
ESTOQUE MÉDIO = (QUANTIDADE_MÍNIMA + QUANTIDADE_MÁXIMA) / 2.

```C#


```

## 2) Faça um programa que:
Leia a cotação do dólar
Leia um valor em dólares
Converta esse valor para Real

```C#
using System;

namespace DollarConverter{
	public class Program
	{
		public static void Main()
		{
			Selector();
		}
		
		public static void Selector(){
			Console.WriteLine("===== Conversor de moeda! =====");
			
			Console.WriteLine("Digite a cotação do dólar: ");
			double currencyValue = double.Parse(Console.ReadLine());
			
			Console.WriteLine("Qual a quantia de dólares que deseja converter para real? ");
			double amount = double.Parse(Console.ReadLine());
			
			double result = Convert(amount, currencyValue);
			Console.WriteLine("O valor convertido é " + result + " reais!");
			
			Console.WriteLine();
			Console.WriteLine("Obrigado pela preferência! ;)");
			Console.WriteLine("====================================================");
		}
		
		public static double Convert(double amount, double currencyValue){
			return amount / currencyValue;
		}
	}
}

```

## 3) Faça um programa para pagamento de comissão de vendedores de peças, levando-se em consideração que sua comissão será de 5% do total da venda e que você tem os seguintes dados:
Identificação do vendedor
Código da peça
Preço unitário da peça
Quantidade vendida

```C#
```
