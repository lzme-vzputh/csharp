# vzputh
---

# C# Programming Guide

## 1. Introduction
   - Overview of C#: its usage in desktop, web, and mobile applications.
   - Why C# is a popular and versatile programming language.
   - Structure of a C# program.

---

## 2. Installing Visual Studio 2022
   - Step-by-step guide to downloading and installing Visual Studio 2022 Community Edition.
   - Set up a .NET development environment.

---

## 3. Creating Your First Project
   - **Steps**:
     1. Open Visual Studio.
     2. Select "Create a new project".
     3. Choose "Console App (.NET Core or .NET Framework)".
     4. Name the project "HelloWorldApp" and click "Create".

---

## 4. Hello VZPUTH!
   - Basic program to print "Hello, World!" to the console.
   ```csharp
   using System;

   class Program
   {
       static void Main()
       {
            Console.WriteLine("I crush on you!"); // with new line
            Console.Write("Mea Hg ><"); // without new line
       }
   }
   ```

---

## 5. Numeric Data Types
   - Overview of `int`, `double`, `float`, and `decimal`.
   ```csharp
   int age = 20;
Console.WriteLine("int\n"+age);
Console.WriteLine(int.MaxValue);
Console.WriteLine(int.MinValue);


long bigNumber = 876533456L;
Console.WriteLine("\n long\n" + bigNumber);
Console.WriteLine(long.MaxValue);
Console.WriteLine(long.MinValue);

decimal money = 9000M;
Console.WriteLine("\n decimal\n" + money);
Console.WriteLine(decimal.MaxValue);
Console.WriteLine(decimal.MinValue);

//  float 

float hight = 1.70F;
Console.WriteLine("\n float\n"+hight);
Console.WriteLine(float.MaxValue);
Console.WriteLine(float.MinValue);

double wight = 0.3455432D;
Console.WriteLine("\n double\n"+wight);
Console.WriteLine(double.MaxValue);
Console.WriteLine(double.MinValue);
   ```

---

## 6. Text-Based Data Types
   - Using `string` and `char`.
   ```csharp
   string name = "vzputh";
   char gender = 'M';

   // for output we can use two option 

   Console.WriteLine($"My name's {name}. Gender {gender}.");// C# Style 

   Console.Write("My name's " +name+ " Gender:" + gender); // Java Style
   ```

---

## 7. Converting String to Numbers
   - Convert strings to integers or other numeric types.
   ```csharp
string textAge ="-500";
Console.WriteLine(textAge);
           
int A =  Convert.ToInt32(textAge) + 600;
Console.WriteLine(A);



double pi = 3.6;
int a = Convert.ToInt32(pi);
int b = Convert.ToInt16(pi);
Console.WriteLine(a);
Console.WriteLine(b);


string couple = "9.87653";
float x = Convert.ToSingle( couple );
Console.WriteLine(x); 
   ```

---

## 8. Boolean Data Type
   - `bool` type for true or false values.
   ```csharp
   bool a = true,
        b= false;
   Console.WriteLine(a); //true
   Console.WriteLine(b); //false
// converted Boolean to Integer
   int x = Convert.ToInt32(a),
       y = Convert.ToInt32(b);
   Console.WriteLine(x); // x=1
   Console.WriteLine(y); // y=0
   ```

---

## 9. Operators
   - **Arithmetic operators**: `+`, `-`, `*`, `/`, `%`
   - **Comparison operators**: `==`, `!=`, `<`, `>`
   - **Logical operators**: `&&`, `||`, `!`
   ```csharp
      int age = 20;  
      Console.WriteLine(age);
      age++;
      Console.WriteLine(age); // age = 21
      age--;
      Console.WriteLine(age);// age = 20 

      // now age = 20 we can use " age = age + 1" it's the same " age++"

      age = age + 5; // age = 20 + 5
      Console.WriteLine(age); 
      age += 5; // age = 25 + 5
      Console.WriteLine(age); 
      // + - * / can use all

      age /= 5;
      Console.WriteLine(age);
      // use in string

      string name = "vzputh";
      name += " is m'nus s'mos";
      Console.WriteLine(name);
      // in Char when sum it use unicode in alphabet
      char ch = 'x';
      ch += 'y'; //  ñ
      Console.WriteLine(ch);
   ```

---

## 10. Remainder
   - Using the `%` operator to find remainders.
   ```csharp
   int remainder = 10 % 3;
   ```

---

## 11. `var` Keyword
   - Implicit typing with `var`.
   ```csharp
   var name = "Alice"; // inferred as string
   var number = 123;   // inferred as int
   ```

---

## 12. `const` Keyword
   - Declaring constants.
   ```csharp
   const double PI = 3.14159;
   ```

