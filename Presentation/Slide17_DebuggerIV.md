##IntelliJ IDEA - Debugging (IV)
* Frames Window: When running the debugging session in IntelliJ idea, the local variables are created inside frames (also known as activation records) and pushed onto a stack. Hence, the frames that are created later are at the top of the stack. For instance, if a method call is made from the main method, the frames in IntelliJ will display both the main method and the method that is called from the main method. However, the called method is listed above the main method. On clicking the main method, all the variables that are present in the main method are displayed while, on clicking the called method, the variables that are visible within the scope of the called method are displayed in the Variables window.
* For the following code:
```  
public static void main (String [] args)
      {
           int mainVariable = 0;
   
           int x = 1;
           int y = 2;
           int z = 2;
   
           anotherMethod();
       }
   
   
       public static void anotherMethod()
       {
           int a = 1;
           int b = 2;
           int c = a+b;
           int d = b+c;
       }

```
* Selecting the `main()` frame, the following values are displayed in the Variables window. Also, `anotherMethod()` appears on top of `main` in the following window:
![Selecting the main frame](https://github.com/rabin2360/Presentation2/blob/master/Presentation/SelectingMainMethodFrame.png)

* Selecting the `anotherMethod()` frame, the following values are displayed in the Variables window.
![Selecting the anotherMethod frame](https://github.com/rabin2360/Presentation2/blob/master/Presentation/SelectingAnotherMethodFrame.png)

[Previous](Slide16_DebuggerIII.md) [Next](Slide18_Conclusion.md)
