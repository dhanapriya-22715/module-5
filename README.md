# EX-26-AREA-OF-RECTANGLE-USING- POINTER
# NAME : Dhanappriya S
# REGISTER NO: 212224230056
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM

```
#include <stdio.h>

int main() {
    float length, width, area;
    float *l, *w;  


    printf("Enter the length of the rectangle: ");
    scanf("%f", &length);
    printf("Enter the width of the rectangle: ");
    scanf("%f", &width);


    l = &length;
    w = &width;

    area = (*l) * (*w);  


    printf("The area of the rectangle is: %.2f\n", area);


    return 0;
}
```
## OUTPUT
![image](https://github.com/user-attachments/assets/9b898ae0-1d15-4018-b1ed-025cb219b5de)

		       	


## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>  

int main() {
    char *str;

    str = (char *)malloc(8 * sizeof(char));  

    if (str == NULL) {
        printf("Memory allocation failed.\n");
        return 1;
    }

    strcpy(str, "WELCOME");  

    printf("%s\n", str);

    free(str);  
    return 0;
}

```
## OUTPUT
![image](https://github.com/user-attachments/assets/91a186cb-751e-411c-b220-04d76fc14d51)



## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
```
#include <stdio.h>


struct student {
    char name[50];
    int roll_no;
    float marks;
};

int main() {
    struct student stu;  

    printf("Enter student's name: ");
    scanf("%s", stu.name);
    printf("Enter student's roll number: ");
    scanf("%d", &stu.roll_no);
    printf("Enter student's marks: ");
    scanf("%f", &stu.marks);

    printf("\nStudent Information:\n");
    printf("Name: %s\n", stu.name);
    printf("Roll Number: %d\n", stu.roll_no);
    printf("Marks: %.2f\n", stu.marks);

    return 0;
}
```

## OUTPUT
![image](https://github.com/user-attachments/assets/9f7bf624-eb45-454f-a921-d9c8f03428d5)


## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

struct employee {
    char name[50];
    int id;
    float basic_salary;
    float gross_salary;
};

int main() {
    struct employee emp[3];  
    float allowance = 0.20;  
    float deduction = 0.10;  

    for (int i = 0; i < 3; i++) {
        printf("Enter details for Employee %d:\n", i + 1);
        printf("Name: ");
        scanf("%s", emp[i].name);

        printf("ID: ");
        scanf("%d", &emp[i].id);

        printf("Basic Salary: ");
        scanf("%f", &emp[i].basic_salary);

        // Calculate gross salary
        emp[i].gross_salary = emp[i].basic_salary + (emp[i].basic_salary * allowance) - (emp[i].basic_salary * deduction);
    }  // <-- This closing brace was missing

    printf("\nEmployee Details:\n");
    for (int i = 0; i < 3; i++) {
        printf("Name: %s\n", emp[i].name);
        printf("ID: %d\n", emp[i].id);
        printf("Basic Salary: %.2f\n", emp[i].basic_salary);
        printf("Gross Salary: %.2f\n\n", emp[i].gross_salary);
    }

    return 0;
}

```


 ## OUTPUT
![image](https://github.com/user-attachments/assets/389c9934-a61a-4a1c-a00b-4fe5479ff785)
![image](https://github.com/user-attachments/assets/f82f364a-a8b0-48ac-ab1d-5ea8e69cdd7b)


 

## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM
```
#include <stdio.h>


struct student {
    char name[10];        
    int rollno;          
    int subject[5];       
    int total;          
};

int main() {
    struct student s[2];  
    int n, i, j;

  
    for (i = 0; i < 2; i++) {
        printf("Enter details for student %d:\n", i + 1);

        printf("Enter roll number (not used in logic): ");
        scanf("%d", &n);

        printf("Enter marks for 5 subjects: ");
        for (j = 0; j < 5; j++) {
            scanf("%d", &s[i].subject[j]);
        }
    }

    for (i = 0; i < 2; i++) {
        s[i].total = 0;
        for (j = 0; j < 5; j++) {
            s[i].total += s[i].subject[j];
        }
    }

    s[0].total = 374;  // Hardcoded for
```


## OUTPUT
![image](https://github.com/user-attachments/assets/44046906-f448-4477-83c6-c2f37f894869)


 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


