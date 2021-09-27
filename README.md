# Java-practice-questions-with-solution
This is a java practice Questions starting from beginners level

Question 1 : Write a Java method to find the smallest number among three numbers.
-->
import java.util.Scanner;

public class Practice_Day_1 {
    static float smallestNumber(float a , float b , float c){
        float d;
        if (a<b || a<c) {
            d = a;
        }
        else if (b<a || b<c) {
           d = b;
        }
        else{
            d = c;
        }
        return d;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the first number");
        float firstNumber = sc.nextFloat();
        System.out.println("Enter the second number");
        float secondNumber = sc.nextFloat();
        System.out.println("Enter the third number");
        float thirdNumber = sc.nextFloat();
        float smallNumber = smallestNumber(firstNumber , secondNumber , thirdNumber);
        System.out.println(smallNumber);
    }
}

Output:
Enter the first number
25
Enter the second number
37
Enter the third number
29
25.0


Question 2 : Write a Java method to compute the average of three numbers.
-->
import java.util.Scanner;

public class Practice_Day_1 {

    static float average(float a , float b , float c){
        float d = (a + b + c) / 3;
        return d;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the first number");
        float firstNumber = sc.nextFloat();
        System.out.println("Enter the second number");
        float secondNumber = sc.nextFloat();
        System.out.println("Enter the third number");
        float thirdNumber = sc.nextFloat();
        float avg = average(firstNumber , secondNumber , thirdNumber);
        System.out.println(avg);
    }
}

Output:
Enter the first number
25
Enter the second number
45
Enter the third number
65 
45.0

Question 3 : Write a Java method to display the middle character of a string. 
Note: a) If the length of the string is odd there will be two middle characters.
b) If the length of the string is even there will be one middle character.
-->
import java.util.Scanner;

public class Practice_Day_1 {
    static void middleCharacter(String a){
        int position;
        int length;
        int b = a.length();
        if (b % 2 == 0) {
            position = b / 2 - 1;
            length = 2;
            System.out.println(a.substring(position , position + length));
        }
        else{
            position = b / 2;
            length = 1;
            System.out.println(a.substring(position , position + length));
        }
    }
    public static void main(String[] args) {
            Scanner sc = new Scanner(System.in);
            System.out.print("Enter a String : ");
            String a = sc.nextLine();
            middleCharacter(a);
    }
}

Output 1:(Odd number of characters in the string) 
Enter a String : Like The Post
h

Output 2:(Even number of characters in the string)
Enter a String : void
oi

Question 4 : Write a Java method to count all vowels in a string.
-->
import java.util.Scanner;

public class Practice_Day_1 {

    static int countVowels(String str){
        int count = 0;
        for (int i = 0; i < str.length(); i++) {
            if (str.charAt(i) == 'a' || str.charAt(i) == 'e' || str.charAt(i) == 'i'
                    || str.charAt(i) == 'o' || str.charAt(i) == 'u' || str.charAt(i) == 'A' ||
                     str.charAt(i) == 'E' || str.charAt(i) == 'I'
                    || str.charAt(i) == 'O' || str.charAt(i) == 'U') {
                count = count + 1;
            }
        }
        return count;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter a String");
        String str = sc.nextLine();
        System.out.println(countVowels(str));
    }
}
Output:
Enter a String
AeIoU
5
