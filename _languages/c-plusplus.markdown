---
layout: language
icon: icon-cplusplus
permalink: c-plusplus/
featured: True

Language: C++
Language_Description: Object oriented programming language based on 'C.'
prism_name: cpp

Data_Types:
- Type: int
  Description: Declares an integer.
  Syntax: int variable_name;
  Example: int foo = 1;

- Type: float
  Description:  Declares a variable that's able to harness the power of decimals (accurate up to 7 digits).
  Syntax: float variable_name;
  Example: float foo = 3.141593;

- Type: double
  Description: Same as float, but is more precise (accurate up to 15 digits).
  Syntax: double variable_name;
  Example: double foo = 3.1415926535897;

- Type: char
  Description: 8 bit data type that usually contains characters.
  Syntax: char variable_name;
  Example: char foo = 'b';

- Type: String
  Description: An object that represents sequences of characters.
  Syntax: string variable_name;
  Example: string foo = "bar";

Structures:
- Type: if
  Description: Executes code if the following statement is true.
  Syntax: |
    if(statement) {
      <code>
    }
  Example: |
    if(x > 5) {
      cout << "I will only run if x is greater than 5";
    }
  Example_Description: Code will only be executed if the variable x is greater than 5.

- Type: else
  Description: Follows an if block and will be executed if the previous if statement evaluates to False.
  Syntax: |
    if(statement) {
      <code>
    }
    else {
      <code>
    }
  Example: |
    int foo = 0;
    if(foo == 1) {
      cout << "This will not run";
    }
    else {
      cout << "This will run";
    }

- Type: else if
  Description: Follows an if block and will be executed if the previous if statement evaluates to False and the else if statement evaluates to True.
  Syntax: |
    if(statement) {
      <code>
    }
    else if (statement) {
      <code>
    }
  Example: |
    int foo = 5;
    if(foo < 0) {
      cout << "I will not run";
    }
    else if (foo > 0) {
      cout << "but I will run";
    }
  Example_Description: Executes when previous if block doesn't and only if x equals 5.

- Type: while
  Description: Repeats code as long as statement remains true.
  Syntax: |
    while (statement) {
      <code>
    }
  Example: |
    int x = 0;
    while (x > 5) {
      cout << "x is equal to " << x << "\n";
      x++;
    }
  Example_Description: Code will only execute if x is greater than 5 and will keep looping until x isn't greater than 5.

- Type: do while
  Description: Code executes once and then statement is tested.  If statement remains true the do while will keep looping.
  Syntax: |
    do {
      <code>
    } while (statement);
  Example: |
    int x = 0;
    do {
      cout << "x is equal to " << x << "\n";
      x++;
    } while (x > 5);
  Example_Description: Code will execute once and then test if x is greater than 5.  If it is then it'll loop, if not it'll move on.

- Type: for
  Description: Loops as long as the stated conditions are met.
  Syntax: |
    for (variable, statement, increment) {
      <code>
    }
  Example: |
    for (int x=0, x>5, x++) {
      cout << "x is equal to " << x << "\n";
    }
  Example_Description: Evaluates 'x' and loops if x is greater than 5.  After each execution the value of x will increase by '+1'.

- Type: switch
  Description: The switch is a flow control statement which is best used when you need to check variable against a large number of values. Each case is what the variable is being checked against. If a case is triggered the all of the code following it is executed until it reaches the end of the switch statement or a break. If none of the cases are equal to your variable then it'll execute the default case.
  Syntax: |
    switch (variable) {
      case value1:
        <code>
        break;
      case value2:
        <code>
        break;
      default:
        <code>
    }
  Example: |
    int x = 3
    switch (x) {
      case 1:
        cout << "This one won't run";
        break;
      case 2:
        cout << "This one won't run either"
        break;
      case 3:
        cout << "This one will run though"
        break;
      default:
        cout << "This one would only run if the others didn't"
    }
  Example_Description: This switch would skip the to case 3 and execute the cout there and then hit the break.

User_Interface:
- Type: cin
  Description: Retrieves input from stdin.
  Syntax: cin >> variable1 >> variable2;
  Example: cin >> x;
  Example_Description: This would import a value for x.

- Type: cout
  Description: Displays to stdout.
  Syntax: cout << variable_or_text;
  Example: cout << "I will be written to stdout";
  Example_Description: Displays the value of "I will be written to stdout."

Comments:
- Type: Single Line
  Syntax: //comments

- Type: Block
  Syntax: |
    /*
    many comments
    and it can even be on
    multiple lines
    */

Hello_World:
- Type: Example
  Example: |
    #include <iostream>
    using namespace std;
    int main()
    {
      cout << "Hello World!";
    }
---
