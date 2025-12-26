# EX-26-AREA-OF-RECTANGLE-USING- POINTER
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
#include<stdio.h>
int main()
{
    int x,y,*p1,*p2;
    p1=&x,p2=&y;
    scanf("%d%d",p1,p2);
    printf("The product is %d",*p1*(*p2));
    return 0;
}

```
## OUTPUT
<img width="431" height="173" alt="image" src="https://github.com/user-attachments/assets/0d427e52-2cc7-48e0-bbe9-2e11e3abf2d4" />
	       	


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
#include<stdio.h>
#include<stdlib.h>
#include<string.h>
int main()
{
    char *str=(char*)malloc(8*sizeof(char));
    strcpy(str,"WELCOME");
    printf("%s",str);
    free(str);
    return 0;
}

```
## OUTPUT
<img width="398" height="161" alt="image" src="https://github.com/user-attachments/assets/97eb142b-08fa-4f99-a5d6-e4f6912440d4" />



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
#include<stdio.h>
struct student
{
  char name[100];
  int roll,marks;
};
int main()
{
    struct student s;
    printf("Enter student name:");
    scanf("%s",s.name);
    printf("\nEnter student roll no:");
    scanf("%d",&s.roll);
    printf("\nEnter student marks:");
    scanf("%d",&s.marks);
    printf("\nStudent information:\nStudent name:%s\nStudent roll no.:%d\nStudent marks:%d",s.name,s.roll,s.marks);
    return 0;
}

```

## OUTPUT
<img width="444" height="419" alt="image" src="https://github.com/user-attachments/assets/86e0bf61-e4f9-4279-8f4c-9bdceed96336" />


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
#include<stdio.h>
struct employee
{
  char name[100];
  int id,salary;
  float gsalary,da,hra;
}e[3];
int main()
{
    int i;
    for(i=0;i<3;i++)
    {
        printf("Enter details for Employee %d:\n", i+1);
        printf("Name: ");
        scanf("%s",e[i].name);
        printf("Id: ");
        scanf("%d",&e[i].id);
        printf("Basic Salary: ");
        scanf("%d", &e[i].salary);
        e[i].da = 0.4 * e[i].salary;
        e[i].hra = 0.2 * e[i].salary;
        e[i].gsalary = e[i].salary + e[i].da + e[i].hra;
    }
    printf("\nEmployee details:\n");
    for(i=0;i<3;i++)
    {
        printf("\nEmployee %d:\n", i + 1);
        printf("Name: %s\n", e[i].name);
        printf("Basic Salary: %d\n", e[i].salary);
        printf("DA: %.2f\n", e[i].da);
        printf("HRA: %.2f\n", e[i].hra);
        printf("Gross Salary: %.2f\n", e[i].gsalary);
    }
    return 0;
}

```

 ## OUTPUT
<img width="422" height="650" alt="image" src="https://github.com/user-attachments/assets/611d360d-773a-4e97-8564-c9fd3d18bf97" />
<img width="451" height="477" alt="image" src="https://github.com/user-attachments/assets/943693d8-ab54-44b5-9c33-866ce598edf1" />


 

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
#include<stdio.h>
struct Student 
{
    char name[50];
    int roll,marks[3];
    int total;
    float avg;
};
int main() {
    struct Student s;
    printf("Enter student name: ");
    scanf("%s", s.name);
    printf("\nRoll no:");
    scanf("%d",&s.roll);
    s.total = 0;
    for (int i = 0; i < 3; i++) 
    {
        printf("Enter marks for subject %d: ", i + 1);
        scanf("%d", &s.marks[i]);
        s.total += s.marks[i];
    }
    s.avg = s.total / 3.0;
    printf("\nStudent Details:\n");
    printf("Name: %s\n", s.name);
    printf("Total Marks: %d\n", s.total);
    printf("Average Marks: %.2f\n", s.avg);
    return 0;
}
```

## OUTPUT
<img width="414" height="383" alt="image" src="https://github.com/user-attachments/assets/36be3660-9860-4d55-b087-bce21e6461f6" />

 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


