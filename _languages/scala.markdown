---
layout: language
icon: icon-scala
Language: Scala
Language_Description: An object-functional language that runs on the JVM.

Declaring_Variables:
- Type: Vals
  Description: Declares a variable that cannot be changed after it is set. Types can be inferred so an explicit type doesn't need to be declared.
  Syntax: "val variablename: Type"
  Example: |
           val apple = 3
           val bacon: String = "yummy"
  Example_Description: Declares a val named apple and sets it to 3, implicitly setting its type to Int. Declares a val named bacon of type String explicitly and sets it to "yummy"

- Type: Vars
  Description: Declares a variable that can be changed after it is initially set. Type is optional as it can usually be inferred.
  Syntax: "var variablename: Type"
  Example: |
            var sauce = 4
            var wakka: String = "b"
            sauce = 5
  Example_Description: Declares a var named sauce and sets it to 4 with type Int. Declares a var named wakka and sets it to "b" with type String. Changes the value of sauce to 5.

Flow_Control:
- Type: "if statements"
  Description: Basic if else statement common to most languages
  Syntax: if(condition) {code} else if (condition2) {code} else {code}
  Example: |
          if( x == 0) {
            println("You have no bananas.")
          } else if (x < 20) {
            println(s"You have $x bananas")
          } else {
            println("Woah! You have a lot of bananas!")
          }
  Example_Description: This will print out how many bananas the use has (see println for more info).

- Type: while
  Description: Repeats code as long as statement remains true.
  Syntax: while (statement) {code}
  Example: while (x>5) {code}
  Example_Description: Code will only execute if x is greater than 5 and will keep looping until x isn't greater than 5.

- Type: match
  Description: Will execute one of a selection of cases based on the value of the variable.
  Syntax: variable match { case-statements }
  Example: |
            bacon match {
              case 1 =>
                println("There is one bacon.")
              case 2 | 3 =>
                println("Thre are two or three bacons.")
              case x if x < 10 =>
                println("There are less than ten bacons.")
              case _ =>
                println("Too many bacons to count.")
  Example_Description: Code will output the number of bacons, utilizing an if condition for > 3 < 10, and the underscore wildcard for anything not matched.

Comments:
- Type: Single Line
  Syntax: //comments

- Type: Block
  Syntax: "/* many comments */"


Hello_World:
- Type: Example
  Example: |-
    object HelloWorld extends App {
      println("Hello World")
    }
---
