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
