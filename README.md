# Avalia-o-3import java.util.Scanner;

public class Atividade01 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        double[] notas = new double[8];
        double[] bimestres = new double[4];
        double[] semestres = new double[2];

        // Entrada das notas
        System.out.println("Digite as 8 notas do aluno:");
        for (int i = 0; i < 8; i++) {
            System.out.print("Nota " + (i + 1) + ": ");
            notas[i] = sc.nextDouble();
        }

        // Cálculo das médias bimestrais
        for (int i = 0; i < 4; i++) {
            bimestres[i] = (notas[i * 2] + notas[i * 2 + 1]) / 2.0;
        }

        // Cálculo das médias semestrais
        semestres[0] = (bimestres[0] + bimestres[1]) / 2.0;
        semestres[1] = (bimestres[2] + bimestres[3]) / 2.0;

        // Cálculo da média final
        double mediaFinal = (semestres[0] + semestres[1]) / 2.0;

        // Exibição dos resultados
        System.out.println("\nResultados:");
        for (int i = 0; i < 4; i++) {
            System.out.printf("%dº Bimestre: %.1f\n", i + 1, bimestres[i]);
        }
        System.out.printf("1º Semestre: %.1f\n", semestres[0]);
        System.out.printf("2º Semestre: %.1f\n", semestres[1]);
        System.out.printf("Média Final: %.1f\n", mediaFinal);
    }
}
