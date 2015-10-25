## IntelliJ IDEA - Code Refactoring (III)
* Change Class Signature: In IntelliJ, the Change Class Signature refactoring allows to turn a class into a generic and then allows the user the manipulate the parameters. When the refactoring is performed, all the class calls, implementations and overrides are corrected automatically.

* Sample code before refactoring:
![Sampe Code Before Refactoring](https://github.com/rabin2360/Presentation2/blob/master/Presentation/beforeClassSignatureRefactoring.png)

* Process of refactoring the class:
![Process of refactoring the class](https://github.com/rabin2360/Presentation2/blob/master/Presentation/processOfChangingClassSignature.png)

* Sample code after refactoring:

![Sample Code After Refactoring](https://github.com/rabin2360/Presentation2/blob/master/Presentation/afterClassSignatureRefactoring.png)

As the picture indicates, when the sample code is refactored to change the class signature, the reference to the class `FirstClass` in the `SecondClass` also changes to `FirstClass<String, Double> myClass` from `FirstClass myClass`. When refactoring the code, `classParameter1` was declared as `String` and `classParameter2` was declared as `Double`. 

* Way(s) to change a class signature in IntelliJ:
      1. In the code editor, place the cursor within the name of the class whose signature is to be changed.
      2. Perform one of the following:
          * Press **Ctrl + F6**.
          * Choose **Refactor | Change Signature** from the context menu.
          * Chose **Refactor | Change Signature** in the main menu.
      3. In the Change Class Signature dialog, add, remove or edit the name and the default value of parameters as desired.

