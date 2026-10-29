A. Arithmetic Operators (Q1–Q3)
Q1. Write a Java program to find the area of a triangle using Heron's formula.
Q1. Area of Triangle

Program:

class Main {
    public static void main(String[] args) {
        double a = 3, b = 4, c = 5;
        double s = (a + b + c) / 2;
        double area = Math.sqrt(s * (s-a) * (s-b) * (s-c));
        System.out.println("Area = " + area);
    }
}

Output:

Area = 6.0
Q2. Create a Java program to calculate compound interest given principal, rate, and time.
Q2. Compound Interest

Program:

class Main {
    public static void main(String[] args) {
        double p = 1000, r = 10, t = 2;
        double amount = p * Math.pow(1 + r/100, t);
        double ci = amount - p;
        System.out.println("Compound Interest = " + ci);
    }
}

Output:

Compound Interest = 210.0
Q3. Develop a Java program to find the distance between two points in a 2D plane.
Q3. Distance Between Two Points

Program:

class Main {
    public static void main(String[] args) {
        int x1 = 2, y1 = 3, x2 = 5, y2 = 7;
        double d = Math.sqrt(Math.pow(x2-x1, 2)
                           + Math.pow(y2-y1, 2));
        System.out.println("Distance = " + d);
    }
}

Output:

Distance = 5.0
B. Unary Operators (Q4–Q5)
Q4. Write a Java program to demonstrate prefix and postfix increment by simulating visitors entering and leaving a store.
Q4. Prefix and Postfix Increment

Program:

class Main {
    public static void main(String[] args) {
        int visitors = 5;
        System.out.println("Before entry: " + visitors);
        System.out.println("Entry: " + (++visitors));
        System.out.println("Exit: " + (visitors--));
        System.out.println("Remaining: " + visitors);
    }
}

Output:

Before entry: 5
Entry: 6
Exit: 6
Remaining: 5
Q5. Create a Java program that takes an integer and outputs its negative value using a unary operator.
Q5. Negative Value

Program:

class Main {
    public static void main(String[] args) {
        int n = 10;
        System.out.println("Negative value = " + (-n));
    }
}

Output:

Negative value = -10
C. Assignment Operators (Q6–Q7)
Q6. Write a Java program to repeatedly divide a number by half using /= until it becomes less than 1.
Q6. Divide by Half

Program:

class Main {
    public static void main(String[] args) {
        double n = 16;
        int steps = 0;
        while (n >= 1) {
            n /= 2;
            steps++;
        }
        System.out.println("Steps = " + steps);
    }
}

Output:

Steps = 5
Q7. Create a Java program to add rainfall data for seven days using +=.
Q7. Total Rainfall

Program:

class Main {
    public static void main(String[] args) {
        int[] rain = {10, 20, 15, 5, 12, 8, 10};
        int total = 0;
        for (int r : rain) {
            total += r;
        }
        System.out.println("Total Rainfall = " + total);
    }
}

Output:

Total Rainfall = 80
D. Relational Operators (Q8–Q9)
Q8. Write a Java program to check whether three given angles form a valid triangle.
Q8. Valid Triangle

Program:

class Main {
    public static void main(String[] args) {
        int a = 60, b = 60, c = 60;
        if (a > 0 && b > 0 && c > 0 && a+b+c == 180)
            System.out.println("Valid Triangle");
        else
            System.out.println("Invalid Triangle");
    }
}

Output:

Valid Triangle
Q9. Create a Java program to compare two strings lexicographically without using built-in comparison functions.
Q9. String Comparison

Program:

class Main {
    public static void main(String[] args) {
        String a = "Apple", b = "Banana";
        int i = 0;
        while (i < a.length() && i < b.length()
                && a.charAt(i) == b.charAt(i))
            i++;

        if (i == a.length() && i == b.length())
            System.out.println("Strings are equal");
        else if (i == a.length() ||
                (i < b.length() && a.charAt(i) < b.charAt(i)))
            System.out.println("Apple comes first");
        else
            System.out.println("Banana comes first");
    }
}

Output:

Apple comes first
E. Logical Operators (Q10–Q11)
Q10. Write a Java program to check whether a year is a leap year and falls within a given range.
Q10. Leap Year and Range

Program:

class Main {
    public static void main(String[] args) {
        int year = 2024;
        boolean leap = year % 400 == 0 ||
                (year % 4 == 0 && year % 100 != 0);

        if (leap && year >= 2000 && year <= 2030)
            System.out.println("Valid Leap Year");
        else
            System.out.println("Not Valid");
    }
}

Output:

Valid Leap Year
Q11. Create a Java program to check whether a student passes a course with the given theory, practical, and overall marks criteria.
Q11. Student Pass Criteria

Program:

class Main {
    public static void main(String[] args) {
        int theory = 45, practical = 55, overall = 50;

        if ((theory >= 40 && practical >= 50) || overall >= 50)
            System.out.println("Pass");
        else
            System.out.println("Fail");
    }
}

Output:

