---
layout: language
icon: icon-shell

Language: PowerShell
Language_Description: A task automation and configuration management framework from Microsoft.

Data_Types:
- Type: Variable
  Description: PowerShell variable types don't have to be declared.
  Syntax: $variable_name = value

- Type: Array
  Description: A series of objects all of which are the same size and type.
  Syntax: $variable_name = value, value2, value3

- Type: Constant
  Description: Constants are created without a '$,' but are referenced with a '$.'
  Syntax: Set-Variable –name variable_name –value variable_value –option constant

Structures:
- Type: if
  Description: Executes code if the following statement is true.
  Syntax: if (statement) {code}
  Example: if (x -eq 0) {code}
  Example_Description: If x is equal to 0 then the code will execute.

- Type: else
  Description: Follows an if block and will be executed if the if block isn't.
  Syntax: else {code}

- Type: else if
  Description: Follows an if block and will be executed if the previous if block wasn't executed and the new parameters are met.
  Syntax: elseif (statement)
  Example: elseif ($x -eq 5) {code}
  Example_Description: Executes when previous if block doesn't and only if x equals 5.

- Type: For
  Description: Loops as long as the stated conditions are met.
  Syntax: For (variable; statement; increment) {code}
  Example: For ($x=1; $x -le 10; $x++) {code}
  Example_Description: This for loop assigns the value of '1' to the variable 'x,' ensures that after each execution x increases by 1 (++), and will only work while x is less than or equal to 10.

- Type: Do While
  Description: Code executes once and then statement is tested.  If statement remains true the do while will keep looping.
  Syntax: |
          Do {variable; increment}
          While (statement)
  Example: |
          Do {$x; $x++}
          While ($x -lt 10)
  Example_Description: This will execute the code and loop as long as x remains less than 10.

- Type: Do Until
  Description: Code executes until statement returns true.
  Syntax: |
          Do {variable; increment}
          Until (statement)
  Example: |
          Do {$x; $x++}
          Until ($x -gt 10)
  Example_Description: This code will loop (adding 1 to x after every execution) until x is greater than 10.

- Type: Foreach
  Description: Loops for each object in a collection.
  Syntax: |
          Foreach (object in collection_of_objects)
          {code_block}
  Example: |
          Foreach ($x in Get-Childitem c:\windows)
          {$x.name; Sx.creationtime}
  Example_Description: This uses a temporary object (x) to read files from 'c:\windows,' name them, and add their creation time.

Functions: TODO

User_Interface:
- Type: Read-Host
  Description: Displays to stdout and retrieves from stdin.
  Syntax: $variable = Read-Host "prompt"
  Example: $x = Read-Host "What your name is?"
  Example_Description: This would output "What your name is?" and store the reply as 'x.'

- Type: Write-Host
  Description: Displays to stdout.
  Syntax: Write-Host output
  Example: Write-Host "Hola!"
  Example_Description: This would output "Hola!"

Comments:
- Type: Single line
  Syntax: #comment

- Type: Block
  Syntax: <# much comment #>

Hello_World: |
            $strString = "Hello World"
            write-host $strString
---
