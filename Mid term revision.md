# Java compiling process

To compile the java program, we can use the command: **javac SourceFileName.** **java**. The javac command reads class and interface definitions and compiles them into a . class file or byte code which can be run on the Java Virtual Machine.

# Compile errors

```java
public class Main {
    public static void main(String[] args) {
        int i = 0  // missing semi-colon is a compile error
        while (i < 5) {
            System.out.println(i);
            //i++;
        }
    }
}
```

# Logical errors

```java
public class Main {
    public static void main(String[] args) {
        int i = 0;
        while (i < 5) { # This is an infinite loop - always true
            System.out.println(i);
        }
    }
}
```

# Rules to declare variables

1. A variable name can consist of Capital letters **A-Z**, lowercase letters **a-z** digits **0-9**, and two special characters such as **_** underscore and **$** dollar sign.
2. The first character must not be a digit.
3. Blank spaces cannot be used in variable names.
4. Java keywords cannot be used as variable names.
5. Variable names are case-sensitive.
6. There is no limit on the length of a variable name but by convention, it should be between 4 to 15 chars.
7. Variable names should always exist on the left-hand side of assignment operators.

# Scanner methods to take user input from the keyboard

| Method          | Description                           |
| :-------------- | :------------------------------------ |
| `nextBoolean()` | Reads a `boolean` value from the user |
| `nextByte()`    | Reads a `byte` value from the user    |
| `nextDouble()`  | Reads a `double` value from the user  |
| `nextFloat()`   | Reads a `float` value from the user   |
| `nextInt()`     | Reads a `int` value from the user     |
| `nextLine()`    | Reads a `String` value from the user  |
| `nextLong()`    | Reads a `long` value from the user    |
| `nextShort()`   | Reads a `short` value from the user   |

```java
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner myObj = new Scanner(System.in);
        System.out.print("Enter a char or a string: ");
        String i = myObj.nextLine();
        System.out.println(i);
        }
    }
```

# Assignment operators

```java
a = 10;
num1 += num2; //num1 = num1 + num2
```

# Math.pow()

```java
double i = Math.pow(2,2) //2 to the power of 2
```

# Casting

```java
public class Main {
    public static void main(String[] args) {
        double i = 12.5;

        System.out.println((int) i);
    }

}
```

# Concatenate

```java
public class Main {
    public static void main(String[] args) {
        double i = 12.6;

        System.out.println("The answer is " + (int) i + " which is an integer part of the " + i);
    }

}
```

# Retrieving array members

```java
public class Main {
    public static void main(String[] args) {
        String phrase = "Can't wait until spring break";
        char c = phrase.charAt(6);
        System.out.println(c);
    }

}
// The answer is w
```

# Named constant

```java
public class Main {
    public static void main(String[] args) {
        final double pi = 3.14;
      
    
        

    }

}
```

# Data types

- Primitive data types - includes `byte`, `short`, `int`, `long`, `float`, `double`, `boolean` and `char`
- Non-primitive data types - such as `String`, Arrays and Classes

| Data Type | Size    | Description                                                  |
| :-------- | :------ | :----------------------------------------------------------- |
| `byte`    | 1 byte  | Stores whole numbers from -128 to 127                        |
| `short`   | 2 bytes | Stores whole numbers from -32,768 to 32,767                  |
| `int`     | 4 bytes | Stores whole numbers from -2,147,483,648 to 2,147,483,647    |
| `long`    | 8 bytes | Stores whole numbers from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 |
| `float`   | 4 bytes | Stores fractional numbers. Sufficient for storing 6 to 7 decimal digits |
| `double`  | 8 bytes | Stores fractional numbers. Sufficient for storing 15 decimal digits |
| `boolean` | 1 bit   | Stores true or false values                                  |
| `char`    | 2 bytes | Stores a single character/letter or ASCII values             |

**If 7 and 30 are int values. What is the result of 30 / 7? What is the result of 30 % 7?**

