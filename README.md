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


### IntelliJ IDE

Under this directory you will notice the following *standard project structure*.

```text
WorkshopJava-app
|-- pom.xml
`-- src
    |-- main
    |   `-- java
    `-- test
        `-- java
```

The `src/main/java` directory contains the project source code, the `src/test/java` directory contains the test source, and the `pom.xml` file is the project's Project Object Model, or POM.

The `pom.xml` file is the core of a project's configuration in Maven.
It is a single configuration file that contains the majority of information required to build a project in just the way you want.
The POM is huge and can be daunting in its complexity, but it is not necessary to understand all of the intricacies just yet to use it effectively.

Add theses lines to your `pom.xml` to load FXGL

```xml
    <dependencies>
        <dependency>
            <groupId>com.github.almasb</groupId>
            <artifactId>fxgl</artifactId>
            <version>17.2</version>
            <scope>compile</scope>
        </dependency>
    </dependencies>

    <build>
        <plugins>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-jar-plugin</artifactId>
                <version>3.0.2</version>
                <configuration>
                    <release>17</release>
                </configuration>
            </plugin>
        </plugins>
    </build>
```

Create a `App.java` file in src/

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
This command will create a `.jar` file (an executable java file)

From now on, you can use IntelliJ idea IDE to make it easier to run your java program.

```bash
intellij-idea-community .
```

### Setup JavaFX environment

Downlaod JavaFX : https://gluonhq.com/products/javafx/

Extract it.

Add an environment variable pointing to the lib directory of the runtime: 

export PATH_TO_FX=path/to/javafx-sdk-20/lib

javac --module-path $PATH_TO_FX --add-modules javafx.controls HelloFX.java

### Creating a Java Application using JavaFX

JavaFX is a Java library used to develop Desktop applications as well as Rich Internet Applications (RIA).
The applications built in JavaFX, can run on multiple platforms including Web, Mobile and Desktops.
(*Learn more abour JavaFX : https://openjfx.io/*)


#### Step 1

Add JavaFX dependencies to the `pom.xml`

```xml
<dependency>
    <groupId>org.openjfx</groupId>
    <artifactId>javafx-controls</artifactId>
    <version>12.0.2</version>
</dependency>
```
Then, add the plugin

```xml
<plugin>
    <groupId>org.openjfx</groupId>
    <artifactId>javafx-maven-plugin</artifactId>
    <version>0.0.8</version>
    <configuration>
        <mainClass>hellofx/org.openjfx.App</mainClass>
    </configuration>
</plugin>
```

In the App.java file, add the following line to import JavaFX application class :

```java
import javafx.application.Application;
```

Make the `App` class inherit from `Application`

In Java, we use the `entends` keyword to make a class inherit from another class.

Then, override the `start` method. This method take a `Stage` class as arguments. Call it `primaryStage`.

In Java, we use the `@Override` keyword to override an inherited method.

```java
    @Override
    public void Do_something(int nb) { ... }
```


## Go further with JavaFX
