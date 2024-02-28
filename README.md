# MATHEUS-TRAFFIC-SYSTEM








import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("**MATHEUS`S TRAFFIC SYSTEM**");
        System.out.print("Qual era a velocidade do carro? ");
        int velocidadeCarro = scanner.nextInt();
        int velocidadeMaxima = 50;
        System.out.print("A carteira do motorista estava vencida? (Sim/Nao): ");
        String carteiraVencida = scanner.next().toUpperCase();
        System.out.print("Era dia de rodízio do carro? (Sim/Nao): ");
        String diaRodizio = scanner.next().toUpperCase();
        int conta = velocidadeCarro - velocidadeMaxima;
        
    double multa;
        if (velocidadeCarro <= 60) {
            multa = 280.00;
        } else if (velocidadeCarro <= 99) {
            multa = 26.00 * conta;
        } else {
            multa = 40.00 * conta;
        }
        
         int Carteira;
        if (carteiraVencida.equals("Sim") && diaRodizio.equals("Sim")) {
            Carteira = 12;
        }else if (carteiraVencida.equals("Nao") || diaRodizio.equals("Sim")) {
            Carteira = 9;
        }else {
            Carteira = 3;
        }
        
        System.out.println("**MATHEUS`S TRAFFIC SYSTEM**");
        System.out.println("RELATÓRIO:");
        System.out.println("Valor da multa: R$" + multa);
        System.out.println("Pontos na carteira: " + Carteira);
        System.out.println("KMs excedidos: " + conta);
        
        if (multa < 1000.00) {
            System.out.println("INFRAÇÃO SIMPLES!");
        }else if (multa <= 2000.00) {
            System.out.println("INFRAÇÃO MEDIANA!");
        }else if (multa > 2000.00){
            System.out.println("APREENSÃO DO VEÍCULO!");
        }
    }
}