```java
public class Main {
    public static void main(String[] args) {
        int a = 7;
        int b = 30;
        System.out.println(b / a); // integer output, ignore floating point; 4
        System.out.println(b % a); // remainder; 2
    }
}
```

**Output of the following Java statements**

```java
public class Main {
    public static void main(String[] args) {
        String str = "I LOVE Java Coding!";
        String str2 = "    I LOVE Java    ";
        System.out.println(str.equals("I love Java Coding!"));
        System.out.println(str.equalsIgnoreCase("I love Java Coding!"));
        System.out.println(str.toLowerCase());
        System.out.println(str.toUpperCase());
        System.out.println(str.substring(5,8));
        System.out.println(str.substring(2));
        System.out.println(str.indexOf("a"));
        System.out.println(str.indexOf("z"));
        System.out.println(str2.trim());
        System.out.println(str);
        System.out.println(str2);

    }
}
```

```
false
true
i love java coding!
I LOVE JAVA CODING!
E J
LOVE Java Coding!
8
-1
I LOVE Java
I LOVE Java Coding!
    I LOVE Java    
```

**Length of a string**

```java
String str = "I LOVE Java Coding!";
int len = str.length();
System.out.println(len);
```

# printf

```java
public class Main {
    public static void main(String[] args) {
        System.out.printf ("The number is: %5.2f \n", 12.1235);
        System.out.printf ("The number is: %5f \n", 12.1235);
        System.out.printf ("The number is: %10.3f", 12.1235);

    }
}
```

```
The number is: 12.12 
The number is: 12.123500 
The number is:     12.124
```

# Special characters

- **\t** – tab
- **\b** – backspace (a step backward in the text or deletion of a single character)
- **\n** – new line
- **\r** – carriage return
- **\f** – form feed
- **\’** – single quote
- **\"** – double quote
- **\\** – backslash

``` java
public class Main {
    public static void main(String[] args) {
        System.out.println("Spring\nBreak\nReady");
    }
}
```

**Under what condition does an if, else-if, while, do-while, and for loop execute? **

**What is used to create a compound statement (or block)? **

# Switch

```java
switch(expression) {
  case x:
    // code block
    break;
  case y:
    // code block
    break;
  default:
    // code block
}
```

# OR, AND and NOT truth tables

# Random class

```java
import java.util.Random;

public class Main {
    public static void main(String[] args) {
        Random random = new Random();
        System.out.println(random.nextInt());

    }
}

```

- **`nextInt()`**: Returns a random `int` value within the range: $ -2,147,483,648<=value<= 2,147,483, 647$
- **`nextInt(int range)`**: Returns a random `int` value within the range: $ 0 <= value < range $
- **`nextDouble()`**: Returns a random `double` value within the range: $ 0.0 <= value < 1.0 $
- **`nextFloat()`**: Returns a random `float` value within the range: $ 0.0 <= value < 1.0 $
- **`nextLong()`**: Returns a random `long` value.

# Common loop errors

- Infinite loop
- Equality vs assignment operator

**If you know how many times a loop is going to run should you use a for loop, while loop, or do while loop? **

# Void and return methods

Void functions are created and used just like value-returning functions except they do not return a value after the function executes.

Declare a method's return type in its method declaration. Within the body of the method, you use the return statement to return the value.

```java
// a method for computing the area of the rectangle
    public int getArea() {
        return width * height;
    }
```

# Debugging techniques

The IntelliJ IDE includes Java debugging features such as advanced breakpoints, integration with testing frameworks, remote debugging, and integration with testing frameworks. 

# Getters and setters

Getter: A method that allows you to access an attribute in a given class. Setter: A method that allows you to set or mutate the value of an attribute in a class

```java
public class Person {
  private String name; // private = restricted access

  // Getter
  public String getName() {
    return name;
  }

  // Setter
  public void setName(String newName) {
    this.name = newName;
  }
}
```

```java
public class Main {
  public static void main(String[] args) {
    Person myObj = new Person();
    myObj.setName("John"); // Set the value of the name variable to "John"
    System.out.println(myObj.getName());
  }
}

// Outputs "John"
```

# Encapsulation

