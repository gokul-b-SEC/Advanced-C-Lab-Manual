EXP NO: 1
C PROGRAM FOR ARRAY OF STRUCTURE TO CHECK ELIGIBILITY FOR THE VACCINE
Aim:

To write a C program for array of structure to check eligibility for the vaccine for a person above 6 years of age.

Algorithm:
Declare a structure eligible with age (integer) and n (character array).
Declare an array e of type eligible.
Input age and name using scanf and store them in the structure.
If e.age <= 6:
Print "Vaccine Eligibility: No"
Else:
Print "Vaccine Eligibility: Yes"
Print the details (e.age, e.n).
Return 0.
Program:
#include <stdio.h>

struct eligible
{
    int age;
    char n[50];
};

int main()
{
    struct eligible e;

    printf("Enter the name: ");
    scanf("%s", e.n);

    printf("Enter the age: ");
    scanf("%d", &e.age);

    printf("\nName: %s\n", e.n);
    printf("Age: %d\n", e.age);

    if (e.age <= 6)
        printf("Vaccine Eligibility: No\n");
    else
        printf("Vaccine Eligibility: Yes\n");

    return 0;
}
Output:
Enter the name: Gokul
Enter the age: 20

Name: Gokul
Age: 20
Vaccine Eligibility: Yes
Result:

Thus, the program is verified successfully.

EXP NO: 2
C PROGRAM FOR PASSING STRUCTURES AS FUNCTION ARGUMENTS AND RETURNING A STRUCTURE FROM A FUNCTION
Aim:

To write a C program for passing structure as function argument and returning a structure from a function.

Algorithm:
Define structure numbers with members a and b.
Declare variable n of type numbers.
Prompt the user to enter values for a and b.
Input values for a and b into n using scanf.
Call the add function with n as an argument.
Return the result from the add function.
Print the result returned by the add function.
Return 0.
Program:
#include <stdio.h>

struct numbers
{
    int a;
    int b;
};

struct numbers add(struct numbers n)
{
    struct numbers result;

    result.a = n.a + n.b;

    return result;
}

int main()
{
    struct numbers n, result;

    printf("Enter the value of a: ");
    scanf("%d", &n.a);

    printf("Enter the value of b: ");
    scanf("%d", &n.b);

    result = add(n);

    printf("Sum = %d\n", result.a);

    return 0;
}
Output:
Enter the value of a: 25
Enter the value of b: 15
Sum = 40
Result:

Thus, the program is verified successfully.

EXP NO: 3
C PROGRAM TO READ A FILE NAME FROM USER AND WRITE THAT FILE USING FOPEN()
Aim:

To write a C program to read a file name from the user and create the file using fopen().

Algorithm:
Include the necessary header file stdio.h.
Begin the main() function.
Declare a file pointer p.
Declare a character array name to store the file name.
Prompt the user to enter a file name.
Use scanf to input the file name into the name array.
Use fopen() to open the file with the name provided by the user in write mode ("w").
If the file is opened successfully:
Print a message indicating that the file has been opened successfully.
If the file cannot be opened:
Print an error message and exit the program.
Use fclose() to close the file.
Print a message indicating that the file has been closed.
Return 0.
Program:
#include <stdio.h>

int main()
{
    FILE *p;
    char name[50];

    printf("Enter the file name: ");
    scanf("%s", name);

    p = fopen(name, "w");

    if (p == NULL)
    {
        printf("Error: Unable to create the file.\n");
        return 1;
    }

    printf("File '%s' opened successfully.\n", name);

    fclose(p);

    printf("File closed successfully.\n");

    return 0;
}
Output:
Enter the file name: sample.txt
File 'sample.txt' opened successfully.
File closed successfully.
Result:

Thus, the program is verified successfully.

EXP NO: 4
C PROGRAM TO READ A FILE NAME FROM USER, WRITE THAT FILE AND INSERT TEXT INTO THAT FILE
Aim:

To write a C program to read a file name from the user, create the file, and insert text into that file.

Algorithm:
Include the necessary header file stdio.h.
Begin the main() function.
Declare a file pointer p.
Declare character arrays name and text.
Declare an integer variable num.
Prompt the user to enter a file name and the number of strings.
Use scanf to input the file name and number of strings.
Use fopen() to open the file in write mode ("w").
If the file cannot be opened:
Print an error message and exit the program.
Use a loop to input strings from the user.
Write each string into the file using fputs().
Use fclose() to close the file.
Print a message indicating that the data has been added successfully.
Return 0.
Program:
#include <stdio.h>

int main()
{
    FILE *p;
    char name[50];
    char text[100];
    int num, i;

    printf("Enter the file name: ");
    scanf("%s", name);

    printf("Enter the number of strings: ");
    scanf("%d", &num);

    p = fopen(name, "w");

    if (p == NULL)
    {
        printf("Error: Unable to create the file.\n");
        return 1;
    }

    printf("File opened successfully.\n");

    for (i = 0; i < num; i++)
    {
        printf("Enter string %d: ", i + 1);
        scanf(" %[^\n]", text);
        fputs(text, p);
        fputs("\n", p);
    }

    fclose(p);

    printf("Data added successfully to the file.\n");

    return 0;
}
Output:
Enter the file name: data.txt
Enter the number of strings: 3
File opened successfully.
Enter string 1: Hello World
Enter string 2: C Programming
Enter string 3: File Handling
Data added successfully to the file.
Result:

Thus, the program is verified successfully.

EXP NO: 5
C PROGRAM TO DISPLAY STUDENT DETAILS USING STRUCTURE
Aim:

The aim of this program is to dynamically allocate memory to store information about multiple subjects, including subject name and marks, input the details for each subject, and display the stored information. Finally, the allocated memory is freed to prevent memory leaks.

Algorithm:
Input the number of subjects.
Read the integer value n from the user, which represents the number of subjects.
Define a structure student with members name and marks.
Dynamically allocate memory using malloc() for n subjects.
If memory allocation fails, display an error message and exit the program.
Use a for loop to read the name and marks of each subject.
Store the subject name and marks in the dynamically allocated memory.
Use another for loop to display the details of each subject.
After all operations are completed, call free() to release the allocated memory.
Return 0.
End the program.
Program:
#include <stdio.h>
#include <stdlib.h>

struct student
{
    char name[50];
    int marks;
};

int main()
{
    struct student *s;
    int n, i;

    printf("Enter the number of subjects: ");
    scanf("%d", &n);

    s = (struct student *)malloc(n * sizeof(struct student));

    if (s == NULL)
    {
        printf("Memory allocation failed.\n");
        return 1;
    }

    for (i = 0; i < n; i++)
    {
        printf("\nEnter the name of subject %d: ", i + 1);
        scanf("%s", s[i].name);

        printf("Enter the marks: ");
        scanf("%d", &s[i].marks);
    }

    printf("\n--- Student Details ---\n");

    for (i = 0; i < n; i++)
    {
        printf("Subject: %s\n", s[i].name);
        printf("Marks: %d\n", s[i].marks);
    }

    free(s);

    return 0;
}
Output:
Enter the number of subjects: 3

Enter the name of subject 1: Mathematics
Enter the marks: 95

Enter the name of subject 2: Physics
Enter the marks: 88

Enter the name of subject 3: Chemistry
Enter the marks: 92

--- Student Details ---
Subject: Mathematics
Marks: 95
Subject: Physics
Marks: 88
Subject: Chemistry
Marks: 92
Result:

Thus, the program is verified successfully.
