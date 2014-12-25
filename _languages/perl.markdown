---
layout: language
icon: icon-perl
permalink: perl/
featured: True

Language: Perl
Language_Description: General purpose programming language that specializes in text processing.

Data_Structures:
- Type: Basic Data Types
  Description: Perl variable types don't have to be explicitly declared. The type declaration happens automatically when a value is assigned.
  Syntax: $variable_name = value;
  Example: "$x = 5;"

- Type: Array
  Description: A series of objects held in a series with an index starting at 0.
  Syntax: |
    @variable = (element1, element2, element3);
  Example: |
    @names = ("larry", "martha", "bob", "lisa");
    print $names[1];
  Example_Description: The example will assign the values to the names array, and then will print out the value stored in the array indexed on position 1, which in this case is martha.

- Type: Hash
  Description: A type of associative array that stores elements in key value pairs.
  Syntax: |
    %variable = (key, value, key, value);
  Example: |
    %ages = ("larry", 23, "martha", 21);
    print $data{'larry'};
  Example_Description: The example will assign the key value pairs to the hash and then will print the value stored in the ages hash indexed on the key of larry, which in this case is 23.

Flow_Control:
- Type: if
  Description: Executes code if the following statement is true.
  Syntax: |
    if(condition){
      <code>
    }
  Example: |
    $x = 6;
    if($x > 5){
      print "$x is greater than 5\n";
    }
  Example_Description: 'The phrase "6 is greater than 5" will print because the value of x is greater than 5'

- Type: else
  Description: Has an if block followed by a block of code to be executed if the if block is false.
  Syntax: |
    if(condition){
      <code>
    }
    else{
      <code>
    }
  Example: |
    $x = 4;
    if($x > 5){
      print "$x is greater than 5\n";
    }
    else{
      print "$x is less than or equal to 5\n";
    }
  Example_Description: Since the value of $x is less than 5, the if statement will return false, and the else code will be executed.

- Type: else if
  Description: Evaluates code in each statement one by one until there is a match. Only the first statement to return true will be executed.
  Syntax: |
    if(condition){
      <code>
    }
    elsif(condition){
      <code>
    }
    else{
      <code>
    }
  Example: |
    $x = 4;
    if($x > 5){
      print "$x is greater than 5\n";
    }
    elsif($x < 5){
      print "$x is less than 5\n";
    }
    else{
      print "$x is equal to 5\n";
    }
  Example_Description: 'The line "4 is less than 5" will print because the second condition is the first condition that is true.'

- Type: while
  Description: Repeats a piece of code while a given condition is true. Checks statement before each run, and will only execute if the statement is true.
  Syntax: |
    while(condition){
      <code>
    }
  Example: |
    $x = 4;
    while($x < 5){
      print "$x is less than 5\n";
      $x++;
    }
  Example_Description: The loop will execute once, as the condition is met for the first iteration of the loop. The value of x is incremented by one during the first iteration, making the second iteration return false.

- Type: until
  Description: Repeats a piece of code until a given condition is true. Checks statement before each run, and will only execute if the statement is false.
  Syntax: |
    until(condition){
        <code>
    }
  Example: |
      $x = 4;
      until($x > 5){
        print "$x is less than 5\n";
        $x++;
      }
  Example_Description: Since the first time the condition is checked returns false, the loop will execute. After the variable is incremented, the loop does not execute a second time because the condition returns true.

- Type: for
  Description: Iterates a set of statements for a predetermined number of times.
  Syntax: |
    for(initial_value; condition; increment){
      <code>
    }
  Example: |
    for($x = 0; $x < 3; $x++){
      print "$x\n";
    }
  Example_Description: 'This loop will print the values: 0, 1, and 2 because the initial value is zero, each iteration increments the variable by one, and the loop executes until $x is less than 3.'

- Type: foreach
  Description: Iterates over a list of elements, performing a set of statements on each element of the list.
  Syntax: |
    foreach var (list){
      <code>
    }
  Example: |
    @name_list = ("alice", "bob")
    foreach $name (@name_list){
      print "$name\n";
    }
  Example_Description: This loop will print out each value in the name_list array, which in this case is alice and bob.

- Type: do while
  Description: Similar to a while statement, except the condition is checked at the end of the loop rather than the beginning. The loop will always execute once.
  Syntax: |
    do {
      <code>
    } while(condition);
  Example: |
    $x = 5;
    do {
      print "$x\n";
    } while($x < 4);
  Example_Description: This loop will only execute once, since the condition is not checked until the end of the loop. Since the condition is false, the loop will not continue.

User_Interface:
- Type: Print
  Description: Displays objects to stdout.
  Syntax: |
    print "content";
  Example: |
    $x = 5;
    print "$x more days until vacation.\n";
  Example_Description: 'The example will print "5 more days until vacation." The \n will add a newline character, causing the next print statement to be printed on the following line.'

- Type: User Input
  Description: Retrieves user input from stdin.
  Syntax: |
    $variable = <STDIN>;
  Example: |
    $x = <STDIN>;
    chomp $x;
  Example_Description: The variable $x will be assigned one line of user input. The comp function will remove the trailing new line character.

Comments:
- Type: Single Line
  Syntax: |
    # This is a single line comment.

- Type: Block
  Syntax: |
    =begin comment
    This is a multi-line comment in perl.
    The begin and end directive starts end ends the comment block.
    The cut directive tells the interpreter to begin expecting additional perl code.
    =end comment
    =cut

File_IO:
- Type: Read
  Description: Used to open a file for reading.
  Syntax: |
    open HANDLE, '<', 'filename';
  Example: |
    open INPUT, '<', 'file.txt';
  Example_Description: This open statement will open the file file.txt in read-only mode and assign the handle INPUT to be used to access the file.

- Type: Write
  Description: Used to open a file for writing.
  Syntax: |
    open HANDLE, '>', 'filename';
  Example: |
    open OUTPUT, '>', 'file.txt';
  Example_Description: This open statement will open the file file.txt in write mode and assign the handle OUTPUT to be used to access the file. A single carrot is used to overwright existing content, where two carrots (>>) are used to append to the file.

Hello_World:
- Type: Example
  Example: |
    #!/usr/bin/perl
    print "Hello, world!\n";
---
