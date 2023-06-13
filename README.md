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

if an error occured, check the `install.md` file

Now that we have the JDK (Java Development Kit; required only for development, coding) and JRE (Java Runtime Environment; required to run Java code and applications) installed, we can now start programming in java.

## Basics of java 

First, we will learn how to write a simple java program;
To create a simple Java program, you need to create a class that contains the main method.

### Step 1 : Creating a program

Create a file named `SimpleApp.java` and add a Java class that contains the main function.
Make it so the main function prints "Hello World!" on the standard output.

By convention, the main function is `public static` and takes a `String args[]` as its argument.
You can make it so it returns `void` or an `int`

The `println` function is contained inside `System.out` class


### Step 2 : Compiling and running the program

Now that we have created a .java file with a class that contains a main function, we can now compile and run it.

To compile a java program we can use the `javac` command (The c in javac means "compiler").

```bash
javac SimpleApp.java
```

We can also use the wildcard symbol to get all the files in a directory

```bash
javac *.java
```

By doing this, a `SimpleApp.class` file has been generated.
Basically, this file contains all the data of the original file as well as the compiled code in machine language.
It's an equivalent to .o or .obj file in C/C++

(*Java is a heavily object oriented language, so it is expected from an application to contain multiple .class files containing a single class.*)

To run the program we can use the `java` command followed by a class containing a main function.

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

## Simple Application in java

Now that you know how to run a java program we will now create a desktop application using the JavaFX library.
The prerequisites for creating this application are `maven` and `IntelliJ Idea IDE`.
If you do not have theses, check the `install.md` file.

Create a new maven project by using the following command :

```bash
mvn archetype:generate -DgroupId=com.WorskshopJava.app -DartifactId=WorkshopJava-app -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.4 -DinteractiveMode=false
```

Under this directory you will notice the following *standard project structure*.

```text
WorkshopJava-app
|-- pom.xml
`-- src
    |-- main
    |   `-- java
    |       `-- com
    |           `-- WorkshopJava
    |               `-- app
    |                   `-- App.java
    `-- test
        `-- java
            `-- com
                `-- WorkshopJava
                    `-- app
                        `-- AppTest.java
```

The `src/main/java` directory contains the project source code, the `src/test/java` directory contains the test source, and the `pom.xml` file is the project's Project Object Model, or POM.

The `pom.xml` file is the core of a project's configuration in Maven.
It is a single configuration file that contains the majority of information required to build a project in just the way you want.
The POM is huge and can be daunting in its complexity, but it is not necessary to understand all of the intricacies just yet to use it effectively.

### What did you do?

You executed the Maven goal `archetype:generate`, and passed in various parameters to that goal. The prefix `archetype` is the plugin that provides the goal.
This `archetype:generate` goal created a simple project based upon a `maven-archetype-quickstart` archetype.
Suffice it to say for now that a plugin is a collection of goals with a general common purpose. For example the jboss-maven-plugin, whose purpose is "deal with various jboss items".


### Before starting coding

Just to make sure that everything is working fine, go in your project directory (Where the pom.xml is located) and run this command

```bash
mvn compile
```
This command will (as you've guessed) compile the project based on the infos in the `pom.xml` file.
The outpur program is find by default in the `/target/` directory.
If there is an error during compilation, call the Workshop guy.

```bash
mvn package
```
This command will created a `.jar` file (an executable java file)


Add this line to the properties tag to make it easier to execute your project once it is compiled

```xml
<exec.mainClass>com.WorkshopJava.app.App</exec.mainClass>
```

Now your properties tab should look like this

```xml
<properties>
    <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
    <maven.compiler.source>1.7</maven.compiler.source>
    <maven.compiler.target>1.7</maven.compiler.target>
    <exec.mainClass>com.WorkshopJava.app.App</exec.mainClass>
</properties>
```
in fact... it does'nt work...














## Go further with JavaFX
