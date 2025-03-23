# calculadora-em-C-1
using System;

class Program
{
    static void Main()
    {
        Console.Write("Digite o primeiro número: ");
        double num1 = double.Parse(Console.ReadLine());

        Console.Write("Digite o segundo número: ");
        double num2 = double.Parse(Console.ReadLine());

        Console.WriteLine("Escolha a operação que deseja realizar:");
        Console.WriteLine("1. Adição");
        Console.WriteLine("2. Subtração");
        Console.WriteLine("3. Multiplicação");
        Console.WriteLine("4. Divisão");
        int operacao = int.Parse(Console.ReadLine());

        double resultado = 0;

        switch (operacao)
        {
            case 1:
                resultado = num1 + num2;
                Console.WriteLine($"Resultado da adição: {resultado}");
                break;

            case 2:
                resultado = num1 - num2;
                Console.WriteLine($"Resultado da subtração: {resultado}");
                break;

            case 3:
                resultado = num1 * num2;
                Console.WriteLine($"Resultado da multiplicação: {resultado}");
                break;

            case 4:
                if (num2 != 0)
                {
                    resultado = num1 / num2;
                    Console.WriteLine($"Resultado da divisão: {resultado}");
                }
                else
                {
                    Console.WriteLine("Erro: Não é possível dividir por zero.");
                }
                break;

            default:
                Console.WriteLine("Operação inválida. Escolha uma opção de 1 a 4.");
                break;
        }
    }
}
