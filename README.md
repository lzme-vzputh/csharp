# vzputh
[IG](https://www.instagram.com/vzputh/)
[FB](https://www.facebook.com/vzputh/)
---

# C# Programming Guide

## 1. Introduction
   - **Overview**: This section introduces the course, which covers fundamental C# programming concepts. Topics include data types, loops, functions, and object-oriented programming principles.
   - **Example**:  
     - **Usefulness**: C# is used across various domains, from web development to desktop applications, mobile apps, and game development, particularly with the Unity engine.
     - **Syntax Overview**: C# has a clean and readable syntax that supports object-oriented programming, making it easier to build modular, maintainable applications.
     - **Why Learn C#**: C# is a high-performance, versatile language maintained by Microsoft, and it is widely used in industry for enterprise-level applications and services.

---

## 2. Installing Visual Studio 2022
   - **Overview**: This section guides you through downloading and setting up Visual Studio 2022, a powerful Integrated Development Environment (IDE) for writing, testing, and debugging C# programs.
   - **Example**:  
     - **Step 1**: Go to the [official Visual Studio website](https://visualstudio.microsoft.com/) to access the latest version.
     - **Step 2**: Download the installer for **Visual Studio 2022 Community Edition**, which is free and includes all essential features.
     - **Step 3**: Run the installer, and when prompted to select workloads, choose **".NET desktop development"**. This will install everything needed to start building C# applications.

---

## 3. Creating Your First Project
   - **Overview**: This section walks you through creating your first C# Console Application, which is a straightforward way to begin learning the language and testing code.
   - **Example**:  
     - **Step 1**: Open Visual Studio, go to **"Create a new project"**, and choose **"Console App (.NET Core or .NET Framework)"** from the list of available templates. Console applications are ideal for practicing fundamental programming concepts without the complexity of graphical interfaces.
     - **Step 2**: Name the project **"HelloWorldApp"** (or any name you prefer) and click **"Create"**. Visual Studio will set up your project with a basic program structure ready for coding.

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
   - ការចែកយកសំណល់
   ```csharp
   int num1 = 20,
       num2 = 3;
   int re = num1 % num2;
   // 20 % 4 = 0
   // note if 100 % 90 = 10 
   // 1000 % 90 = 10
   Console.WriteLine(re);
   ```

---

## 11. `var` Keyword
   - Implicit typing with `var`.
   - we can use `var` keyword inferred as dataType `string` `int` `float`...
   ```csharp
 
   var name = "vzputh"; // inferred as string
   Console.WriteLine(name);
   var sex = 'm';  // inferred as char
   Console.WriteLine(sex);
   var db = 5000D;
   Console.WriteLine(db);
   var lg = 4322344L;
   Console.WriteLine(lg);
   ```

---

## 12. `const` Keyword
   - Declaring constants.
   - we use `const` for lock value.
   ```csharp
   const double PI = 3.14159;
   ```

---


## 13. Console Input/Output
   - Use `Console.ReadLine()` for `Input` and `Console.WriteLine()` for `Output`
   - `Console.ReadLine()` work only `string` and `char`
   - If for other numeric types we need Convert strings to integers or other numeric types or `Convert.To'...'(Console.ReadLine())`
#### 1.Convert `ageInput`
   ```csharp
   Console.Write("Enter your name:");
   string name = Console.ReadLine();

   Console.Write("Enter your age:");
   string ageInput = Console.ReadLine();
   int age = Convert.ToInt32(ageInput);

   Console.WriteLine($"My name's {name},I'm {age} year old.");
   ```
#### 2.Fast
   ```csharp 
   Console.Write("Enter your name:");
   string name = Console.ReadLine();

   Console.Write("Enter your age:");
   int age = Convert.ToInt32(Console.ReadLine());

   Console.WriteLine($"My name's {name},I'm {age} year old.");
   ```
#### 
   ```csharp
   string ageInput = Console.ReadLine();
   int age = Convert.ToInt32(ageInput);
   // Is the same.
   int age = Convert.ToInt32(Console.ReadLine());
   ```


---

## 14. If Statements
   - Conditional logic with `if`.
   ```csharp
   if (age > 18)
       Console.WriteLine("Adult");
   ```

---

## 15. Switch Statements
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

## 16. For Loops
   - Looping a specified number of times.
   ```csharp
   for (int i = 0; i < 5; i++)
       Console.WriteLine(i);
   ```

---

## 17. While Loops
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

## 28. Conditional Operator
   - Using `condition ? "true" : "false"`   for inline conditionals.
   ```csharp
   int age = 18;
   string result = (age >= 18) ? "Adult" : "Minor";
   ```

---

## 19. Numeric Formatting
   - Format numbers as currency or percentage.
   ```csharp
   // string.format only numeric

double price = 10D / 3D;
Console.WriteLine(string.Format("{3} {0}  {1}   {0}   {2}​",price,99,12,25));// by array

Console.WriteLine(string.Format("...{0:0}", price));
Console.WriteLine(string.Format("...{0:0.0}",price));
Console.WriteLine(string.Format("{0:0.00}", price));
Console.WriteLine(string.Format("{0:0.000}",price));
Console.WriteLine(string.Format("{0:0.#}", price));
   ```
```csharp
//Console.WriteLine(money.ToString("C")); can use only "C" keyword c= currency

double price = 10D / 3D;
Console.WriteLine(string.Format("$10 / $3 = ${0:0.00}", money));
Console.WriteLine(money.ToString("C")); //$3.33
Console.WriteLine(money.ToString("C1"));//$3.3
Console.WriteLine(money.ToString("C2"));//$3.33
Console.WriteLine(money.ToString("C3"));//$3.333
Console.WriteLine(money.ToString("C4"));//$3.3333
```
```csharp
   Console.WriteLine(money.ToString("C", CultureInfo.CreateSpecificCulture("en-GB"))); £
   Console.WriteLine(money.ToString("C", CultureInfo.CreateSpecificCulture("en-US")));  $
   Console.WriteLine(money.ToString("C", CultureInfo.CreateSpecificCulture("en-TH")));   THB
   Console.WriteLine(money.ToString("C", CultureInfo.CreateSpecificCulture("en-KH")));   KHR
   Console.WriteLine(money.ToString("C", CultureInfo.CreateSpecificCulture("en-KR")));   ₩
   Console.WriteLine(money.ToString("C", CultureInfo.CreateSpecificCulture("en-JP")));   ¥
```

---

## 20. `TryParse` Function
   - Parse strings with error handling.
   ```csharp
   string input = "123";
   if (int.TryParse(input, out int result))
       Console.WriteLine("Valid integer");
   ```

---

## 21. Verbatim String Literal
   - Using `@` for multi-line and file path strings.
   ```csharp
   string path = @"C:\Users\Public\Documents";
   ```

---

## 22. String Formatting
   - Format strings with placeholders.
   ```csharp
   string name = "John";
   int age = 30;
   Console.WriteLine(string.Format("Name: {0}, Age: {1}", name, age));
   ```

---

## 23. String Interpolation
   - Embed variables directly in strings.
   ```csharp
   string name = "Alice";
   int age = 25;
   Console.WriteLine($"Name: {name}, Age: {age}");
   ```

---

## 24. String Concatenation
   - Concatenate strings using `+`.
   ```csharp
   string firstName = "John";
   string lastName = "Doe";
   string fullName = firstName + " " + lastName;
   ```

---

## 25. Empty String
   - Declare empty strings.
   ```csharp
   string emptyString = "";
   ```

---

## 26. String `Equals` Function
   - Compare strings for equality.
   ```csharp
   string str1 = "hello";
   string str2 = "Hello";
   bool isEqual = str1.Equals(str2, StringComparison.OrdinalIgnoreCase);
   ```

---

## 27. String Iteration Looping
   - Iterate over each character in a string.
   ```csharp
   string word = "Hello";
   foreach (char letter in word)
       Console.WriteLine(letter);
   ```

---

## 28. String `IsNullOrEmpty` Function
   - Check if a string is null or empty.
   ```csharp
   string str = null;
   if (string.IsNullOrEmpty(str))
       Console.WriteLine("String is null or empty");
   ```

---

## 29. Arrays
   - Declare and use arrays.
   ```csharp
   int[] numbers = { 1, 2, 3, 4, 5 };
   ```

---

## 30. Array Sorting
   - Sort arrays.
   ```csharp
   int[] numbers = { 5, 2, 9, 1 };
   Array.Sort(numbers);
   ```

---

## 31. Array Reversal
   - Reverse the elements of an array.
   ```csharp
   Array.Reverse(numbers);
   ```

---

## 32.Array Clearing
   - Set all elements to default values.
   ```csharp
   Array.Clear(numbers, 0, numbers.Length);
   ```

---

## 33. Array `IndexOf`
   - Find the index of a specific element.
   ```csharp
   int index = Array.IndexOf(numbers, 3);
   ```

---

## 34. Lists
   - Dynamic collections.
   ```csharp
   List<string> names = new List<string> { "Alice", "Bob" };
   ```

---

## 35. Dictionary
   - Key-value pairs.
   ```csharp
   Dictionary<string, int> ages = new Dictionary<string, int>
   {
       { "Alice", 30 },
       { "Bob", 25 }
   };
   ```

---

## 36. Functions
   - Define functions with return values.
   ```csharp
   static int Add(int a, int b) => a + b;
   ```

---

## 37. Void Functions
   - Functions that don't return a value.
   ```csharp
   static void PrintHello() => Console.WriteLine("Hello");
   ```

---

## 38. Return Type Functions
   - Functions with a specified return type.
   ```csharp
   static int Square(int x) => x * x;
   ```

---

## 39. Function Parameters
   - Passing arguments to functions.
   ```csharp
   static int Add(int a, int b) => a + b;
   ```

---

## 40. Optional Parameters
   - Use default values for parameters.
   ```csharp
   static void Greet(string name = "Guest") => Console.WriteLine($"Hello, {name}");
   ```

---

## 41. Named Parameters
   - Explicitly name parameters in function calls.
   ```csharp
   Greet(name: "Alice");
   ```

---

## 42. Out Parameters
   - Passing parameters with `out`.
   ```csharp
   static bool TryParse(string s, out int number) => int.TryParse(s, out number);
   ```

---

## 43. Reference Parameters
   - Using `ref` to pass parameters by reference.
   ```csharp
   static void Increment(ref int x) => x++;
   ```

---

## 44. Exception Handling
   - Handling errors with try-catch.
   ```csharp
   try { int.Parse("abc"); }
   catch (FormatException) { Console.WriteLine("Invalid format"); }
   ```

---

## 45. Try…catch
   - Basic try-catch for handling exceptions.

---

## 46. Printing Error Messages
   - Print exception messages.
   ```csharp
   try { int.Parse("abc"); }
   catch (Exception ex) { Console.WriteLine(ex.Message); }
   ```

---
## 47. Debugging
   - Using breakpoints and stepping through code.

---

## 48. Local/Auto Window
   - Viewing local variables in debug mode.

---

## 49. Watch Window
   - Tracking specific variables during debugging.

---

## 50. Structures
   - Define a struct with fields.
   ```csharp
   struct Point { public int X; public int Y; }
   ```

---

## 51. Classes
   - Define a class with properties and methods.
   ```csharp
   class Person { public string Name; }
   ```

---

## 52. Class Functions
   - Methods defined in a class.

---

## 53. Class Fields
   - Define class-level variables.

---

## 54. Class Variable/Function Scope
   - Define public and private members.

---

## 55. Class Properties
   - Encapsulate fields with properties.
   ```csharp
   class Person { public string Name { get; set; } }
   ```

---

## 56. Class ToString Function Override
   - Override `ToString()` for custom output.
   ```csharp
   class Person { public override string ToString() => "Person"; }
   ```

---
