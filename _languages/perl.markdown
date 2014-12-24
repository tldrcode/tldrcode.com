---
layout: language
icon: icon-perl
permalink: perl/
featured: True

Language: Perl
Language_Description: General purpose programming language that specializes in text processing.

Data_Types:
- Type: All
  Description: Perl variable types don't have to be explicitly declared. The type declaration happens automatically when a value is assigned.
  Syntax: $variable_name = value
  Example: "$x = 5;"

Data_Structures:
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
---
