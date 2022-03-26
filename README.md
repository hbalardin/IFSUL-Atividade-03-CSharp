Aluno: Henrique Balardin
Turma: 4INF
Ano: 2022

# IFSUL-Atividade-03-C#
Atividade de Linguagem de Programação III.

## 1) Faça um programa para calcular o estoque médio de uma peça, sendo que:
ESTOQUE MÉDIO = (QUANTIDADE_MÍNIMA + QUANTIDADE_MÁXIMA) / 2.

```C#
using System;

namespace InvetoryManger{
	public class Program
	{
		public static void Main()
		{
			Selector();
		}
		
		public static void Selector(){
			Console.WriteLine("===== Gerenciador de estoque! =====");
			
			Console.WriteLine("Qual a quantidade mínima de estoque? ");
			int currencyValue = int.Parse(Console.ReadLine());
			
			Console.WriteLine("Qual a quantidade máxima de estoque? ");
			int amount = int.Parse(Console.ReadLine());
			
			double result = GetAverage(amount, currencyValue);
			Console.WriteLine("O estoque médio é " + result + " !");
			
			Console.WriteLine();
			Console.WriteLine("Obrigado pela preferência! ;)");
			Console.WriteLine("====================================================");
		}
		
		public static double GetAverage(int min, int max){
			return (min + max)/2;
		}
	}
}

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
using System;

namespace ComissionManger{
	public class Program
	{
		public static void Main()
		{
			Selector();
		}
		
		public static void Selector(){
			Console.WriteLine("===== Gerenciador de comissões! =====");
			
			Console.WriteLine("Digite a identifição do vendedor: ");
			string sellerId = Console.ReadLine();
			
			Console.WriteLine("Digite o código da peça: ");
			string itemId = Console.ReadLine();
			
			Console.WriteLine("Digite o preço unitário da peça: ");
			double unitPrice = double.Parse(Console.ReadLine());
			
			Console.WriteLine("Digite a quantidade de peças vendidas: ");
			int quantity = int.Parse(Console.ReadLine());
			
			double total = getTotal(unitPrice, quantity);
			double comissionValue = getComission(total);
			
			Console.WriteLine("Considerando uma comissão de 5%, o vendedor com identificação '" + sellerId + "' vendeu " + total + " reais em peças, e receberá o valor de " + comissionValue + " reais!");
			
			Console.WriteLine();
			Console.WriteLine("Obrigado pela preferência! ;)");
			Console.WriteLine("====================================================");
		}
		
		public static double getTotal(double price, int quantity){
			return price * quantity;
		}
		
		public static double getComission(double value){
			return value * 0.05;
		}
	}
}

```
