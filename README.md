import java.util.Locale;
import java.util.Scanner;

public class menu {

public static void main(String[] args) {

Locale.setDefault(Locale.US);
Scanner sc = new Scanner(System.in);

int questao;

do {
System.out.println("Informa qual questão deseja desenvolver: ");
System.out.println("");
System.out.println("1 - Cálculo Triângulo, circulo, quadrado, retângulo, trapéio ");
System.out.println("2 - Ler duas Peças e Calcular o valor total da Nota ");
System.out.println("3 - DIFERENCA = (A * B - C * D). ");
System.out.println("4 - Cálculo de Almoço");
System.out.println("5 - Compra de Bolsa");
System.out.println("0 - Sair");

questao = sc.nextInt();

if (questao == 0) {
System.out.println("\nAté Logo!");
sc.close();
}

switch (questao){
       case 1:
       
    System.out.println("Informe o valor de A: ");
    float a = sc.nextFloat();
    System.out.println(a);
   
    System.out.println("Informe o valor de B: ");
    float b = sc.nextFloat();
    System.out.println(b);
   
    System.out.println("Informe o valor de C: ");
    float c = sc.nextFloat();
    System.out.println(c);
   
    double triangulo = a * c / 2.0;
    System.out.println(String.format("TRIANGULO: %.2f", triangulo));
   
       double circulo = 3.14159 * (c * c);
       System.out.println(String.format("CIRCULO: %.2f", circulo));
           
       double trapezio = ((a + b) * c) / 2;
       System.out.println(String.format("TRAPEZIO: %.2f", trapezio));
           
       double quadrado = b * b;
       System.out.println(String.format("QUADRADO: %.2f", quadrado));

       double retangulo = a * b;
       System.out.println(String.format("RETANGULO: %.2f", retangulo));
    break;    
       case 2:
        System.out.println("Informe o código da peça 1 : ");
    double peca1 = sc.nextDouble();
   
    System.out.println("Informe a quatidade da peça 1: ");
    double qtd1 = sc.nextDouble();
   
    System.out.println("Informe o preço da peça 1: ");
    double preco1 = sc.nextDouble();
   
    System.out.println("Informe o código da peça 2 : ");
    double peca2 = sc.nextDouble();
   
    System.out.println("Informe o preço da peça 2: ");
    double preco2 = sc.nextDouble();
   
    System.out.println("Informe a quatidade da peça 2: ");
    double qtd2 = sc.nextDouble();
   
    double valortotal= qtd1*preco1+qtd2*preco2;
    System.out.println("O valor a ser pago é:  "+ valortotal);
           break;            
       case 3:
        System.out.println("Informe o o valor a : ");
    int A = sc.nextInt();
   
    System.out.println("Informe o o valor b : ");
    int B = sc.nextInt();
   
    System.out.println("Informe o o valor c : ");
    int C = sc.nextInt();
   
    System.out.println("Informe o o valor d : ");
    int D = sc.nextInt();
   
    int resultado = (A*B-C*D);
    System.out.println("A diferença é:  "+ resultado);
    break;    
       case 4:
        System.out.println("Cliente, informe a quantidade de comida que você vai consumir : ");
    int kg = sc.nextInt();
    double valorkg = 23.00;

    double valor = (kg*valorkg);
    System.out.println(String.format("O valor a pagar é: R$ %.2f", valor));
           break;            
       case 5:                  
        System.out.println("Dona Maria, informe o valor da bolsa : ");
        double valorbolsa5 = sc.nextDouble();
    double descontoespecie = valorbolsa * 0.10;
    double itemdesconto = valorbolsa - descontoespecie;
    System.out.println(String.format("O valor a ser pago com desconto é: R$%.2f", itemdesconto));
    double parcela = valorbolsa / 3;
    double parcelas2 = parcela * 2;
    System.out.println(String.format("O valor em uma parcela é: R$%.2f", parcela));
    System.out.println(String.format("O valor em duas parcelas é: R$%.2f", parcelas2));
   
    double itemcomjuros = valorbolsa * 0.05;
    double bolsajuros = (valorbolsa + itemcomjuros) / 10.0;
    System.out.println(String.format("O valor parcelado em 10 vezes com juros é: R$%.2f", bolsajuros));
           break;        
}
} while (questao != 0);
sc.close();
}
}
