EXP NO:1 C PROGRAM FOR ARRAY OF STRUCTURE TO CHECK ELIGIBILITY FOR THE VACCINE.

Aim: To write a C program for array of structure to check eligibility for the vaccine person age above 6 years of age.

Algorithm:

Declare structure eligible with age (integer) and n (character array)
Declare variable e of type eligible
Input age and name using scanf, store in e
If e.age <= 6
Print "Vaccine Eligibility: No" Else
Print "Vaccine Eligibility: Yes"
Print details (e.age, e.n)
Return 0
Program:
```
#include <stdio.h>
#include <string.h>

struct Person {
    char name[50];
    int age;
};

int main() {
    struct Person p;
    scanf("%d", &p.age);
    scanf("%s", p.name);
    printf("Age:%d\n", p.age);
    printf("Name:%svaccine:%d\n",p.name,p.age);
    
   
    if(p.age>6)
    printf("eligibility:yes");
    else
    printf("eligibility:no");
    return 0;
}
```
Output:
<img width="1258" height="244" alt="image" src="https://github.com/user-attachments/assets/1ca15a7f-cfa5-499b-b6b8-7226ada8bdfa" />
Result: Thus, the program is verified successfully.

EXP NO:2 C PROGRAM FOR PASSING STRUCTURES AS FUNCTION ARGUMENTS AND RETURNING A STRUCTURE FROM A FUNCTION Aim: To write a C program for passing structure as function and returning a structure from a function

Algorithm:

Define structure numbers with members a and b.
Declare variable n of type numbers.
Prompt the user to enter values for a and b.
Input values for a and b into n using scanf.
Call the add function with n as an argument.
Print the result returned by the add function.
Return 0
Program:
```
#include <stdio.h>
struct numbers {
    int a;
    int b;
};
struct numbers add(struct numbers n) {
    struct numbers result;
    result.a = n.a + n.b;
    result.b = n.a * n.b;
    return result;
}
int main() {
    struct numbers n, result;
    printf("Enter value for a: ");
    scanf("%d", &n.a);
    printf("Enter value for b: ");
    scanf("%d", &n.b);
    result = add(n);
    printf("Sum: %d\n", result.a);
    printf("Product: %d\n", result.b);
    return 0;
}
```
Output:
<img width="852" height="436" alt="image" src="https://github.com/user-attachments/assets/f16e4e10-7db5-48d1-abfb-4c3a2799507a" />
Result: Thus, the program is verified successfully

EXP.NO:3 C PROGRAM TO READ A FILE NAME FROM USER AND WRITE THAT FILE USING FOPEN()

Aim: To write a C program to read a file name from user

Algorithm:

Include the necessary header file stdio.h.
Begin the main function.
Declare a file pointer p. Declare a character array name to store the file name.
Prompt the user to enter a file name. Use scanf to input the file name into the name array.
Print a message indicating that the file with the specified name has been created successfully.
Use fopen to open a file with the name provided by the user in write mode ("w").
If successful, continue to the next step.
If unsuccessful, print an error message and exit the program with a non-zero status.
Print a message indicating that the file has been opened successfully.
Use fclose to close the file.
Print a message indicating that the file has been closed.
End the main function.
Return 0 to indicate successful program execution.
Program:
```
#include <stdio.h>
int main()
{
    FILE *fp;
    char name[100];
    scanf("%s",name);
    printf("%s File Created Successfully\n",name);
    fp=fopen("%s","w");
    printf("%s File Opened\n",name);
    fclose(fp);
    printf("%s File Closed\n",name);
}
```
Output:
<img width="849" height="281" alt="image" src="https://github.com/user-attachments/assets/4571ed7c-ceb9-41b8-852c-3e44f4d282be" />
Result: Thus, the program is verified successfully