Pass
F. Ternary Operators (Q12–Q13)
Q12. Write a Java program to find the smallest of four numbers using nested ternary operators.
Q12. Smallest of Four Numbers

Program:

class Main {
    public static void main(String[] args) {
        int a = 12, b = 5, c = 8, d = 3;
        int min = (a < b ? a : b);
        min = min < c ? min : c;
        min = min < d ? min : d;
        System.out.println("Smallest = " + min);
    }
}

Output:

Smallest = 3
Q13. Create a Java program to identify whether a character is a vowel, consonant, digit, or special symbol using the ternary operator.
Q13. Character Classification

Program:

class Main {
    public static void main(String[] args) {
        char ch = 'A';
        String result = !Character.isLetterOrDigit(ch) ?
                "Special Symbol" :
                Character.isDigit(ch) ? "Digit" :
                "AEIOUaeiou".indexOf(ch) >= 0 ?
                "Vowel" : "Consonant";
        System.out.println(result);
    }
}

Output:

Vowel
G. Bitwise Operators (Q14–Q15)
Q14. Write a Java program to swap two integers without using a temporary variable, using XOR.
Q14. Swap Using XOR

Program:

class Main {
    public static void main(String[] args) {
        int a = 10, b = 20;
        a = a ^ b;
        b = a ^ b;
        a = a ^ b;
        System.out.println("a = " + a);
        System.out.println("b = " + b);
    }
}

Output:

a = 20
b = 10
Q15. Create a Java program to count the number of set bits in the binary representation of a number.
Q15. Count Set Bits

Program:

class Main {
    public static void main(String[] args) {
        int n = 13, count = 0;
        while (n > 0) {
            count += n & 1;
            n >>= 1;
        }
        System.out.println("Set Bits = " + count);
    }
}

Output:

Set Bits = 3
H. Shift Operators (Q16–Q17)
Q16. Write a Java program to multiply and divide a number by powers of two using shift operators.
Q16. Shift Operations

Program:

class Main {
    public static void main(String[] args) {
        int n = 8;
        System.out.println("Multiply by 4 = " + (n << 2));
        System.out.println("Divide by 4 = " + (n >> 2));
    }
}

Output:

Multiply by 4 = 32
Divide by 4 = 2
Q17. Create a Java program to cyclically rotate the bits of an integer to the left by two positions.
Q17. Rotate Bits Left

Program:

class Main {
    public static void main(String[] args) {
        int n = 8;
        int result = (n << 2) | (n >>> 30);
        System.out.println("Rotated value = " + result);
    }
}

Output:

Rotated value = 32

Note: Q17 rotates a 32-bit integer. For the selected value 8, the two highest bits are zero, so the result is 32.

I. For Loop (Q18–Q19)
Q18. Write a Java program to print the first 20 terms of the Fibonacci sequence using a for loop.
Q18. Fibonacci Sequence

Program:

class Main {
    public static void main(String[] args) {
        int a = 0, b = 1;
        for (int i = 1; i <= 20; i++) {
            System.out.print(a + " ");
            int c = a + b;
            a = b;
            b = c;
        }
    }
}

Output:

0 1 1 2 3 5 8 13 21 34
55 89 144 233 377 610 987 1597 2584 4181
Q19. Create a Java program to print all Armstrong numbers between 1 and 1000 using a for loop.
Q19. Armstrong Numbers

Program:

class Main {
    public static void main(String[] args) {
        for (int n = 1; n <= 1000; n++) {
            int temp = n, sum = 0;
            while (temp > 0) {
                int d = temp % 10;
                sum += d * d * d;
                temp /= 10;
            }
            if (sum == n)
                System.out.print(n + " ");
        }
    }
}

Output:

1 153 370 371 407

Note: This program uses the standard three-digit Armstrong formula, so it identifies the Armstrong numbers from 1 to 1000 under that definition.

J. Do-While Loop (Q20–Q21)
Q20. Write a Java program to repeatedly accept a password until the correct one is entered using a do-while loop.
Q20. Password Validation

Program:

import java.util.Scanner;

class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String password;
        do {
            System.out.print("Enter password: ");
            password = sc.nextLine();
        } while (!password.equals("java123"));

        System.out.println("Correct Password");
        sc.close();
    }
}

Sample Output:

Enter password: hello
Enter password: java123
Correct Password
Q21. Create a Java program to display all factors of a number using a do-while loop.
Q21. Factors of a Number

Program:

class Main {
    public static void main(String[] args) {
        int n = 12, i = 1;
        do {
            if (n % i == 0)
                System.out.print(i + " ");
            i++;
        } while (i <= n);
    }
}

Output:

1 2 3 4 6 12
K. While Loop (Q22–Q23)
Q22. Write a Java program to reverse the digits of an integer using a while loop.
Q22. Reverse a Number

Program:

class Main {
    public static void main(String[] args) {
        int n = 1234, rev = 0;
        while (n > 0) {
            rev = rev * 10 + n % 10;
            n /= 10;
        }
        System.out.println("Reverse = " + rev);
    }
}

Output:

