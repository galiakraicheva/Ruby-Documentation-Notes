# Class: String Notes

First, let's make a distinction: when we write the name of a method and # before it, we mean that this method is an instance method. If we write a name of a method and :: in front of it, we mean a class method. 

***

str % arg -> new_str
Here the string specifies some formatting (substitution) and that formatting (substitution) is applied to the arg. Arg can be a other_string or and and array/hash. It can be other_string if the string on the left of the % specifies only one substitution. If it specifies more than one substitution, arg should be an array or a hash. 
***

str * integer -> new_string
If we have "Hello" * 3, it returns a new string "HelloHelloHello"
***
 
str + str -> new_str
Concatination: "cat " + "business" returns "cat business"
***

str <=> other_str -> 1, 0, -1, or nill
It compares the two strings. 

The first string is bigger: returns 1. To determine which string is greater, the interpreter compares the first character of the first string to the first character of the second string and whichever has the lower ASCII number, is the bigger string. If they are equal, it compares the second character, etc. If two strings are identical at the beginning but one of them is longer (after the other finishes, it continues with characters), the longer one is compared to the first one. 
If the two strings are equal: returns 0. Capitalization matters. Capital letters have higher ASCII number than lower case letters.
If the second string is greater: returns -1.
If the two values are incomparable: returns nil. For example, one of them is a number, the other is a string.
***





