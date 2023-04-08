# lesson3.88


public class Main {
    public static void main(String[] args) {
        double[] numbers = {2.5, 6.04, -8.0, 9.8, -6.9, -7.5, 10.5, -1.3, 1.5, 6.5, -4.1, 7.8, 8.5, 8.9, 1.8};
        double sum = 0;
        int amount = 0;
        boolean examination = false;
        for (double nums : numbers) {
            if (nums < 0) {
                examination = true;
            } else if (nums > 0 && examination) {
                sum += nums;
                amount++;
                System.out.println(nums);
            }
        }
        System.out.println("Среднее арифметическое положительных чисел: " + sum / amount);

        System.out.println("-------------------");

        int[] data = {12, 56, -7, 0, 95};
        for (int i = 0; i < data.length; i++) {
            int min = data[i];
            int minId = i;
            for (int j = i + 1; j < data.length; j++) {
                if (data[j] < min) {
                    min = data[j];
                    minId = j;
                }
            }
            int temp = data[i];
            data[i] = min;
            data[minId] = temp;
            System.out.println(Arrays.toString(data));
