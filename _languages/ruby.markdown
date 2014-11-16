---
layout: language
icon: icon-ruby

Language: Ruby
Language_Description: General purpose, object oriented programming language.

Data_Types:
- Type: All
  Description: Ruby variable types don't have to be declared.
  Syntax: variable_name

Structures:
- Type: for
  Description: Loops as long as the stated conditions are met.
  Syntax: |
          for statement
          code
  Example: |
          for x in 0..5
          code
  Example_Description: X is set at value 0, the code is executed, and x will increase by a value of 1 each execution.  The loop will end once the value of x is greater than 5.

- Type: while
  Description: Repeats code as long as statement remains true.
  Syntax: |
          while statement
          code
  Example: |
            while x>5
            code
  Example_Description: This will loop as long as x is greater than 5.

- Type: until
  Description: Code executes until statement returns true.
  Syntax: |
          until statement
          code
  Example: |
            until x>5
            code
  Example_Description: The code will execute until x is greater than 5.

Functions: TODO

User_Interface:

Comments:
- Type: Single line
  Syntax: "#comment"

- Type: Block
  Syntax: |
          =begin
          many comment
          =end

Hello_World: |
            def h
            puts 'Hello, world!'
            end

---
