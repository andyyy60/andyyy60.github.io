# Basics of Java

### Table of Contents
1. Data Types
- What is a primitive data type?
2. Variables

a. Declaring variables

3. Operators

a. Arithmetic operators

b. Relational operators

4. Strings

a. Creating strings

b. Using string operators


---

## Primitive Data Types

##### What is a primitive data type?

tha *primitive* data type is composed of no other data types and cannot be broken down any further. It does not contain any dot operators or helper classes and nothing can be derived from it.
For example, an `int` cannot be broken down any further, while `Integer` is an *object* and can be broken down to its components.

`boolean`
Use this data type for simple flags that track true/false conditions
* Description: Has only two possible values ``true`` or ``false``
* Default value: `false`
* Example literals: `true`, `false`



`byte`
Use this data type for saving memory in large arrays (where memory actually matters). They can also be used in place of int where their limits help to clarify your code, read more about ``byte`` [here](https://docs.oracle.com/javase/7/docs/api/java/lang/Byte.html).
* Description:  Has a minimum value of -128 and a maximum value of 127 (inclusive), 8-bit signed two's complement integer.
* Default:  `0`
* Example literals: **(none)**

`char`
Use this data type when dealing with single Unicode characters.

* Description: The char data type is a single 16-bit Unicode character.
* Default:  `\u0000`
* Example literals: `'a'`, `'\u0041'`, `'\\'`

`short`
Just like ``byte``, use this data type for saving memory in large arrays (where memory actually matters). Read more about ``short``  [here](https://docs.oracle.com/javase/7/docs/api/java/lang/Short.html).
* Description: Has a minimum value of -32,768 and a maximum value of 32,767 (inclusive). 16-bit signed two's complement integer. 
* Default:  `0`
* Example literals: **(none)**

`int`
Use this data type to store numbers up to (2^31)-1. The object counterpart ``Integer`` allows methods such as ``compareUnsigned``.

* Description: 32-bit signed two's complement integer, has a minimum value of -2^31 and a maximum value of (2^31)-1.
* Default:  `0`
* Example literals: `-2`, `-1`, `0`, `1`, `2`

`long`
Use this data type to store big integers > (2^31)-1 that would not fit in an ``int`` variable otherwise
* Description: This data type is a long version of ``int``, it allows for bigger values to be stored in a variable,  the signed long has a minimum value of -263 and a maximum value of 263-1 (64-bit signed two's complement integer).
* Default:  `0`
* Example literals: `-2L`, `-1L`, `0L`, `1L`, `2L`

`float`
As with short and byte, use a float if you need to save memory in large arrays of floating point numbers, if precision is necessary, use ``double``

* Description: This data type allows for decimal numbers to be stored with single-precision of 32-bits.
* Default:  `0.0`
* Example literals: `1.23e100f`, `-1.23e-100f`, `.3f`, `3.14F`

`double`
Use this data type when dealing with decimal numbers (ex. ``0.0``)

* Description: Another decimal number primitive type. Usually the default type for decimal points, stores with twice as much precision as float with 64-bit IEEE 754 floating point.
* Default:  `0.0`
* Example literals: `1.23456e300d`, `-1.23456e-300d`, `1e1d`

---

## Variables

##### Declaring variables

To declare a variable in java, you have to specify it’s type. If I want a variable to hold the number 3, I have to tell java I want it to store an integer and then I tell it the integer to store, like so:

	int myVariable = 3;

If I want to reassign the value of a variable, can just do this:

	int myVariable2;
	myVariable2 = 4;

I can only do this type of declaration because myVariable2 was initialized as type int. Initially it has no value attached to it, but then the next line assigns it the value 4. The same process can be done with any primitive type or string, but an object from a class is a special case.

To declare a variable, pick a name that describes the content of it and write it in the following syntax: [*type*] [*variable name*]
Examples:

    int myNumber;
    myNumber = 5;

Or combine them into one line:

    int myNumber = 5;

To define a decimal number:

    double d = 4.5;

To define a decimal number of type ``float``

    float f = (float) 4.5; //changes f from default double to float
    
or

    float f = 4.5f; // shorter way to change double to float

## Operators

Next, we cover arithmetic & relational operators.

### Arithmetic

`+` addition

    int additionExample = 9 + 10;

`-` subtraction

    int substractionExample = 9 - 10;


`*` multiplication

    int multiplicationExample = 2 * 4;

`/` division

    int divisionExample = 8/2;

`%` modulus

    int modulusExample = 8%2;

`++` increment
    
    int incrementExample = 1;
    incrementExample++; // incrementExample contains 2 now

`--` decrement

    int decrementExample = 1;
    decrementExample--; // decrementExample contains 0 now

### Relational

`==` equal to

    int left = 1;
    int right = 1;
    System.out.println( left == right ); //prints out "true" 

`!=` not equal to

    int left = 1;
    int right = 0;
    System.out.println( left != right ); //prints out "true" 

`>` greater than

    int left = 5;
    int right = 12;
    System.out.println( left > right ); //prints out "false" 

`<` less than

    int left = 5;
    int right = 12;
    System.out.println( left < right ); //prints out "true" 

`>=` greater than or equal to

    int left = 5;
    int middle = 5
    int right = 12;
    System.out.println( left >= right ); //prints out "false" 
    System.out.println( left >= middle ); //prints out "true" 


`<=` less than or equal to

    int left = 5;
    int middle = 5
    int right = 12;
    System.out.println( left <= right ); //prints out "true" 
    System.out.println( left >= middle ); //prints out "true" 

---

## Strings

Strings are a sequence of characters. In Java, they are objects (meaning they can be broken down and you can use operators in them)

#### Creating Strings
To create a string, declare a variable of type ``String``

    String greeting = "Hello world!";

#### Using string operators

Because String is a class, it contains built-in functions that can be used with any varible of type ``String``.

##### Length of a String

    String sentence = "Please excuse my dear aunt sally";
    int length = sentence.length(); //contains the number of characters in variable sentence

##### Combining two strings together

This is also know as 'concatenating' two strings.

    String str1 = "my favorite food is";
    String str2 = "pizza";
    String sentence = string1.concat(string2); // "my favorite food is pizza"
    


## Hello World

Open terminal and `cd` to the directory of choosing. Then create the **source code** file:

	$ touch FirstJavaClass.java

Open `FirstJavaClass.java` (your source code) with preferred text editor or IDE and input this code:

	public class FirstJavaClass {

		public static void main(String args []) {
			System.out.println("Hello World");
		}

	}

Compile the source code. Enter into the terminal:

	$ javac FirstJavaClass.java

The output of compiling the source code is the **build**.

Run the build. Enter into the terminal:

	$ java FirstJavaClass

A first java program. Pretty exciting!

---

## If Then

Make a `JavaIfThen.java` file and input the following code:

	public class JavaIfThen {
	    public static void main (String args []) {
	        int x = 5;
	        int z = 10;

	        if (x + z == 15) {
	            System.out.println("x + z = 15");
	        }
	    }
	}

Compile the source code and run the build.

Your terminal will print `x + z = 15` because the statement `x + z == 15` is `True`.

---

## While Loop

Make a `JavaWhileLoop.java` file and input the code:

	public class JavaWhileLoop {
	    public static void main(String args []) {
	        int x = 0;
	        while (x < 8) {
	            System.out.println("The value of x is: " + x);
	            x++;
	        }
	    }
	}

Compile the source code and run the build.

This will print to the terminal eight iterations of the value of the variable `x` of type `int`, with values from `0` to `7` iterating by `1`.

---

## For Loop

Make a `JavaForLoop.java` file and input the code:

	public class JavaForLoop {
	    public static void main(String args[]) {
	        int x = 32;
	        for (int i = 0; i < x; i++) {
	            System.out.println("i = " + i);
	        }
	    }
	}

Compile the source code and run the build.

This will print to the terminal thirty-two iterations of the value of the variable `i` of type `int`, with values from `0` to `31` iterating the variable `i` of type `int` by the amount of `1`.

---

## CheckerBoard Program

Make a `CheckerBoard.java` file. Enter into it the following code:

	public class CheckerBoard {
	    public static void main( String args[] ) {
	        String x = "* * * * * * * *";
	        String y = " * * * * * * * *";
	        for ( int i = 0; i < 8; i++ ) {
	            if ( i % 2 == 0 ) {
	                System.out.println(x);
	            } else {
	                System.out.println(y);
	            }
	        }
	    }
	}

Compile the source code and run the build.

Love the checkerboard pattern.

---

# **Object-Oriented Design**

Java is an object-oriented programming language.

## Objects

An object is a bundle of software that has **states** & **behaviors**.

Analogously, a lamp object may have two states, `on` and `off`; as well as two behaviors, `turn on` and `turn off`. More complex objects may have more complex sets of states and behaviors.

Bundling software into objects provides the following benefits:

* **Modularity**: object source code can be updated independently from other code.

* **Information-hiding**: object states & behaviors may be used only within the scope of the object & may be hidden from outside code.

* **Code re-use**: if an object already exists, it may be imported into any program, allowing for specialization of specific tasks.

* **Pluggability & debugging ease**: if a particular object is problematic, it may be removed and replaced with a different object.

## Classes
	
A class is a software blueprint or prototype that describes states & behaviors for the objects they create.

Analogously, there may be millions of cats in the world. Each cat evolved from the same set of dna blueprints and therefore contains the same components. In object-oritented terms, a cat is an instance of the class of objects known as cats.

### Creating a Cat Class

Create your source code file and name it `Cat.java`.

	$ touch Cat.java

Open `Cat.java` and enter into it the following code:

	public class Cat {
	    public String name;
	    public String speak() {
	        return "Meow!";
	    }
	}

This `Cat` class has state `name` and behavior `speak()`. Notice that this is not a complete application because it does not contain a `main` method. Some other class in the may be responsible for instantiating & using cat objects created with the `Cat` class.

## Inheritance

Inheritance refers to classes inheriting states & behaviors from their superclasses.

Object-oriented programming allows classes to inherit commonly used state and behavior from other classes. In the Java programming language, each class is allowed to have one direct superclass, and each superclass has the potential for an unlimited number of subclasses.

To create a subclass, use the `extends` keyword, followed by the name of the class to inherit from:

	class Cat extends Mammal {
		// fields and methods for Cat
	}

This gives `Cat` all the same fields and methods as `Animal`, yet allows its code to focus excusively on the features that make it unique. 

## Interfaces

Objects define their interaction with the outside world through the methods that they expose. Methods form the object's interface with the outside world.

An interface is a contract between a class and the outside world. When a class implements an interface it promises to provide the behavior published by that interface.

	interface Animal {
		void behavior_1(int input);
		void behavior_2(int input);
		void behavior_3(int input);
	}

To implement this interface, the name of your class would change (to a particular type of animal, such as mammal).

	class Mammal implements Animal {
		int variable_1 = 0;
		int variable_2 = 0;
		int variable_3 = 0;

		void behavior_1(int input){
			variable_1 = input;
		}

		void behavior_2(int input){
			variable_2 = input;
		}

		void behavior_3(int input){
			variable_3 = input;
		}
	}

Implementing an interface allows a class to become more formal about the behavior it promises to provide. Interfaces forme a contract between the class and the outside world, and this contract is enforced at build time by the compiler. If your class claims to implement an interface, all methods defined by that interface must appear in its source code before the class will successfully compile.

## Packages

A package is a namespace for organizing classes and interfaces in a logical manner. Placing code into packages makes managing large software projects easy to manage.

Because software written in Java programming language can be composed of thousands of individual classes, for which it makes sense to keep things organized by placing related classes and interfaces into packages
.
## Constructors

Every class has at least a constructor. Constructors are invoked when a class is instantiated to create an object.

---

# FORGIVE ME

* Have not added arrays
* Have not added variable declarations
* Finish packages
* Finish constructors