---

## 13. Exercise - Storing User Data
   - Collect and display user data.
   ```csharp
   string name = "John";
   int age = 28;
   Console.WriteLine($"Name: {name}, Age: {age}");
   ```

---

## 14. Exercise - Odd/Even Checker
   - Determine if a number is odd or even.
   ```csharp
   int number = 4;
   if (number % 2 == 0)
       Console.WriteLine("Even");
   else
       Console.WriteLine("Odd");
   ```

---

## 15. Console Input/Output
   - Use `Console.ReadLine()` and `Console.WriteLine()`.
   ```csharp
   Console.Write("Enter your name: ");
   string name = Console.ReadLine();
   Console.WriteLine($"Hello, {name}!");
   ```

---

## 16. If Statements
   - Conditional logic with `if`.
   ```csharp
   if (age > 18)
       Console.WriteLine("Adult");
   ```

---

## 17. Switch Statements
   - Switch-case structure.
   ```csharp
   int day = 3;
   switch (day)
   {
       case 1: Console.WriteLine("Monday"); break;
       case 2: Console.WriteLine("Tuesday"); break;
       case 3: Console.WriteLine("Wednesday"); break;
       default: Console.WriteLine("Unknown day"); break;
   }
   ```

---

## 18. For Loops
   - Looping a specified number of times.
   ```csharp
   for (int i = 0; i < 5; i++)
       Console.WriteLine(i);
   ```

---

## 19. While Loops
   - Loop while a condition is true.
   ```csharp
   int count = 0;
   while (count < 5)
   {
       Console.WriteLine(count);
       count++;
   }
   ```

---

## 20. Conditional Operator
   - Using `?:` for inline conditionals.
   ```csharp
   int age = 18;
   string result = (age >= 18) ? "Adult" : "Minor";
   ```

---

## 21. Numeric Formatting
   - Format numbers as currency or percentage.
   ```csharp
   double price = 1234.5678;
   Console.WriteLine(price.ToString("C")); // Currency
   ```

---

## 22. `TryParse` Function
   - Parse strings with error handling.
   ```csharp
   string input = "123";
   if (int.TryParse(input, out int result))
       Console.WriteLine("Valid integer");
   ```

---

## 23. Exercise - Times Table
   - Display a multiplication table.
   ```csharp
   int number = 5;
   for (int i = 1; i <= 10; i++)
       Console.WriteLine($"{number} x {i} = {number * i}");
   ```

---

## 24. Exercise - Fizz Buzz Game
   - A classic programming exercise.
   ```csharp
   for (int i = 1; i <= 100; i++)
   {
       if (i % 3 == 0 && i % 5 == 0) Console.WriteLine("FizzBuzz");
       else if (i % 3 == 0) Console.WriteLine("Fizz");
       else if (i % 5 == 0) Console.WriteLine("Buzz");
       else Console.WriteLine(i);
   }
   ```

---

## 25. Verbatim String Literal
   - Using `@` for multi-line and file path strings.
   ```csharp
   string path = @"C:\Users\Public\Documents";
   ```

---

## 26. String Formatting
   - Format strings with placeholders.
   ```csharp
   string name = "John";
   int age = 30;
   Console.WriteLine(string.Format("Name: {0}, Age: {1}", name, age));
   ```

---

## 27. String Interpolation
   - Embed variables directly in strings.
   ```csharp
   string name = "Alice";
   int age = 25;
   Console.WriteLine($"Name: {name}, Age: {age}");
   ```

---

## 28. String Concatenation
   - Concatenate strings using `+`.
   ```csharp
   string firstName = "John";
   string lastName = "Doe";
   string fullName = firstName + " " + lastName;
   ```

---

## 29. Empty String
   - Declare empty strings.
   ```csharp
   string emptyString = "";
   ```

---

## 30. String `Equals` Function
   - Compare strings for equality.
   ```csharp
   string str1 = "hello";
   string str2 = "Hello";
   bool isEqual = str1.Equals(str2, StringComparison.OrdinalIgnoreCase);
   ```

---

## 31. String Iteration Looping
   - Iterate over each character in a string.
   ```csharp
   string word = "Hello";
   foreach (char letter in word)
       Console.WriteLine(letter);
   ```

---

## 32. String `IsNullOrEmpty` Function
   - Check if a string is null or empty.
   ```csharp
   string str = null;
   if (string.IsNullOrEmpty(str))
       Console.WriteLine("String is null or empty");
   ```

---

## 33. Exercise - Print String in Reverse
   - Print each character in reverse order.
   ```csharp
   string input = "hello";
   for (int i = input.Length - 1; i >= 0; i--)
       Console.Write(input[i]);
   ```