Encapsulation is a fundamental concept in object-oriented programming (OOP) that refers to the bundling of data and methods that operate on that data within a single unit, which is called a class in Java. Encapsulation is a way of hiding the implementation details of a class from outside access and only exposing a public interface that can be used to interact with the class.

In Java, encapsulation is achieved by declaring the instance variables of a class as private, which means they can only be accessed within the class. To allow outside access to the instance variables, public methods called getters and setters are defined, which are used to retrieve and modify the values of the instance variables, respectively. 

```java
class Person { 
	private String name; 
	private int age; 

	public String getName() { return name; } 

	public void setName(String name) { this.name = name; } 

	public int getAge() { return age; } 

	public void setAge(int age) { this.age = age; } 
} 

public class Main { 
	public static void main(String[] args) 
	{ 
		Person person = new Person(); 
		person.setName("John"); 
		person.setAge(30); 

		System.out.println("Name: " + person.getName()); 
		System.out.println("Age: " + person.getAge()); 
	} 
}

```

# Comments

- Single line //
- Multi line /* */
- Documentation comment
  - Documentation comments are very similar to regular multi-line comments except that the starting characters include an extra asterisk: **/\****  */

**What is the shortcut equivalent of total = total + next**

```java
total += next
```

**What is a local variable? **

A local variable in Java is **a variable that's declared within the body of a method**. Then you can use the variable only within that method. Other methods in the class aren't even aware that the variable exists.

# Objects and classes

# String to double

```java

import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        int a = 0;
        double b = 0.0;
        Scanner myObj = new Scanner(System.in);
        System.out.print("Enter a number: ");
        String i = myObj.nextLine();
        a = Integer.parseInt(i)+Integer.parseInt(i);
        b = Double.parseDouble(i)+5.0;
        System.out.println(a);
        System.out.println(b);
    }
}
```

# While and for loop

```java

import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        int j = 0;
        while(j<5) {
            System.out.println("While loop counter is: " + j);
            j++;
        }

            for (int i = 0; i < 5; i++) {
                System.out.println("For loop counter is: " + i);
            }

        }

    }

```

# Nested if then else

```java
public class Test {

    public static void main(String args[]) {
        int x = 30;
        int y = 10;

        if( x == 30 ) {
            if( y == 10 ) {
                System.out.print("X = 30 and Y = 10");
            }
        }
    }
}
```

```java
public class Test {

    public static void main(String args[]) {
        int x = 30;
        int y = 10;

        if( x < 30 ) {
            System.out.print("X < 30");
        } else {
            if( y > 9 ) {
                System.out.print("X > 30 and Y > 9");
            }
        }
    }
}
```

# Instance methods

Instance methods are methods that require an object of its class to be created before it can be called. To invoke an instance method, we have to create an Object of the class in which the method is defined. 

```java
// Example to illustrate accessing the instance method .
import java.io.*;

class Foo {

    String name = "";

    // Instance method to be called within the
    // same class or from another class defined
    // in the same package or in different package.
    public void geek(String name) {
        this.name = name;
    }
}

class GFG {
    public static void main(String[] args)
    {

        // create an instance of the class.
        Foo ob = new Foo();

        // calling an instance method in the class 'Foo'.
        ob.geek("Hello World");
        System.out.println(ob.name);
    }
}
```

# Static methods

Static methods are the methods in Java that can be called without creating an object of class. They are referenced by the **class name itself** or reference to the Object of that class. 

```java
// Example to illustrate Accessing
// the Static method(s) of the class.
import java.io.*;

class Geek {

    public static String geekName = "";

    public static void geek(String name)
    {
        geekName = name;
    }
}

class GFG {
    public static void main(String[] args)
    {

        // Accessing the static method geek()
        // and field by class name itself.
        Geek.geek("Hello World");
        System.out.println(Geek.geekName);


    }
}

```

# Stub class

A stub is a class or object that we use in unit tests to return fake data similar to the function’s data when it is in production. An example of this can be a call to an API that gives some data as a response, but when we use a test stub, we hard-code the data to test it.



