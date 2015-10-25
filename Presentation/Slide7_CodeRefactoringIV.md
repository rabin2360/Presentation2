## IntelliJ IDEA - Code Refactoring (IV)
* Pulling and pushing members: The Pull Members Up refactoring allows subclass members to be pulled into the superclass or an interface, or pulling an interface to a superinterface. The Push Members Down refactoring pushes the class members to subclasses or subinterface. When pushing down, the members are relocated to direct subclasses/interfaces only.
* Sample code before Push Members Down refactoring:

![Sample Code Before Refactoring](https://github.com/rabin2360/Presentation2/blob/master/Presentation/beforePushDownRefactoring.png)

* Example of Push Members Down refactoring:

![Sample Code After Refactoring](https://github.com/rabin2360/Presentation2/blob/master/Presentation/afterPushDownRefactoring.png)

For the aforementioned example, there exists a class `ParentClass` which is inherited by `ChildClass`. Before the Push Members Down refactoring, the `ParentClass` contains a method `MethodToBePushed()`. For the purpose of the example, the method `MethodToBePushed()` gets pushed to the `ChildClass`. All of this is done easily by using the Push Members Down.

* Similarly, the methods that are present in the child class can easily be pulled up by the super class (or pullling methods from interface to superinterface). This is achieved by using Push Members Up Refactoring provided by the IntelliJ IDE.

* Way(s) to pull/push methods in IntelliJ:
      1. In the code editor, place the cursor within the name of the class whose method is being push down or pulled up.
      2. From the menu select **Refactor | Pull Members Up** or **Refactor | Push Members Down**.
      3. In the Pull Members Up or Push Members Down dialog box, select the classes that are to be pulled up or pushed down.
      4. To move a method as abstract, select the check box in the column Make abstract.
      5. Click Refactor to pull or push a method.


[Previous](Slide6_CodeRefactoringIII.md) [Next](Slide8_CodeRefactoringV.md)
