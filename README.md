# workshopJavaApp

## What is Java and what is it used for

Java is a programming language and a platform. Java is a high level, robust, object-oriented and secure programming language.

Java was developed by Sun Microsystems (which is now the subsidiary of Oracle) in the year 1995. James Gosling is known as the father of Java. Before Java, its name was Oak. Since Oak was already a registered company, so James Gosling and his team changed the name from Oak to Java.

*Learn more about Java history at https://www.javatpoint.com/history-of-java*

Platform: Any hardware or software environment in which a program runs, is known as a platform. Since Java has a runtime environment (JRE) and API, it is called a platform.

Java is an object-oriented programming language. Everything in Java is an object. Object-oriented means we organize our software as a combination of different types of objects that incorporate both data and behavior.

Basic concepts of OOPs are:
* Object
* Class
* Inheritance
* Polymorphism
* Abstraction
* Encapsulation

This workshop will not cover all of theses concepts, but feel free to check them out after this workshop !

*Learn more about Java features at : https://www.javatpoint.com/features-of-java*

## Prerequisites

To learn Java, you must have the basic knowledge of C/C++ programming language.

First check if java is installed

```bash
java -version
```

if an error occured, check the install.md file

Now that we have the JDK (Java Development Kit; required only for development, coding) and JRE (Java Runtime Environment; required to run Java code and applications) installed, we can now start programming in java.

## Basics of java 

(Main class, compiling and runnning Java code)

First, we will learn how to write a simple java program;
To create a simple Java program, you need to create a class that contains the main method.

### Step 1 : Creating a program

Create a file named **SimpleApp.java** and add a Java class that contains the main function.
Make it so the main function prints "Hello World!" on the standard output.

By convention, the main function is **public static** and takes a **String args[]** as its argument.
You can make it so it returns *void* or an *int*

The *println* function is contained inside *System.out* class


### Step 2 : Compiling and running the program

Now that we have created a .java file with a class that contains a main function, we can now compile and run it.

To compile a java program we can use the *javac* command (The c in javac means "compiler").

```bash
javac SimpleApp.java
```

We can also use the wildcard symbol to get all the files in a directory

```bash
javac *.java
```

By doing this, a "SimpleApp.class" file has been generated.
Basically, this file contains all the data of the original file as well as the compiled code in machine language.
It's an equivalent to .o or .obj file in C/C++

(*Java is a heavily object oriented language, so it is expected from an application to contain multiple .class files containing a single class.*)

To run the program we can use the *java* command followed by a class containing a main function.

```bash
java SimpleApp
```

It won't work if we put the file extension as argument. It will be like if we write

```bash
java SimpleApp.class.class
```

Note that I said *a class containing a main function* because it's totally possible for an application to conrain mulple classes containing a main function.

The expected output should be :

```text
Hello World!!
```

## Advanced concepts of java

...

## Application in java

...

