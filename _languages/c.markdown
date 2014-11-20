---
layout: language
icon: icon-c

Language: C
Language_Description: General purpose, low-level programming language.

Data_Types:
- Type: int
  Description: Declares an integer.
  Syntax: int variable_name;

- Type: float
  Description:  Declares a variable that's able to harness the power of decimals (accurate up to 7 digits).
  Syntax: float variable_name;

- Type: double
  Description: Same as float, but is more exact (acurate up to 15 digits).
  Syntax: double variable_name;

- Type: char
  Description: 8 bit data type that usually contains characters.
  Syntax: char variable_name;

Flow Control:
- Type: if
  Description: Executes code if the following statement is true.
  Syntax: if(statement) {code}
  Example: if(x>5) {code}
  Example_Description: Code will only be executed if the variable x is greater than 5.

- Type: else
  Description: Follows an if block and will be executed if the if block isn't.
  Syntax: else {code}

- Type: else if
  Description: Follows an if block and will be executed if the previous if block wasn't executed and the new parameters are met.
  Syntax: else if (statement) {code}
  Example: else if (x==5) {code}
  Example_Description: Executes when previous if block doesn't and only if x equals 5.

- Type: while
  Description: Repeats code as long as statement remains true.
  Syntax: while (statement) {code}
  Example: while (x>5) {code}
  Example_Description: Code will only execute if x is greater than 5 and will keep looping until x isn't greater than 5.

- Type: do while
  Description: Code executes once and then statement is tested.  If statement remains true the do while will keep looping.
  Syntax: do while (statement) {code}
  Example: do while (x>5) {code}
  Example_Description: Code will execute once and then test if x is greater than 5.  If it is then it'll loop, if not it'll move on.

- Type: for
  Description: Loops as long as the stated conditions are met.
  Syntax: for (variable, statement, increment) {code}
  Example: for (int x=0; x>5, x++) {code}
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
  Example_Description: This would read one line of code, then jump to the case 2 label, where it would execute from there until the end of the switch statement. Note: even the code under default: will get executed.

File I/O:
- Type: fscanf
  Description: reads data from the file pointed to by fp, into the locations pinted to by the additional arguments.
  Example: |-
           int a, b;
           int *B = &b;
           char string[10];
           FILE *ifp = fopen("data.txt", "r");
           fscanf(ifp, "%d %d %s", &a, B, string);
  Example_Description: Reads in two integers and a string from the beginning of data.txt, and store them in the variables a, b, and string, respectively.
- Type: scanf
  Description: Special case of fscanf that simply uses stdin rather than an arbitrary file.
  Syntax: scanf (control_string, &var1, &var2, ...);
  Example: scanf ("%d", &x);
  Example_Description: This would read an integer from stdin and place the value of it into x
- Type fprintf
  Syntax: int fprintf ( FILE * ofp, const char * format, ... ); 
  Description: Print the message described by format and the additional arguments.
  Example: |-
           int x = 10;
           float flt = 34.10;
           char str = "Hello";
           FILE *ofp = fopen("output.txt", "w");
           printf("%s %d is an integer, %f is a number\n", str, x, flt);
  Example_Description: opens the file output.txt for writing, then writes the message "Hello 10 is an integer, 34.100000 is a number" followed by a newline character
- Type: printf
  Description: Special case of the fprintf function, that only interacts with stdout.
  Syntax: printf ("text");
  Example: printf ("%d", x);
  Example_Description: Writes the value of 'x' to the stdout file.

Comments:
- Type: Single Line
  Syntax: //comments

- Type: Block
  Syntax: "/*many comments*/"


Hello_World:
- Type: Example
  Example: |-
    #include<stdio.h>
    main()
    {
      printf("Hello World");
    }
---
