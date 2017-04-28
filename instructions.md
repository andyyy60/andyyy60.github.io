# Basics of Java

In this section we cover the very basics of Java: primitive data types, operators, printing, conditional statements, and loops.

---

## Primitive Data Types

There are eight primitive data types in Java:

`boolean`

* Description: **true or false**
* Default: `false`
* Size: **1 bit**
* Example literals: `true`, `false`

`byte`

* Description: **twos complement integer**
* Default:  `0`
* Size:  **8 bits**
* Example literals: **(none)**

`char`

* Description: **Unicode character**
* Default:  `\u0000`
* Size:  **16 bits**
* Example literals: `'a'`, `'\u0041'`, `'\\'`

`short`

* Description: **twos complement integer**
* Default:  `0`
* Size:  **16 bits**
* Example literals: **(none)**

`int`

* Description: **twos complement integer**
* Default:  `0`
* Size:  **32 bits**
* Example literals: `-2`, `-1`, `0`, `1`, `2`

`long`

* Description: **twos complement integer**
* Default:  `0`
* Size:  **64 bits**
* Example literals: `-2L`, `-1L`, `0L`, `1L`, `2L`

`float`

* Description: **IEEE 754 floating point**
* Default:  `0.0`
* Size:  **32 bits**
* Example literals: `1.23e100f`, `-1.23e-100f`, `.3f`, `3.14F`

`double`

* Description: **IEEE 754 floating point**
* Default:  `0.0`
* Size:  **64 bits**
* Example literals: `1.23456e300d`, `-1.23456e-300d`, `1e1d`

---

## Operators

Next, we cover arithmetic & relational operators.

### Arithmetic

`+` addition

`-` subtraction

`*` multiplication

`/` division

`%` modulus

`++` increment

`--` decrement

### Relational

`==` equal to

`!=` not equal to

`>` greater than

`<` less than

`>=` greater than or equal to

`<=` less than or equal to

---

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

