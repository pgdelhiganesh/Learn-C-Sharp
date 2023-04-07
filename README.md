# Learn-C-Sharp

> C# (C-Sharp) is a programming language developed by Microsoft that runs on the .NET Framework.
> C# is used to develop web apps, desktop apps, mobile apps, games and much more.

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
- **using System** means that we can use classes from the **System** namespace.
- **namespace** is used to organize your code, and it is a container for classes and other namespaces.
- **class** is a container for data and methods.
- Every C# statement ends with a semicolon ;.
- C# is **case-sensitive**: "MyClass" and "myclass" has different meaning.
- Unlike Java, the name of the C# file does not have to match the class name
- **//** Single-line command.
- **/*** Multi-line command. ***/**
---
- **int** - stores integers (whole numbers), without decimals, such as 123 or -123
- **double** - stores floating point numbers, with decimals, such as 19.99 or -19.99
- **char** - stores single characters, such as 'a' or 'B'. Char values are surrounded by single quotes
- **string** - stores text, such as "Hello World". String values are surrounded by double quotes
- **bool** - stores values with two states: true or false
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
char myLetter = 'D';         // Character
bool myBool = true;          // Boolean
string myText = "Hello";     // String
```

---
-- You can add the **const** keyword in front of the variable type, that value will not to be change in any case.
***You cannot declare a constant variable without assigning the value.** If you do, an error will occur.
```
const int myNum = 15;
myNum = 20; // error, cannot change value

const int myNumber; // error, must assign value while declaring
```
---
