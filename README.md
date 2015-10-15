# Presentation 2
Presentation 2 for CSCI 5828

IntelliJ Features to be covered:
## Introduction
* IntelliJ IDEA is a Java IDE (Integrated Development Environment) developed by JetBrains. IntelliJ IDEA offers supports for development frameworks, mobile development, developer tools and web development.
* Some of the development frameworks, mobile development platoforms, developer's tools and web development languages supported by IntelliJ IDEA IDE are:

* Development Frameworks:
    1. Java EE
    2. Spring
    3. GWT
    4. Grails
    5. Play

* Mobile Development platforms:
    1. Android
    2. PhoneGap
    3. Cordova
    4. Ionic

* Developer's tools:
    1. Maven
    2. Gradle
    3. Git
    4. SVN
    5. Mercurial

* Web Development Languages:
    1. JavaScript
    2. HTML
    3. CSS

## IntelliJ IDEA - Feature(s)
* Smart Code Completion:
* On-the-fly Code Analysis
* Advanced Refactorings
* Version Control Tools
    1. Git
        i. How to connect to Git:
        ii. Creating commits:
        iii. Cloning:
        iv. Pushing to the master:
        v. Visualization:
    2. SVN
    3. Mercurial
* Build Tools
    1. Maven
    2. Gradle
    3. Gant

## IntelliJ IDEA - Smart Code Completion
* IntelliJ allows the developer to be more productive by providing intelligent code completion. The intelligent code completion is supported for Java, Scala, Groovy, JavaScript, HTML, CSS amongst other programming languages.
* The code completion feature in IntelliJ helps the developers to complete names of classes, methods, fields and keywords that are within the visibility of the **current scope**. For instance,

![Instant Code completion](https://github.com/rabin2360/Presentation2/blob/master/Presentation/InstantCodeCompletion.png)

 This boots the productivity of the developer.

## IntelliJ IDEA - On-the-fly Code Analysis
* IntelliJ performs static code analysis to determine places of probable bugs, locate dead code, improvide code structure and detect performance issues without executing the code being written. This makes it easier for developers to write the code and identify problems even before executing the code.
* For the following code
```
 boolean value = false;

        if(value == true)
        {
            System.out.println("This code will never be executed !");
        }
        else
        {
            System.out.println("This statement will always be executed!");
```

On writing the code above, IntelliJ performs the static code analysis as follows:
![On the fly code analysis](https://github.com/rabin2360/Presentation2/blob/master/Presentation/OnTheFlyCodeAnalysis.png)

## IntelliJ IDEA - Code Refactoring (I)
* Refactoring allows the developers to change the written code without changing the behavior of the code. Usually the process of refactoring the code leads to a readable code which in turn makes maintaining and extending the existing code a simpler task.
*IntelliJ IDEA provides a wide variety of code refactorings. To name a few, below is the list:
    1. Change Class Signature
    2. Change Method Signature
    3. Pull Members up
    4. Push Members down
    5. Replace Inheritence with Delegation
    6. Replace Method Code Duplicates

## IntelliJ IDEA - Code Refactoring (II)
### Change Method Signature: In IntelliJ, Change Method Signature refactoring can be used to achieve a wide array of results. Below are a few of ways to Change Method Signature in IntelliJ:
* Change the method name and return type.
* Change parameter names and re-order parameters
* Add new parameters

### The following picture shows the code before Change Method Signature refactoring is performed. Using IntelliJ, in the following code,
* the name of `oldMethodName` will be changed to `newMethodName`.
* the order of the parameters `(int parameter1, double parameter2)` will be changed to `(double parameter2, int parameter1)`.
* the return type of the method `oldMethodName` will be changed from `int` to `double`.
* the parameter mame will be changed from `parameter1` to `newParameter1` and `parameter2` to `newParameter2`. The default value of newParameter1 will stay 1 and newParameter2 will stay 0.
* a new parameter will be added by the name 'newParameter3' with a default value of 3.

[oldMethodRefactoring]

[Process]

[newMethodRefactoring]

As seen from the screen shot after performing the refactoring, based on the refactoring done in the method `newMethodName`, the call to `newMethodName` in method `anotherMethodName` in class `SecondClass` changes accordingly where
* the position of the default values are changed accordingly for all the parameters
* when adding a new parameter, the default value for the new parameter is added automatically on the function call


* Maven, Gradle, Refactoring, Debugger, Decompile
