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

* For the following code
```
        int x = 6;
        x = x + x;
```

On writing the code above, IntelliJ performs the static code analysis as follows:

![On the fly code analysis part 2](https://github.com/rabin2360/Presentation2/blob/master/Presentation/OnTheFlyCodeAnalysisPart2.png)

## IntelliJ IDEA - Code Refactoring (I)
* Refactoring allows the developers to change the written code without changing the behavior of the code. Usually the process of refactoring the code leads to a readable code which in turn makes maintaining and extending the existing code a simpler task.
*IntelliJ IDEA provides a wide variety of code refactorings. To name a few, below is the list:
    1. Change Method Signature
    2. Change Class Signature
    3. Pull Members up or push members down
    4. Replace Inheritence with Delegation
    5. Replace Method Code Duplicates

## IntelliJ IDEA - Code Refactoring (II)
* Change Method Signature: In IntelliJ, changing the method signature can be performed in various ways. Below are a few ways to change the method signature in IntelliJ:
    1. Change the method name and return type
    2. Change parameter names and re-order parameters
    3. Add new parameters

* The following picture shows the code before Change Method Signature refactoring is performed. Using IntelliJ, in the following code,
    1. the name of `oldMethodName` will be changed to `newMethodName`.
    2. the order of the parameters `(int parameter1, double parameter2)` will be changed to `(double parameter2, int parameter1)`.
    3. the return type of the method `oldMethodName` will be changed from `int` to `double`.
    4. the parameter mame will be changed from `parameter1` to `newParameter1` and `parameter2` to `newParameter2`. The default value of newParameter1 will stay 1 and newParameter2 will stay 0.
    5. a new parameter will be added by the name 'newParameter3' with a default value of 3.

* Before refactoring the sample code:

![Before refactoring](https://github.com/rabin2360/Presentation2/blob/master/Presentation/beforeMethodRefactoring.png)

* Process of refactoring the sample code:
![How to refactor a method](https://github.com/rabin2360/Presentation2/blob/master/Presentation/processOfChangingMethodSignature.png)
* After refactoring the sample code:
![After refactoring](https://github.com/rabin2360/Presentation2/blob/master/Presentation/afterMethodRefactoring.png)

* As seen from the screen shot after performing the refactoring, based on the refactoring done in the method `newMethodName`, the call to `newMethodName` in method `anotherMethodName` in class `SecondClass` changes accordingly where
    1. the position of the default values are changed accordingly for all the parameters
    2. when adding a new parameter, the default value for the new parameter is added automatically on the function call

* Way to change a method signature in IntelliJ:
    1. In the code editor, place the cursor within the name of the method whose signature is to be changed.
    2. Perform one of the following:
        * Press `Ctrl + F6`.
        * Choose Refactor | Change Signature from the context menu.
        * Chose Refactor | Change Signature in the main menu.
    3. In the Change Signature dialog box, change the method visibility scope, method name, return type, manage parameters, etc. as desired.

## IntelliJ IDEA - Code Refactoring (III)
* Change Class Signature: In IntelliJ, the Change Class Signature refactoring allows to turn a class into a generic and then allows the user the manipulate the parameters. When the refactoring is performed, all the class calls, implementations and overrides are corrected automatically.

* Sample code before refactoring:
![Sampe Code Before Refactoring](https://github.com/rabin2360/Presentation2/blob/master/Presentation/beforeClassSignatureRefactoring.png)

* Process of refactoring the class:
![Process of refactoring the class](https://github.com/rabin2360/Presentation2/blob/master/Presentation/processOfChangingClassSignature.png)

* Sample code after refactoring:

![Sample Code After Refactoring](https://github.com/rabin2360/Presentation2/blob/master/Presentation/afterClassSignatureRefactoring.png)

As the picture indicates, when the sample code is refactored to change the class signature, the reference to the class `FirstClass` in the `SecondClass` also changes to `FirstClass<String, Double> myClass` from `FirstClass myClass`. When refactoring the code, `classParameter1` was declared as `String` and `classParameter2` was declared as `Double`. 

* * Way to change a class signature in IntelliJ:
      1. In the code editor, place the cursor within the name of the class whose signature is to be changed.
      2. Perform one of the following:
          i. Press `Ctrl + F6`.
          ii. Choose Refactor | Change Signature from the context menu.
          iii. Chose Refactor | Change Signature in the main menu.
      3. In the Change Class Signature dialog, add, remove or edit the name and the default value of parameters as desired.

## IntelliJ IDEA - Code Refactoring (IV)
* Pulling and pushing members: The Pull Members Up refactoring allows subclass members to be pulled into the superclass or an interface, or pulling an interface to a superinterface. The Push Members Down refactoring pushes the class members to subclasses or subinterface. When pushing down, the members are relocated to direct subclasses/interfaces only.
* Sample code before Push Members Down refactoring:

![Sample Code Before Refactoring](https://github.com/rabin2360/Presentation2/blob/master/Presentation/beforePushDownRefactoring.png)

* Example of Push Members Down refactoring:

![Sample Code After Refactoring](https://github.com/rabin2360/Presentation2/blob/master/Presentation/afterPushDownRefactoring.png)

For the aforementioned example, there exists a class `ParentClass` which is inherited by `ChildClass`. Before the Push Members Down refactoring, the `ParentClass` contains a method `MethodToBePushed()`. For the purpose of the example, the method `MethodToBePushed()` gets pushed to the `ChildClass`. All of this is done easily by using the Push Members Down.

* Similarly, the methods that are present in the child class can easily be pulled up by the super class (or pullling methods from interface to superinterface). This is achieved by using Push Members Up Refactoring provided by the IntelliJ IDE.

* Way to pull/push methods in IntelliJ:
      1. In the code editor, place the cursor within the name of the class whose method is being push down or pulled up.
      2. From the menu select Refactor | Pull Members Up or Refactor | Push Members Down.
      3. In the Pull Members Up or Push Members Down dialog box, select the classes that are to be pulled up or pushed down.
      4. To move a method as abstract, select the check box in the column Make abstract.
      5. Click Refactor to pull or push a method.
      
## IntelliJ IDEA - Code Refactoring (V)
* Replace inheritence with delegation: Replacing inheritence with delegation can substantially improve the class design if the subclass does not extend the functionality of the superclass. IntelliJ provides a way to refactor the code such that there is removal of inheritence from the code design. The functionality of the superclass is preserved when refactoring.
* The following code uses inheritence. 
```
    public abstract class ParentClass
    {
        public void ParentingMethod()
        {
            //code here
        }

        public abstract void ParentRelationship();

    }

    public class ChildClass extends ParentClass
    {

        public void ChildActivityMethod()
        {
            //code here
        }
        
        public void ParentRelationship()
        {
            //parenting relationship code
        }
    }
```

* In the above code, the `ChildClass` extends the `ParentClass` and implements the abstract method `ParentRelationship()`. Using IntelliJ, the aforementioned code can be refactored as follows, where the integrity of the parent class stays the same. However, IntelliJ creates a private inner class in the `ChildClass`. This private inner class inherits from the superclass. Selected methods from the `ParentClass` are invoked in the private inner class. After refactoring the code looks something like below:
```
    public abstract class ParentClass
    {
        public void ParentingMethod()
        {
            //code here
        }

        public abstract void ParentRelationship();

    }

    public class ChildClass {

        private final InnerClassName parentClass = new InnerClassName();

        public void ChildActivityMethod()
        {
            //code here
        }

        public ParentClass getParentClass() {
            return parentClass;
        }

        public void ParentRelationship() {
            parentClass.ParentRelationship();
        }

        private class InnerClassName extends ParentClass {
            public void ParentRelationship()
            {
                //parenting relationship code
            }
        }
    }
```

* From the code excerpt, it is observed, that the new inner class created in the `ChildClass` is `InnerClassName` that invokes the method `ParentRelationShip()`. Hence, `InnerClassName` is used to delegate the task of calling `ParentRelationShip()` from `ChildClass` to `ParentClass`. Inheritence is not used to call `ParentRelationShip()` in this case.

* When refactoring, IntelliJ creates a private inner class that inherits the former superclass. Following that, selected methods of the parent class are invoked via the new inner class.

* Way to replace inheritence with delegation in IntelliJ:
      1. In the code editor, place the cursor in the child class method name.
      2. From the menu select Refactor | Replace Inheritence with Delegation.
      3. In the Replace Inheritence with Delegation box, 
        * specify the parent object in the field 'Replace with delegation inheritence from'.
        * in the 'Inner Class Name' field, specify the name for the inner class.
        * in the 'Delegate members' area, select the methods that will be delegated through the inner class.
        * finally, select 'Refactor'.
       
* Maven, Gradle, Refactoring, Debugger, Decompile