Reverse = 4321
Q23. Create a Java program to determine whether a number is a palindrome using a while loop.
Q23. Palindrome Number

Program:

class Main {
    public static void main(String[] args) {
        int n = 121, temp = n, rev = 0;
        while (temp > 0) {
            rev = rev * 10 + temp % 10;
            temp /= 10;
        }
        System.out.println(n == rev ? "Palindrome" : "Not Palindrome");
    }
}

Output:

Palindrome
L. For-Each Loop (Q24–Q25)
Q24. Write a Java program to find the maximum and minimum values in an integer array using a for-each loop.
Q24. Maximum and Minimum

Program:

class Main {
    public static void main(String[] args) {
        int[] a = {10, 5, 20, 3, 15};
        int max = a[0], min = a[0];

        for (int n : a) {
            if (n > max) max = n;
            if (n < min) min = n;
        }
        System.out.println("Maximum = " + max);
        System.out.println("Minimum = " + min);
    }
}

Output:

Maximum = 20
Minimum = 3
Q25. Create a Java program to calculate the average marks of students stored in a 2D array using a for-each loop.
Q25. Average Marks

Program:

class Main {
    public static void main(String[] args) {
        int[][] marks = {{70, 80}, {60, 90}};
        int sum = 0, count = 0;

        for (int[] row : marks) {
            for (int m : row) {
                sum += m;
                count++;
            }
        }
        System.out.println("Average = " + (sum / (double) count));
    }
}

Output:

Average = 75.0
M. Switch-Case (Q26–Q27)
Q26. Write a Java program to display whether a day is a weekday or weekend using its number from 1 to 7.
Q26. Weekday or Weekend

Program:

class Main {
    public static void main(String[] args) {
        int day = 6;
        switch (day) {
            case 1, 2, 3, 4, 5:
                System.out.println("Weekday");
                break;
            case 6, 7:
                System.out.println("Weekend");
                break;
            default:
                System.out.println("Invalid Day");
        }
    }
}

Output:

Weekend
Q27. Create a Java program that displays the meaning of a grade from A to F using switch-case.
Q27. Grade Meaning

Program:

class Main {
    public static void main(String[] args) {
        char grade = 'A';
        switch (grade) {
            case 'A': System.out.println("Excellent"); break;
            case 'B': System.out.println("Good"); break;
            case 'C': System.out.println("Average"); break;
            case 'D': System.out.println("Below Average"); break;
            case 'E': System.out.println("Poor"); break;
            case 'F': System.out.println("Fail"); break;
            default: System.out.println("Invalid Grade");
        }
    }
}

Output:

Excellent
N. Continue Statement (Q28)
Q28. Write a Java program to print numbers from 1 to 50, skipping perfect squares using continue.
Q28. Skip Perfect Squares

Program:

class Main {
    public static void main(String[] args) {
        for (int i = 1; i <= 50; i++) {
            int root = (int) Math.sqrt(i);
            if (root * root == i)
                continue;
            System.out.print(i + " ");
        }
    }
}

Output:

2 3 5 6 7 8 10 11 12 13 14 15 17 18 19 20
22 23 24 26 27 28 29 30 31 32 33 34 35 37
38 39 40 41 42 43 44 45 46 47 48 50
O. Break Statement (Q29)
Q29. Create a Java program to generate random integers from 1 to 100 and stop when a number divisible by both 7 and 13 is found.
Q29. Random Numbers Using Break

Program:

import java.util.Random;

class Main {
    public static void main(String[] args) {
        Random r = new Random();
        int n;
        do {
            n = r.nextInt(100) + 1;
            System.out.println(n);
            if (n % 7 == 0 && n % 13 == 0)
                break;
        } while (true);
    }
}

Sample Output:

12
45
8
91

Note: The sample output is illustrative. The program stops when it generates a number divisible by both 7 and 13; within 1–100, that number is 91.

P. Mixed Advanced (Q30)
Q30. Write a Java program that checks whether a number is a power of 4 using shift operators, toggles its third bit using bitwise operators, and prints its multiplication table while skipping multiples of 6 and stopping at multiples of 48.
Q30. Mixed Operators and Loops

Program:

class Main {
    public static void main(String[] args) {
        int n = 16;
        boolean power = false;

        for (int x = n; x > 0; x >>= 2) {
            if (x == 1) {
                power = true;
                break;
            }
        }
        System.out.println("Power of 4: " + power);

        int toggled = n ^ (1 << 2);
        System.out.println("After toggling 3rd bit: " + toggled);

        for (int i = 1; i <= 20; i++) {
            int value = n * i;
            if (value % 48 == 0) break;
            if (i % 6 == 0) continue;
            System.out.println(n + " x " + i + " = " + value);
        }
    }
}

Output:

Power of 4: true
After toggling 3rd bit: 20
16 x 1 = 16
16 x 2 = 32

Note: The loop stops when the product reaches 48's multiple (here, 16 × 3 = 48), so it prints only the first two multiplication results.

Your assignment Q1–Q30 is complete, with full questions, Java programs, and sample outputs.# JAVA-LAB-SHEET-2
