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
```
int myNum = 5;
double myDoubleNum = 5.99D;
char myLetter = 'D';
bool myBool = true;
string myText = "Hello";
```
---
-- If you don't want others (or yourself) to overwrite existing values, you can add the **const** keyword in front of the variable type.
You cannot declare a constant variable without assigning the value. If you do, an error will occur: **A const field requires a value to be provided**.
```
const int myNum = 15;
myNum = 20; // error
```
---