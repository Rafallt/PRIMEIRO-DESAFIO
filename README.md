import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        // Recebe o número de entradas
        int N = scanner.nextInt();
        List<Integer> evenNumbers = new ArrayList<>();
        List<Integer> oddNumbers = new ArrayList<>();

        for (int i = 0; i < N; i++) {
            int value = scanner.nextInt();
            if (value % 2 == 0) {
                evenNumbers.add(value);
            } else {
                oddNumbers.add(value);
            }
        }

        // Ordena os números pares em ordem crescente
        Collections.sort(evenNumbers);
        
        // Ordena os números ímpares em ordem decrescente
        Collections.sort(oddNumbers, Collections.reverseOrder());

        for (int num : evenNumbers) {
            System.out.println(num);
        }
        
        for (int num : oddNumbers) {
            System.out.println(num);
        }
    }
}

