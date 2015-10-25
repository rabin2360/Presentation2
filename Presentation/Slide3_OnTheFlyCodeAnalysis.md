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

[Previous](Slide2_SmartCodeCompletion) [Next](Slide4_CodeRefactoringI)
