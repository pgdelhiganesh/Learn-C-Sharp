# Learn-C-Sharp

C# (C-Sharp) is a programming language developed by Microsoft that runs on the .NET Framework.  
C# is used to develop web apps, desktop apps, mobile apps, games and much more.

```
using System;

namespace HelloWorld
{
  class Program
  {
    static void Main(string[] args)
    {
      Console.WriteLine("Hello World!");    

      // Create a string variable and get user input from the keyboard and store it in the variable
      string userName = Console.ReadLine();
      // Print the value of the variable (userName), which will display the input value
      Console.WriteLine("Username is: " + userName);
      
      // The Console.ReadLine() method returns a string. Therefore, cannot read like int or other datatype
      Console.WriteLine("Enter your age:");
      int age = Convert.ToInt32(Console.ReadLine());
      Console.WriteLine("Your age is: " + age);
    }
  }
}
```
---
+ **using System** means that we can use classes from the **System** namespace.
+ **namespace** is used to organize your code, and it is a container for classes and other namespaces.
+ **class** is a container for data and methods.
+ Every C# statement ends with a semicolon ;.
+ C# is **case-sensitive**: "MyClass" and "myclass" has different meaning.
+ Unlike Java, the name of the C# file does not have to match the class name
+ **//** Single-line command.
+ **/*** Multi-line command. ***/**
---
+ The general rules for naming variables are:
```
// Names can contain letters, digits and the underscore character (_)  
// Names must begin with a letter  
// Names should start with a lowercase letter and it cannot contain whitespace  
// Names are case sensitive ("myVar" and "myvar" are different variables)  
// Reserved words (like C# keywords, such as int or double) cannot be used as names
```
---

Data Type | Size | Description
------------- | ----- | ----------
int | 4 bytes | Stores whole numbers from -2,147,483,648 to 2,147,483,647
long | 8 bytes | Stores whole numbers from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807
float | 4 bytes | Stores fractional numbers. Sufficient for storing 6 to 7 decimal digits
double | 8 bytes | Stores fractional numbers. Sufficient for storing 15 decimal digits
bool | 1 bit | Stores true or false values
char | 2 bytes | Stores a single character/letter, surrounded by single quotes
string | 2 bytes per character	| Stores a sequence of characters, surrounded by double quotes

```
int myNum = 5;               // Integer (whole number)
double myDoubleNum = 5.99D;  // Floating point number
long myLongNum = 15000000000L;
char myLetter = 'D';         // Character
bool myBool = true;//false          // Boolean // will print **True** / **False**
string myText = "Hello";     // String
//A floating point number can also be a scientific number with an "e" to indicate the power of 10:
float f1 = 35e3F; // will print 35000
double d1 = 12E4D; // will print 120000
```
---
+ You can add the **const** keyword in front of the variable type, that value will not to be change in any case.  
  Cannot declare a constant variable without assigning the value. If you do, an error will occur.
```
const int myNum = 15;
myNum = 20; // error, cannot change value

const int myNumber; // error, must assign value while declaring
```
---
+ **Implicit Type Casting** (automatically) - converting a smaller type to a larger type size  
char -> int -> long -> float -> double
+ **Explicit Type Casting** (manually) - converting a larger type to a smaller size type  
double -> float -> long -> int -> char
---
Operator | Name | Description | Example
-------- | ---- | ----------- | -------
**-** | Subtraction | Subtracts one value from another | x - y	
\* | Multiplication | Multiplies two values | x * y	
/ | Division | Divides one value by another | x / y	
% | Modulus | Returns the division remainder | x % y	
++ | Increment | Increases the value of a variable by 1 | x++	
-- | Decrement | Decreases the value of a variable by 1 | x--

Operator | Example | Same As
-------- | ---- | ----------
= | x = 5 | x = 5	
+= | x += 3 | x = x + 3	
-= | x -= 3 | x = x - 3	
*= | x *= 3 | x = x * 3	
/= | x /= 3 | x = x / 3	
%= | x %= 3 | x = x % 3	
&= | x &= 3 | x = x & 3	
|= | x |= 3 | x = x | 3	
^= | x ^= 3 | x = x ^ 3	
\>>= | x >>= 3 | x = x >> 3
<<= | x <<= 3 | x = x << 3

