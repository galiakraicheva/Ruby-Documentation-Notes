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

str[index] -> new string or nil
This method threats the string as if it were an array and returns a substring with the character that was at this "index" position in the original string. As with arrays, counting starts at 0. Returns nil if there is no such an index. 
***

str[start, length] -> new string or nil
This methods also takes a substring. The start index is the index of the first character of the substring and length is the number of characters included afterwards. So the character with the start index is also included. 
***

capitalize -> new string
Returns a new string with the first letter capitalized and all the other letters in lowercase. On the contrary, the method #capitalize! returns the same string modified or nil if there were no modifications to the string. 
***

chars -> an_array
Returns an array of all the characters of the string. 
***

chomp -> new_string
Removes the new line symbol at the end of the line. In most operating systems it is /n but in some it is /n/r or some other combination. The full name of this method is chomp(separator=$/), which means that in the separator argument you can specify how the new line symbol looks like. By default, the separator is $/ so if you don't provide a separator, $/ will be used. 4/ is a global variable which contains the new line character of the operating system. 
Example:
"hello".chomp -> "hello"
"hello\n".chomp -> "hello"
"hello \n there".chomp -> "hello \n there"
"hello".chomp("llo") -> "he"
***

chop -> new_string
Return a substring of the original string without the last character. 
***

chr -> string
Returns a substring with the first character of the string.
***

clear -> empty_string
Removes all the content of the string and returns the string empty.





