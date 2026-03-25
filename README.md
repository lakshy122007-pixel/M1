# EX-01-Datatypes-Operators

## AIM:

Write a C program to read 3 characters one by one and print the characters in a reverse order.

## ALGORITHM:

1. Start the program.
2. Declare three character variables (say a, b, c).
3. Read three characters one by one from the user.
4. Print the characters in reverse order (c, b, a).
5. Stop the program. End the program.

## PROGRAM:

```
#include <stdio.h>

int main() {
    char a, b, c;

    printf("Enter three characters:\n");
    
    scanf(" %c", &a);
    scanf(" %c", &b);
    scanf(" %c", &c);

    printf("Characters in reverse order: %c %c %c", c, b, a);

    return 0;
}

```

## OUTPUT:

Enter three characters:
A
B
C
Characters in reverse order: C B A

## RESULT:

Thus the program to read 3 characters one by one and print the characters in a reverse order has been executed successfully.

# EX-02- Conditional-Statements

## AIM:

Write a C program to read A values and check whether A is positive number or not.

# ALGORITHM:

1. Start the program.
2. Declare an integer variable A.
3. Read the value of A from the user.
4. Check if A > 0.
5. If true, print "A is a positive number".
6. Otherwise, print "A is not a positive number".
7. Stop the program.

# PROGRAM:

```
#include <stdio.h>

int main() {
    int A;

    printf("Enter a value: ");
    scanf("%d", &A);

    if (A > 0) {
        printf("%d is a positive number", A);
    } else {
        printf("%d is not a positive number", A);
    }

    return 0;
}

```

# OUTPUT:

Enter a value: 5
5 is a positive number

# RESULT:

Thus the program to read A values and check whether A is positive number or not has been executed successfully.

# EX-03- Operators-Expressions

## AIM:

Write a program to find minimum between two fraction numbers using conditional operator or ternary operator.

## ALGORITHM:

1. Start the program.
2. Declare four integer variables: n1, d1 (first fraction) and n2, d2 (second fraction).
3. Read numerator and denominator for both fractions.
4. Find the minimum using cross multiplication:
5. Compare (n1 * d2) and (n2 * d1) using the ternary operator.
6. Print the smaller fraction.
7. Stop the program.

## PROGRAM:

```
#include <stdio.h>

int main() {
    int n1, d1, n2, d2;

    printf("Enter first fraction (numerator and denominator): ");
    scanf("%d %d", &n1, &d1);

    printf("Enter second fraction (numerator and denominator): ");
    scanf("%d %d", &n2, &d2);

    // Using ternary operator to find minimum fraction
    (n1 * d2 < n2 * d1) ? 
        printf("Minimum fraction is %d/%d", n1, d1) : 
        printf("Minimum fraction is %d/%d", n2, d2);

    return 0;
}

```

## OUTPUT:

Enter first fraction (numerator and denominator): 1 2
Enter second fraction (numerator and denominator): 3 4
Minimum fraction is 1/2

## RESULT:

Thus the program to find minimum between two fraction numbers using conditional operator or ternary operator has been executed successfully.

# EX-04- Using Conditional Statements

## AIM:

Write a C program to check whether the input value is equal to 1 using simple if statement

## ALGORITHM:

1. Start the program.
2. Declare an integer variable num.
3. Read the input value from the user.
4. Check if num == 1 using a simple if statement.
5. If true, print "Value is equal to 1".
6. Stop the program.

## PROGRAM:

```
#include <stdio.h>

int main() {
    int num;

    printf("Enter a value: ");
    scanf("%d", &num);

    if (num == 1) {
        printf("Value is equal to 1");
    }

    return 0;
}

```

## OUTPUT:

Enter a value: 1
Value is equal to 1

## RESULT:

Thus the program to check whether the input value is equal to 1 using simple if statement has been executed successfully

# EX-05- Calculating Total, Percentage, And Division Using Conditional Statements

## AIM:

To write a C program that reads marks of three subjects, calculates the total and percentage, and then determines the division (First, Second, Pass, or Fail) based on the percentage and minimum marks criteria.

## ALGORITHM:

1. Start the program.
2. Declare variables for three subject marks (m1, m2, m3), total, and percentage.
3. Read marks of three subjects from the user.
4. Calculate total:
   total = m1 + m2 + m3
5. Calculate percentage:
   percentage = total / 3.0
6. Check minimum marks condition (each subject ≥ 35):
7. If any subject < 35 → Fail
8. Else determine division based on percentage:
   ≥ 60 → First Division
   ≥ 50 → Second Division
   ≥ 35 → Pass Division
9. Otherwise → Fail
10. Display total, percentage, and division.
11. Stop the program.

## PROGRAM:

```
#include <stdio.h>

int main() {
    int m1, m2, m3, total;
    float percentage;

    printf("Enter marks of three subjects: ");
    scanf("%d %d %d", &m1, &m2, &m3);

    total = m1 + m2 + m3;
    percentage = total / 3.0;

    printf("Total = %d\n", total);
    printf("Percentage = %.2f\n", percentage);

    // Check minimum marks condition
    if (m1 < 35 || m2 < 35 || m3 < 35) {
        printf("Division: Fail");
    } else {
        if (percentage >= 60) {
            printf("Division: First Division");
        } else if (percentage >= 50) {
            printf("Division: Second Division");
        } else if (percentage >= 35) {
            printf("Division: Pass Division");
        } else {
            printf("Division: Fail");
        }
    }

    return 0;
}
```

## OUTPUT:

Enter marks of three subjects: 75 80 70
Total = 225
Percentage = 75.00
Division: First Division

## RESULT:

The program successfully takes three subject marks, calculates the total and percentage, and correctly determines the division based on predefined grading logic.
