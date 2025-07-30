# ObjectArrays
Exercise


        import java.util.*;
        public class ObjectArray {
        public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter size of the array:");
        int size = scanner.nextInt();
        scanner.nextLine();  

        Object[] objectArray = new Object[size];

        System.out.println("\nEnter " + size + " elements |Do number first add space and do letters :");

        for (int i = 0; i < size; i++) {
            objectArray[i] = scanner.nextLine();
        }

        List<String> list = new ArrayList<>();
        for (Object obj : objectArray) {
            list.add(obj.toString());
        }
        System.out.println("\nReverse Order:");
                System.out.println("\nElements");

        
        List<String> reversed = new ArrayList<>(list);
        Collections.reverse(reversed);
        for (String item : reversed) {
            System.out.print(item + " ");
        }
        list.sort((a, b) -> {
            int numA = Integer.parseInt(a.split(" ")[0]);
            int numB = Integer.parseInt(b.split(" ")[0]);
            return Integer.compare(numA, numB);
        });

        System.out.println("\n\nAscending Order:");
                System.out.println("\nElements");

        for (String item : list) {
            System.out.print(item + " ");
        }

        scanner.close();
    }
}
