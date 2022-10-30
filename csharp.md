# C# Cheatsheet

## Comments
To ensure readability of code, use the following syntax
```c#
// Place a comment here
```
On the topic of readability - it is advised that camel case is used when defining functions

## 'using'
'using' is used to import packages such as Linq or IO for use in programs. It is used as such
```c#
using System.Linq;
```

## Types and Conversion/Parsing
### Types
**Data Type** | **Size** | **Description** 
--- | --- | ---
int | 4 bytes | Stores whole numbers from -2,147,483,648 to 2,147,483,647
long | 8 bytes | Stores whole numbers from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807
float | 4 bytes | Stores fractional numbers. Sufficient for storing 6 to 7 decimal digits
double | 8 bytes | Stores fractional numbers. Sufficient for storing 15 decimal digits
bool | 1 bit | Stores true or false values
char | 2 bytes | Stores a single character/letter, surrounded by single quotes
string | 2 bytes per char | Stores a sequence of characters, surrounded by double quotes

## Lists
```c#
using System.Collections.Generic; // Imports the package needed for lists to function
var list = new List<int>(); // Generates an empty list of integers
list.Add(12); // Adds the integer '12' to the list
Console.WriteLine(list[0]); // Prints index 0 of the lest to the console - in this case this returns 12, to the command line
Console.WriteLine(list.Count()); //Prints the number of entries in the list, to the command line
Console.WriteLine(list.Sum()); //Prints the sum of a list to the command line
Console.WriteLine(list.IndexOf(12)); //Prints the index of the entry '12' to the command line. -1 is returned if no entry is found.
list.Sort(); // Sorts the list, either alphabetically in the case of strings, or in order of magnitude from smallest to greatest, in the case of numerical values.

```

### Conversion/Parsing
The Convert function can be used to convert variables to different types, shown below to convert a variable to a 16-bit integer, however the Int16 can be replaced with a variety of formats.
```c#
int x = Convert.ToInt16(variable);
```
The TryParse function converts string representations of integers to integer format, returning a boolean as to whether or not they can be converted.

Input:
```c#
bool res;
int a;
string myStr = "12";
res = int.TryParse(myStr, out a);
Console.WriteLine("String is a numeric representation: "+res);
```
Output:
```
String is a numeric representation: True
```

## Functions

Functions take the following format:
```c#
static int add(int x, int y)
{
    return x + y;
}
```
Unlike Python, C# requires that functions state their output format - void must be used if there is no output returned, and data types (Integer, Decimal, Double, etc) must be specified at the start of a function.

## Logical operators
```c#
if (a||b) return true; // a or b
if (a&&b) return true; // a and b
if (a^b) return true; // a xor b
if (a==b) return true; // a equals b
if (a!=b) return true; // a not equals b
```
# Loops 

'while' loops executes a piece of code repeatedly whilst a statement is true.
```c#
while (True) Console.WriteLine("True");
```
'for' loops include three statements - the first is executed once, the second defines the condition for the code block, and the third is executed each time the after the code block has been executed. The format is as such
```c#
for (statement 1; statement 2; statement 3) 
{
  // code block to be executed
}
```
'foreach' loops iterate through lists or arrays, and are used in the following format
```c#
var list = new List<int> {1,2,3,4,5};
foreach(int a in list) { Console.WriteLine(a); }
```

# The Conditional/Tertiary Operator
