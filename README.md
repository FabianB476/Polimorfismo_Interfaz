### POLIFORMISMO

-El polimorfismo es una característica de la programación orientada a objetos (POO) que permite que distintos objetos respondan de manera diferente al mismo mensaje 
### INTERFAZ 

- La interfaz es un conjunto de métodos que definen cómo se debe comportar un objeto. También se le conoce como protocolo 


# 

![](https://image.jimcdn.com/app/cms/image/transf/dimension=661x10000:format=png/path/s98fa877a37296084/image/i23d8c6c7f3b0df82/version/1476921720/image.png-75x5png)

![](https://img.shields.io/github/stars/pandao/editor.md.svg) ![](https://img.shields.io/github/forks/pandao/editor.md.svg) ![](https://img.shields.io/github/tag/pandao/editor.md.svg) ![](https://img.shields.io/github/release/pandao/editor.md.svg) ![](https://img.shields.io/github/issues/pandao/editor.md.svg) ![](https://img.shields.io/bower/v/editor.md.svg)


**Table of Contents**

[TOCM]

[TOC]



####Javascript　

using System;

class Matematicas
{
    public virtual double CalcularPerimetro()
    {
        return 0;
    }
}

class Triangulo : Matematicas
{
    public double Lado { get; set; }

    public Triangulo(double lado)
    {
        Lado = lado;
    }

    public override double CalcularPerimetro()
    {
        return 3 * Lado;
    }
}

class Cuadrado : Matematicas
{
    public double Lado { get; set; }

    public Cuadrado(double lado)
    {
        Lado = lado;
    }

    public override double CalcularPerimetro()
    {
        return 4 * Lado;
    }
}

class Program
{
    static void Main()
    {
        Console.WriteLine("Calculadora de Perímetro");
        Console.WriteLine("Seleccione la figura (1- Triángulo, 2- Cuadrado): ");
        int opcion = int.Parse(Console.ReadLine());

        if (opcion == 1)
        {
            Console.WriteLine("Ingrese el lado del triángulo: ");
            double lado = double.Parse(Console.ReadLine());
            Triangulo triangulo = new Triangulo(lado);
            Console.WriteLine("El perímetro del triángulo es: " + triangulo.CalcularPerimetro());
        }
        else if (opcion == 2)
        {
            Console.WriteLine("Ingrese el lado del cuadrado: ");
            double lado = double.Parse(Console.ReadLine());
            Cuadrado cuadrado = new Cuadrado(lado);
            Console.WriteLine("El perímetro del cuadrado es: " + cuadrado.CalcularPerimetro());
        }
        else
        {
            Console.WriteLine("Opción no válida.");
        }
    }
}
