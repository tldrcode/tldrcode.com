---
layout: language
icon: icon-python

Language: Python
Language_Description: General purpose, high-level programming language.

Data_Types:
- Type: All
  Description: Python variable types don't have to be declared.  Simply creating a variable and setting it equal (with '=') to a value works.
  Syntax: variable_name = value

Structures:
- Type: if
  Description: Executes code if the following statement is true.
  Syntax: "if statement: code"
  Example: "if x>5: code"
  Example_Description: The code will only execute if x is greater than 5.

- Type: if else
  Description: Has an if block followed by a code to be executed if the if block isn't.
  Syntax: |
          if statement: code
          else: code
  Example: |
          "if x>5: code
          else: code"
  Example_Description: If x is greater than 5 then the code on the first line will be executed.  If x isn't greater than 5 then the second line of code will be executed.

- Type: if elseif
  Description: First evaluates the parameters attached to 'if.' If that returns false then the code moves on to evaluate the 'else if.' If the else if also returns false then the program will execute the last code (the part following 'else').  Only the first statement to return true will be executed!
  Syntax: |
          if statement: code
          else if statement: code
          else: code
  Example: |
          if x>5: code
          else if x<5: code
          else: code
  Example_Description: If x is greater than 5 then the first line will execute.  If x is less than 5 then the second line will execute. If x is 5 then the third line will execute.

- Type: for
  Description: Loops as long as the stated conditions are met.
  Syntax: "for variable in range (start [,stop [,increment]]): code"
  Example: "for x in range (10, 0, -2): code"
  Example_Description: Variable 'x' is assigned a value of 10 and after each execution of the code x's value is decreased by 2.  The code will execute until x equals 0.

- Type: while
  Description: Executes the code repeatedly as long as the statement remains true.
  Syntax: "while statement: code"
  Example: "while x>5: code"
  Example_Description: This code would be executed as long as x is greater than 5 and would repeatedly execute until x wasn't greater than 5.

Functions: TODO

User_Interface:
- Type: print
  Description: Displays to stdout.
  Syntax: print "text"

- Type: raw_input
  Description: Retrives from stdin.
  Syntax: raw_input("prompt")
  Example: raw_input("What your name is?")
  Example_Description: Code will output "What your name is?" and give the chance for text to be input.


Comments:
- Type: Single Line
  Syntax: '#comments'

- Type: Block
  Syntax: |
          '''
          comments
          '''

Hello_World: print "Hello world!"
---
