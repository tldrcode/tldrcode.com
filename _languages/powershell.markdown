---
layout: language
icon: icon-shell
permalink: powershell/
featured: False

Language: PowerShell
Language_Description: A task automation and configuration management framework from Microsoft.

Data_Types:
- Type: Variable
  Description: PowerShell variable types don't have to be declared.
  Syntax: $variable_name = value
  Example: $x = 4

- Type: Array
  Description: A series of objects all of which can be of varying types and sizes.
  Syntax: $variable_name = @(value1, value2, value3)
  Example: $myArray = @("This is a string", 56, 56.78)

- Type: Constant
  Description: Constants are values that can't be changed. For Powershell they are declared differently but can be referenced the same way as other variable with the preceding "$".
  Syntax: |
    Set-Variable –name variable_name –value variable_value –option constant
    $variable_name
  Example: |
    Set-Variable -Name myConstantString -Value "Hey this is a cool constant. This value is not easily changed" -Option Constant
    $myConstantString

Structures:
- Type: if
  Description: Executes code if the following statement is true.
  Syntax: |
    if (statement) {
      <code>
    }
  Example: |
    if (x -eq 0) {
      <code>
    }
  Example_Description: If x is equal to 0 then the code will execute.

- Type: else
  Description: Follows an if block and will be executed if the if block isn't.
  Syntax: |
    if(statement) {
      <code>
    }
    else {
      <code>
    }
  Example: |
    if($false) {
      Write-Host "I will not run"
    }
    else {
      Write-Host "I will run"
    }

- Type: else if
  Description: Follows an if block and will be executed if the previous if block wasn't executed and the new parameters are met.
  Syntax: |
    if (statement) {
      <code>
    }
    ElseIf (statement) {
      <code>
    }
  Example: |
    $x = 3
    if ($x -lt 0) {
      Write-Host "x is less than zero. This will not run."
    }
    ElseIf ($x -gt 0) {
      Write-Host "x is greater than zero. This will run."
    }
    Else {
      Write-Host "This number appears to be zero. This will not run."
    }
  Example_Description: Executes when previous if block doesn't and only if x equals 5.

- Type: For
  Description: Loops as long as the stated conditions are met.
  Syntax: |
    For (variable; statement; increment) {
      <code>
    }
  Example: |
    For ($x=1; $x -le 10; $x++) {
      Write-Host "x is equal to $x"
    }
  Example_Description: This for loop assigns the value of '1' to the variable 'x,' ensures that after each execution x increases by 1 (++), and will only work while x is less than or equal to 10.

- Type: Do While
  Description: Code executes once and then statement is tested.  If statement remains true the do while will keep looping.
  Syntax: |
    Do {
      <code>
    } While (statement)
  Example: |
    $x = 0
    Do {
      Write-Host "x is equal to $x"
      $x++
    } While ($x -ne 10)
  Example_Description: This will execute the code and loop as long as x remains less than 10.

- Type: Do Until
  Description: Code executes while statement is false.
  Syntax: |
    Do {
      <code>
    } Until (statement)
  Example: |
    $x = 0
    Do {
      Write-Host "x is equal to $x"
      $x++
    } Until ($x -eq 10)
  Example_Description: This code will loop (adding 1 to x after every execution) until x is greater than 10.

- Type: Foreach
  Description: Loops for each object in a collection.
  Syntax: |
    Foreach (placeholder_variable IN collection) {
      <code>
    }
  Example: |
    $files = Get-Childitem c:\windows
    Foreach ($file in $files){
      Write-Host "$file.name - $file.creationtime"
    }
  Example_Description: This creates an array of all the files in the 'c:\windows\' directory. It the loops through this collection and prints both the file name and creation time.

Comparison_Operators:
- Type: equals
  Syntax: "-eq"
  Example: |
    $x = 5
    if ($x -eq 5) {
      Write-Host "x is 5"
    }

- Type: not equal
  Syntax: "-ne"
  Example: |
    $x = 5
    if ($x -ne 6) {
      Write-Host "x is not equal to 6"
    }

- Type: greater than
  Syntax: "-gt"
  Example: |
    $x = 9
    if ($x -gt 5) {
      Write-Host "x is greater than 5"
    }

- Type: greater than or equal to
  Syntax: "-ge"
  Example: |
    $x = 3
    if ($x -ge 3)
    {
      Write-Host "x is greater than or equal to 3"
    }

- Type: less than
  Syntax: "-lt"
  Example: |
    $x = 34
    if ($x -lt 54) {
      Write-Host "x is less than 54"
    }


- Type: less than or equal to
  Syntax: "-le"
  Example: |
    $x = 11
    if ($x -le 11) {
      Write-Host "x is less than or equal to 11"
    }

- Type: contains
  Syntax: "-contains"
  Example: |
    $x = "cat dog pineapple pear mouse"
    if ($x -contains "apple") {
      Write-Host "This string contains apple"
    }

- Type: wildcard comparison
  Syntax: "-like"
  Example: |
    if ("powershell" -like "pow*") {
      Write-Host "The string starts with pow"
    }

- Type: wildcard comparison negation
  Syntax: "-notlike"
  Example: |
    if ("powershell" -notlike "hey") {
      Write-Host "the string is not hey"
    }

Logical_Operators:
- Type: not
  Syntax: "-not"
  Example: |
    if (-not $false) {
      Write-Host "this will always run"
    }

- Type: and
  Syntax: "-and"
  Example: |
    $x = $true
    $y = $true
    if ($x -and $y) {
      Write-Host "x and y evaluate to true"
    }

- Type: or
  Syntax: "-or"
  Example: |
    $x = $true
    $y = $false
    if ($x -or $y) {
      Write-Host "x or y evaluate to true"
    }

User_Interface:
- Type: Read-Host
  Description: Displays to stdout a prompt and then retrieves input from stdin.
  Syntax: $variable = Read-Host "prompt"
  Example: |
    $x = Read-Host "What your name is?"
    Write-Host "Hello, $x"
  Example_Description: This would output "What your name is?" and store the reply as 'x'. It would then print Hello and then whatever you typed in.

- Type: Write-Host
  Description: Displays to stdout.
  Syntax: Write-Host outputString
  Example: Write-Host "Hola!"
  Example_Description: This would output "Hola!"

Comments:
- Type: Single line
  Syntax: "#comment"

- Type: Block
  Syntax: |
    <# much comment
    This is a multi-line comment #>

Hello_World:
- Type: Example
  Example: |
    $strString = "Hello World"
    write-host $strString
---
