---
#To use this template please rename the file to the langugage name with the
#extension of ".markdown"

#This allows for the language's page to be rendered correctly
layout: language

#Specifiy the icon name here - You can find all available here - http://mfizz.com/oss/font-mfizz
#If you know of other better font icon libraries we should use tell us
icon: icon-c

# Permalink - the permanent link for this language for a nice looking URL.
# Should just be language but all lower case - needs trailing /
permalink: c/

#Basic language details
Language: C
Language_Description: General purpose, low-level programming language.

#All the data for the language that gets populated on the rendered page
#This is all in YAML. The basic structure is specified below. You can add new
#sections and it should automatically add a new section on the page. The section
#titles will be the what specified below with all the _ replaced with spaces.

#If you need any with YAML this page should help http://www.yaml.org/refcard.html
#You can be really awesome and remake this page for TLDR code. *wink wink*

Data_Types:
- Type: Basic variables
  Description: Declares a variable of one of the basic built-in types.
  Syntax: typename variablename
  Example: |
           int x, y=3
           float f;
           char c;
  Example_Description: declares two integers, x and y. y is initialized to 3. declares a floating point variable, f and a char(1 byte) variable c.

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
