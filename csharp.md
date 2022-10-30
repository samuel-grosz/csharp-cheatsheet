# C# Cheatsheet

## Comments
To ensure readability of code, use the following syntax
```c#
// Place a comment here
```
On the topic of readability - it is advised that camel case is used when defining functions

## Types and Conversion
The Convert function can be used to convert variables to different types, shown below to convert a variable to a 16-bit integer.
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