---

## 34. Exercise - Password Checker
   - Check if a password is at least 8 characters.
   ```csharp
   string password = "secret";
   if (password.Length >= 8)
       Console.WriteLine("Valid password");
   ```

---

## 35. Arrays
   - Declare and use arrays.
   ```csharp
   int[] numbers = { 1, 2, 3, 4, 5 };
   ```

---

## 36. Array Sorting
   - Sort arrays.
   ```csharp
   int[] numbers = { 5, 2, 9, 1 };
   Array.Sort(numbers);
   ```

---

## 37. Array Reversal
   - Reverse the elements of an array.
   ```csharp
   Array.Reverse(numbers);
   ```

---

## 38.

 Array Clearing
   - Set all elements to default values.
   ```csharp
   Array.Clear(numbers, 0, numbers.Length);
   ```

---

## 39. Array `IndexOf`
   - Find the index of a specific element.
   ```csharp
   int index = Array.IndexOf(numbers, 3);
   ```

---

## 40. Lists
   - Dynamic collections.
   ```csharp
   List<string> names = new List<string> { "Alice", "Bob" };
   ```

---

## 41. Dictionary
   - Key-value pairs.
   ```csharp
   Dictionary<string, int> ages = new Dictionary<string, int>
   {
       { "Alice", 30 },
       { "Bob", 25 }
   };
   ```

---

## 42. Exercise - Odd/Even Number Split
   - Separate odd and even numbers in a list.

---

## 43. Exercise - Array of Multiples
   - Generate an array with multiples of a number.

---

## 44. Functions
   - Define functions with return values.
   ```csharp
   static int Add(int a, int b) => a + b;
   ```

---

## 45. Void Functions
   - Functions that don't return a value.
   ```csharp
   static void PrintHello() => Console.WriteLine("Hello");
   ```

---

## 46. Return Type Functions
   - Functions with a specified return type.
   ```csharp
   static int Square(int x) => x * x;
   ```

---

## 47. Function Parameters
   - Passing arguments to functions.
   ```csharp
   static int Add(int a, int b) => a + b;
   ```

---

## 48. Optional Parameters
   - Use default values for parameters.
   ```csharp
   static void Greet(string name = "Guest") => Console.WriteLine($"Hello, {name}");
   ```

---

## 49. Named Parameters
   - Explicitly name parameters in function calls.
   ```csharp
   Greet(name: "Alice");
   ```

---

## 50. Out Parameters
   - Passing parameters with `out`.
   ```csharp
   static bool TryParse(string s, out int number) => int.TryParse(s, out number);
   ```

---

## 51. Reference Parameters
   - Using `ref` to pass parameters by reference.
   ```csharp
   static void Increment(ref int x) => x++;
   ```

---

## 52. Exercise - Area of a Triangle
   - Calculate the area of a triangle.
   ```csharp
   static double Area(double b, double h) => 0.5 * b * h;
   ```

---

## 53. Exercise - Sum of int Array
   - Sum elements in an array.

---

## 54. Exception Handling
   - Handling errors with try-catch.
   ```csharp
   try { int.Parse("abc"); }
   catch (FormatException) { Console.WriteLine("Invalid format"); }
   ```

---

## 55. Try…catch
   - Basic try-catch for handling exceptions.

---

## 56. Printing Error Messages
   - Print exception messages.
   ```csharp
   try { int.Parse("abc"); }
   catch (Exception ex) { Console.WriteLine(ex.Message); }
   ```

---

## 57. Exercise - Custom TryParse
   - Create a custom TryParse function.

---

## 58. Debugging
   - Using breakpoints and stepping through code.

---

## 59. Local/Auto Window
   - Viewing local variables in debug mode.

---

## 60. Watch Window
   - Tracking specific variables during debugging.

---

## 61. Exercise - Fix Logic Error
   - Debugging exercises to fix common errors.

---

## 62. Structures
   - Define a struct with fields.
   ```csharp
   struct Point { public int X; public int Y; }
   ```

---

## 63. Classes
   - Define a class with properties and methods.
   ```csharp
   class Person { public string Name; }
   ```

---

## 64. Class Functions
   - Methods defined in a class.

---

## 65. Class Fields
   - Define class-level variables.

---

## 66. Class Variable/Function Scope
   - Define public and private members.

---

## 67. Class Properties
   - Encapsulate fields with properties.
   ```csharp
   class Person { public string Name { get; set; } }
   ```

---

## 68. Class ToString Function Override
   - Override `ToString()` for custom output.
   ```csharp
   class Person { public override string ToString() => "Person"; }
   ```

---
