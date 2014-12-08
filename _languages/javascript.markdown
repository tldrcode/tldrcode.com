---
layout: language
icon: icon-javascript
permalink: javascript/
featured: True

Language: JavaScript
Language_Description: Object oriented programming language mostly used to create interactive effects within web browsers.

Data_Types:

- Type: Number
  Description: An integer or floating-point value. In JavaScript there is no distincion between the 2 (internally they are all represented as floating point values).
  Syntax: var1 = 1; var2 = 1.2;

- Type: String
  Description: A sequence of unicode characters used to represent text.
  Syntax: var3 = 'var';

- Type: Boolean
  Description: A true/false value.
  Syntax: var0 = false; var1 = true;


Structures:

- Type: if
  Description: Executes code if the following statement is true.
  Syntax: if(statement) {code}
  Example: if(x>5) {code}
  Example_Description: Code will only be executed if the variable x is greater than 5.

- Type: else
  Description: Follows an if block and will be executed if the if block isn't.
  Syntax: if(statement){...} else{code}
  Example: |-
      int i = 10;
      if(i == 10){
        code
      }else{
        code
      }
  Example_Description: Else code executes if i is not equal to 10.

- Type: else if
  Description: Follows an if block and will be executed if the previous if block wasn't executed and the new parameters are met.
  Syntax: if(statment) {code} else if(statement) {code}
  Example: |-
      int x = 5;
      if(x == 10) {
        code
      }else if (x == 5) {
        code
      }
  Example_Description: Executes when previous if block doesn't and only if x equals 5.

- Type: while
  Description: Repeats code as long as statement remains true.
  Syntax: while (statement) {code}
  Example: while (x>5) {code}
  Example_Description: Code will only execute if x is greater than 5 and will keep looping until x isn't greater than 5.

- Type: do while
  Description: Code executes once and then statement is tested.  If statement remains true the do while will keep looping.
  Syntax: do {code} while (statement)
  Example: do {code} while (x>5)
  Example_Description: Code will execute once and then test if x is greater than 5.  If it is then it'll loop, if not it'll move on.

- Type: for
  Description: Loops as long as the stated conditions are met.
  Syntax: for (variable; statement; increment) {code}
  Example: for (x; x>5; x+1) {code}
  Example_Description: Evaluates 'x' and loops if x is greater than 5.  After each execution the value of x will increase by '1'.

- Type: switch
  Description: Allows specific code to be used. Variable used must be an integer and the 'vars' must be constant. The switch will jump to the first case that's equal to your stated variable and do the rest of the codes from there (so it'll skip everything before the first case used).  If none of the cases are equal to your variable then it'll only execute the last section of code (the code following 'default').
  Syntax: |
          switch (variable)
          {case var1: code; break;
          case var2: code; break;
          default: code; break;}
  Example: |
          int x = 5
          var1 = 4
          var2 = 5
          switch (x)
            {case var1: code; break;
            case var2: code; break;
            default: code; break;}
  Example_Description: This switch would skip the first line of code and execute everything after that.


Functions:

- Type: Anonymous function
  Description: An unnamed function that is called at runtime.
  Syntax: function (parameters) { code }
  Example: function (var1, var2)
            {
              console.log (var1 + var2);
            }

- Type: Named function
  Description: A function given a name, to be executed when explicitly called.
  Syntax: function myFunction (parameters) { code }
  Example: function addThis (var1, var2)
                      {
                        var total = var1 + var 2;

                        return total;
                      }
            addThis(1, 2);

- Type: Immediately invoked function expression (IIFE)
  Description: A function invoked at runtime, creating its own scope.
  Syntax: (function(){ code })();
  Example: (function(){ console.log('code'); })();


User_Interface:

- Type: Prompt
  Description: Displays as a prompt.
  Syntax: window.prompt (text_or_prompt, default_value);
  Example: window.prompt ("What is your name?, "Type your name here");
  Example_Description: Displays "What is your name?" and auto-fills the textbox with "Type your name here."

- Type: Alert
  Description: Displays message that must be accepted to continue.
  Syntax: window.alert ("text");
  Example: window.alert ("Meth, not even once.");
  Example_Description: This will display a message reading "Meth, not even once" and will require the user to acknowledge the message to continue.


Comments:

- Type: Single Line
  Syntax: // comments

- Type: Block
  Syntax: "/* many comments */"


Hello_World:
- Type: Example
  Example: |-
    <!DOCTYPE HTML>
    <html>
      <body>
        <p>Header...</p>
        <script>
          window.alert('Hello, World!');
        </script>
        <p>...Footer</p>
      </body>
    </html>
---
