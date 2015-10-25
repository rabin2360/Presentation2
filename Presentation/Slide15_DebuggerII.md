##IntelliJ IDEA - Debugger (II)
* Break point/conditional breakpoints: IntelliJ allows breaks to be set in the executable lines of code. IntelliJ has several types of breakpoints that can be used according to the debugging needs. When a breakpoint is set in the code, it is marked with a red stripe, after the breakpoint has been reached, the red strip changes to blue.
* The following are the different types of breakpoints:
    * Line Breakpoint: The breakpoints are assigned to lines of code. They are represented by a red dot with a check mark within it. For instance,
    
      ![Line Breakpoint] (https://github.com/rabin2360/Presentation2/blob/master/Presentation/LineBreakPoint.png)
      
    * Temporary Line Breakpoint: The breakpoints are assigned to lines of code but they are removed after being hit. They are represented by a red dot circle with 1 displayed within the circle.
    
      ![Temporary Line Breakpoint] (https://github.com/rabin2360/Presentation2/blob/master/Presentation/TemporaryBreakPoint.png)
     
    * Method Breakpoint: Method breakpoints stop the program when entering and exiting the method. They allow debugging by attaching the breakpoint to a method name. Using method breakpoint can significantly slow down the application. The method breakpoints are represented by a red dot with four smaller black dots in the red dot.

      ![Method Breakpoint] (https://github.com/rabin2360/Presentation2/blob/master/Presentation/MethodBreakPoint.png)
      
    * Exception Breakpoint: This breakpoint is triggered when the specified exception is triggered in the program. IntelliJ IDEA provides exception breakpoints for Java and JavaScript. The exception breakpoint is represented by a red dot with a lightning bolt within the red dot.
    
      ![Exception Breakpoint] (https://github.com/rabin2360/Presentation2/blob/master/Presentation/ExceptionBreakPoint.png)
      
    * Field Watchpoint: A watchpoint is a special breakpoint that stops the application whenever the avlaue of the given expression changes. It is represented by a red dot that encircles a dash sign in it. If `test` is the variable being watched, before debugging, it looks like below
    
      ![Field WatchPoint - Before] (https://github.com/rabin2360/Presentation2/blob/master/Presentation/BeforeWatchPointTriggered.png) 
    
       After debugging, it looks like below:
        
       ![Field Watchpoint - After] (https://github.com/rabin2360/Presentation2/blob/master/Presentation/AfterWatchPointTrigger.png) 
      
    * JavaScript/Flex/PHP Breakpoints: IntelliJ also allows to set breakpoints in JavaScript, Flex and PHP files. They are identical to the line breakpoints that are set in Java.  

[Previous](Slide14_DebuggerI.md) [Next](Slide16_DebuggerIII.md)
