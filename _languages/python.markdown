---
layout: language
icon: icon-python
permalink: python/
featured: True

Language: Python
Language_Description: General purpose, high-level programming language.

Data_Types:
- Type: All
  Description: Python variable types don't have to be explicitly declared. The type declaration happens automatically when a value is assigned.
  Syntax: variable_name = value
  Example: "x = 5"

Data_Structures:
- Type: List
  Description: Holds elements in sequence. List indexing begins on zero and items do not have to be of the same data type.
  Syntax: list = [element1, element2, element3];
  Example: |
    list = ["blue", "yellow", 1, 2];
        print(list[1])
  Example_Description: The elements blue, yellow, 1, and 2 will be added to the list. The print statement will print the list item indexed on 1, which in this case is yellow.

- Type: Dictionary
  Description: A structure containing items which consist of a key and a value.
  Syntax: 'dict = {key1 : value1, key2 : value2}'
  Example: |
    dict = {'name' : 'bob', 'age' : 25}
        print(dict['name'])
  Example_Description: The value of bob is assigned to the key of name. The print statement will print the value associated with the key of name, which in this case is bob.

Flow_Control:
- Type: if
  Description: Executes code if the following statement is true.
  Syntax: |
    if statement:
        <code>
  Example: |
    if x > 5:
        print(x)
  Example_Description: The value of x will only be printed if x is greater than 5.

- Type: else
  Description: Has an if block followed by a code to be executed if the if block isn't.
  Syntax: |
    if statement:
        <code>
    else:
        <code>
  Example: |
    if x > 5:
        print(x)
    else:
        x = 6
  Example_Description: If x is greater than 5, the value of x will be printed. If it is equal to or less than 5, the value of 6 will be assigned to the variable x.

- Type: else if
  Description: Evaluates code in each statement one by one until there is a match. Only the first statement to return true will be executed!
  Syntax: |
    if statement:
        <code>
    elif statement:
        <code>
    else:
        <code>
  Example: |
    if x > 5:
        print("Greater than")
    elif x < 5:
        print("Less than")
    else:
        print("Equal to")
  Example_Description: If x is greater than 5 then the first line will execute.  If x is less than 5 then the second line will execute. If x is equal to 5 then the third line will execute.

- Type: for
  Description: Runs a piece of code on each value in the range.
  Syntax: |
    for iterating_var in sequence:
        <code>
  Example: |
    for x in range(0, 10):
        print(x)
  Example_Description: This for loop will print the numbers 0-9.

- Type: while
  Description: Executes the code repeatedly as long as the statement remains true.
  Syntax: |
    while statement:
        <code>
  Example: |
    x = 0

    while x < 5:
        x += 1
  Example_Description: This while loop will increase x by one until x is no longer less than 5.

User_Interface:
- Type: Print (Python 3.x)
  Description: Displays to stdout.
  Syntax: 'print("text", var)'
  Example: |
    x = 5
    print("The value is: ", x)
  Example_Description: 'Will print the string "The value is: 5"'

- Type: Print (Python 2.x)
  Description: Displays to stdout.
  Syntax: 'print "text", var'
  Example: |
    x = 5
    print "The value is: ", x
  Example_Description: 'Will print the string "The value is: 5"'

- Type: Input (Python 3.x)
  Description: Retrieves from stdin.
  Syntax: input("prompt")
  Example: foo = input("What your name is?")
  Example_Description: This line will output "What your name is?" and will store the users response in the variable foo.

- Type: Input (Python 2.x)
  Description: Retrieves from stdin.
  Syntax: raw_input("prompt")
  Example: foo = raw_input("What your name is?")
  Example_Description: This line will output "What your name is?" and will store the users response in the variable foo.


Comments:
- Type: Single Line
  Syntax: '# This is a comment.'

- Type: Block
  Syntax: |
          '''
          This is a large block of comments.
          They can even span multiple lines.
          '''

File_IO:
- Type: Read
  Description: Open a file for reading.
  Syntax: file_object = open(filename, access_mode)
  Example: foo = open('file.txt', 'r')
  Example_Description: This will open file.txt in read only mode.

- Type: Write
  Description: Open a file for writing.
  Syntax: file_object = open(filename, access_mode)
  Example: foo = open('file.txt', 'w')
  Example_Description: Opens file.txt for writing. Overwrites file if it exists and creates the file it does not.

Hello_World:
- Type: Example
  Example: |
    #!/usr/bin/env python
    print("Hello, world!")
---
