# Avalia-o-
import java.util.Scanner;

public class SistemaEscolar {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        double[] notas = new double[8];
        
        // Receber as 8 notas
        for (int i = 0; i < 8; i++) {
            System.out.print("Digite a nota do " + (i + 1) + "º bimestre: ");
            notas[i] = scanner.nextDouble();
        }
        
        // Calcular médias semestrais
        double somaSemestre1 = 0;
        double somaSemestre2 = 0;
        
        for (int i = 0; i < 4; i++) {
            somaSemestre1 += notas[i];
        }
        for (int i = 4; i < 8; i++) {
            somaSemestre2 += notas[i];
        }
        
        double mediaSemestre1 = somaSemestre1 / 4;
        double mediaSemestre2 = somaSemestre2 / 4;
        
        // Calcular média final
        double somaTotal = somaSemestre1 + somaSemestre2;
        double mediaFinal = somaTotal / 8;
        
        // Apresentar resultados
        System.out.println("\n===== RESULTADOS =====");
        for (int i = 0; i < 8; i++) {
            System.out.printf("Nota do %dº bimestre: 
            %.2f\n", (i + 1), notas[i]);
        }
        
        System.out.printf("Média do 1º semestre: %.2f\n", mediaSemestre1);
        System.out.printf("Média do 2º semestre: %.2f\n", mediaSemestre2);
        System.out.printf("Média final: %.2f\n", mediaFinal);
        
        scanner.close();
    }
}
import java.util.Scanner;

public class ConversorTemperatura {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        // Entrada
        System.out.print("Digite a temperatura em graus Celsius: ");
        double celsius = scanner.nextDouble();
        
        // Conversão
        double fahrenheit = (celsius * 9 / 5) + 32;
        double kelvin = celsius + 273.15;
        
        // Saída clara e informativa
        System.out.println("\n===== Conversão de Temperatura =====");
        System.out.printf("Temperatura original: %.2f °C\n", celsius);
        System.out.printf("Convertida para Fahrenheit: %.2f °F\n", fahrenheit);
        System.out.printf("Convertida para Kelvin: %.2f K\n", kelvin);
        
        scanner.close();
    }
}