Operator | Example | Same As
-------- | ---- | ----------
== | Equal to | x == y	
!= | Not equal | x != y	
\> | Greater than | x > y	
< | Less than | x < y	
\>= | Greater than or equal to | x >= y	
<= | Less than or equal to | x <= y

Operator | Example | Description | Example
-------- | ------- | ----------- | -------
&& | Logical and | Returns True if both statements are true | x < 5 &&  x < 10	
\|\| | Logical or | Returns True if one of the statements is true | x < 5 || x < 4	
! | Logical not | Reverse the result, returns False if the result is true | !(x < 5 && x < 10)

---
String Math
+ Console.WriteLine(Math.Max(5, 10)); //5
+ Console.WriteLine(Math.Min(5, 10)); //5
+ Console.WriteLine(Math.Sqrt(64)); //8
+ Console.WriteLine(Math.Abs(-4.7)); //4.7
+ Console.WriteLine(Math.Round(9.99)); //10
---
String Interpolation
Also note that you have to use the dollar sign ($) when using the string interpolation method.
```
String interpolation was introduced in C# version 6.
string firstName = "John";
string lastName = "Doe";
string name = $"My full name is: {firstName} {lastName}";
Console.WriteLine(name);
```
---
Array
```
// Create an array of four elements, and add values later
string[] cars = new string[4];

// Create an array of four elements and add values right away 
string[] cars = new string[4] {"Volvo", "BMW", "Ford", "Mazda"};

// Create an array of four elements without specifying the size 
string[] cars = new string[] {"Volvo", "BMW", "Ford", "Mazda"};

// Create an array of four elements, omitting the new keyword, and without specifying the size
string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};

// Sort a string
string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
Array.Sort(cars);
foreach (string i in cars)
{
  Console.WriteLine(i);
}

// Sort an int
int[] myNumbers = {5, 1, 8, 9};
Array.Sort(myNumbers);
foreach (int i in myNumbers)
{
  Console.WriteLine(i);
}
```
```
using System;
using System.Linq;

namespace MyApplication
{
  class Program
  {
    static void Main(string[] args)
    {
      int[] myNumbers = {5, 1, 8, 9};
      Console.WriteLine(myNumbers.Max());  // returns the largest value
      Console.WriteLine(myNumbers.Min());  // returns the smallest value
      Console.WriteLine(myNumbers.Sum());  // returns the sum of elements
    }
  }
}
```
---
Multidimensional Arrays
```
int[,] numbers = { {1, 4, 2}, {3, 6, 8} };
//Good to know: The single comma [,] specifies that the array is two-dimensional.
//A three-dimensional array would have two commas: int[,,]
```
 | Column 0 | Column 1 | Column 2
-------- | ---- | ----------
row 0 | 1 | 4 | 2
row 1 | 3 | 6 | 8
```
//Access Elements of a 2D Array
int[,] numbers = { {1, 4, 2}, {3, 6, 8} };
Console.WriteLine(numbers[0, 2]);  // Outputs 2

//Change Elements of a 2D Array
int[,] numbers = { {1, 4, 2}, {3, 6, 8} };
numbers[0, 0] = 5;  // Change value to 5
Console.WriteLine(numbers[0, 0]); // Outputs 5 instead of 1

//Loop Through a 2D Array
foreach (int i in numbers)
{
  Console.WriteLine(i);
}
//(or using for loop)
//for (int i = 0; i < numbers.GetLength(0); i++) 
//{ 
//  for (int j = 0; j < numbers.GetLength(1); j++) 
//  { 
//    Console.WriteLine(numbers[i, j]); 
//  } 
//}  
Output:
1
4
2
3
6
8
```
---
C# Methods

//Named Arguments

It is also possible to send arguments with the key: value syntax.

That way, the order of the arguments does not matter:
```
static void MyMethod(string child1, string child2, string child3) 
{
  Console.WriteLine("The youngest child is: " + child3);
}

static void Main(string[] args)
{
  MyMethod(child3: "John", child1: "Liam", child2: "Liam");
}

// The youngest child is: John
```
//Method Overloading (With method overloading, multiple methods can have the same name with different parameters)

Note: Multiple methods can have the same name as long as the number and/or type of parameters are different.
```
int MyMethod(int x)
float MyMethod(float x)
double MyMethod(double x, double y)
```
---
