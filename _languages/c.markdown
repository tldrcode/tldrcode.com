---
layout: language
icon: icon-c
permalink: c/
featured: False

Language: C
Language_Description: General purpose, low-level programming language.

Data_Types:
- Type: Basic variables
  Description: Declares a variable of one of the basic built-in types.
  Syntax: typename variablename
  Example: |
           int x, y=3
           float f;
           char c;
  Example_Description: declares two integers, x and y. y is initialized to 3. declares a floating point variable, f and a char(1 byte) variable c.

- Type: Array
  Description: For storing a list of things
  Syntax: |
          //declaration
          typename arrayname[ARRAY_SIZE];
          //access the nth element
          arrayname[n-1]  //arrays are indexed starting at 0
  Example: |
           int primes[10] = {2, 3, 5, 7, 11, 13, 17, 19, 23, 29};
           int five = primes[2];
  Example_Description: Creates and array then indexes on that array

- Type: Struct
  Description: Declares a data type with several member variables. Structs are used to group variables together.
  Syntax: |
          //define the structure
          struct mystruct
          {
            typename membername;
            ...
          };
          //declare an instance
          struct mystruct instancename;
  Example: |
           struct point
           {
            int x, y;
           };
           struct point begin, end;
           begin.x = 0;
           begin.y = 0;
  Example_Description: Defines a struct called point, than creates 2 instances, called begin and end. The x and y members of begin are then set to 0.

- Type: Strings
  Description: Null-terminated strings. Strings are just arrays of chars
  Syntax: char string[13] = "Hello World!";

- Type: Pointer
  Description: Data type for storing locations in memory.
  Syntax: typename * ptr_var;
  Example: |
           int * pA, *pB;
           int a = 3, b = 5, c = 0;
           pA = &a;
           pB = &b;
           c = *pA; //c is now 3
           a = *pB; //a is now 5, and *pA is also 5


Flow_Control:
- Type: "if/else if /else"
  Description: Basic if else statement common to most languages
  Syntax: if(condition) {code} else if (condition2) {code} else {code}
  Example: |
          if( x == 0)
          {
            printf("You don't have any bananas\n");
          } else if (x < 20) {
            printf("You have %d bananas\n", x);
          } else {
            printf("Woah! You have a lot of bananas!\n");
          }
  Example_Description: This will print out how many bananas the use has (see printf for more info).

- Type: while
  Description: Repeats code as long as statement remains true.
  Syntax: while (statement) {code}
  Example: while (x>5) {code}
  Example_Description: Code will only execute if x is greater than 5 and will keep looping until x isn't greater than 5.

- Type: do while
  Description: Code executes once and then statement is tested.  If statement remains true the do while will keep looping.
  Syntax: |
          do{ code }while(statement);
  Example: |
          do{
            //code
          } while(x > 5);
  Example_Description: Code will execute once and then test if x is greater than 5.  If it is then it'll loop, if not it'll move on.

- Type: for
  Description: Loops as long as the stated conditions are met.
  Syntax: for (initialization; condition; increment) {code}
  Example: for (int x=0; x>5; x++) {code}
  Example_Description: Evaluates 'x' and loops if x is greater than 5.  After each execution the value of x will increase by '+1'.

- Type: switch
  Description: Allows specific code to be used. Variable used must be an integer and the 'vars' must be constant. The switch will jump to the first case that's equal to your stated variable and do the rest of the codes from there (so it'll skip everything before the first case used).  If none of the cases are equal to your variable then it'll only execute the last section of code (the code following 'default').
  Syntax: |
          switch (variable)
          {
            case var1:
              code;
            case var2:
              code;
            default:
              code;
          }
  Example: |
          int x = 2;
          switch (x)
            {
              case 1:
                //code;
              case 2:
                //code;
              default:
                //code;
            }
  Example_Description: "This would initialize x to be 2, then jump to the case 2 label, where it would execute from there until the end of the switch statement. Note: even the code under default: will get executed."

- Type: Function
  Description: For creating and using subroutines.
  Syntax: returnType name(int arg1, int arg2, float arg3) { code }
  Example: int product(int a, int b) { return a * b; }
  Example_Description: Function returns the product of both of its arguments.

File_IO:
- Type: fopen
  Description: Opens a file
  Syntax: FILE * file_ptr = fopen( filename, file_mode);
  Example: FILE * input_file = fopen("input.txt", "r");
  Example_Description: Open a file named "input.txt" in read mode, and store the pointer to the file descriptor in input_file.

- Type: fscanf
  Description: reads data from the file pointed to by fp, into the locations pinted to by the additional arguments. Read information about format strings for more info.
  Example: |-
           int a, b;
           int *B = &b;
           char string[10];
           FILE *ifp = fopen("data.txt", "r");
           fscanf(ifp, "%d %d %s", &a, B, string);
  Example_Description: Reads in two integers and a string from the beginning of data.txt, and store them in the variables a, b, and string, respectively.

- Type: scanf
  Description: Special case of fscanf that simply uses stdin rather than an arbitrary file. Read information about format strings for more info.
  Syntax: scanf (control_string, &var1, &var2, ...);
  Example: scanf ("%d", &x);
  Example_Description: This would read an integer from stdin and place the value of it into x

- Type: fprintf
  Syntax: int fprintf ( FILE * ofp, const char * format, ... );
  Description: Print the message described by format and the additional arguments. Read information about format strings for more info.
  Example: |-
           int x = 10;
           float flt = 34.10;
           char str = "Hello";
           FILE *ofp = fopen("output.txt", "w");
           printf("%s %d is an integer, %f is a number\n", str, x, flt);
  Example_Description: opens the file output.txt for writing, then writes the message "Hello 10 is an integer, 34.100000 is a number" followed by a newline character

- Type: printf
  Description: Special case of the printf function, that only interacts with stdout. Read information about format strings for more info.
  Syntax: printf ("%d","text");
  Example: printf ("%d", x);
  Example_Description: Writes the value of 'x' to the stdout file.

Comments:
- Type: Single Line
  Syntax: //comments

- Type: Block
  Syntax: "/* many comments */"


Hello_World:
- Type: Example
  Example: |-
    #include<stdio.h>
    int main(int argc, char *argv[])
    {
      printf("Hello World\n");
    }
---
