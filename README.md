# Presentation 2
Presentation 2 for CSCI 5828

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
       
## IntelliJ IDEA - Git Integration (I)
* IntelliJ IDEA has Git integration and allows the git functions to be performed from the IDE itself. IntelliJ allows to either create a local Git repository or push the files in the local Git repository to be pushed to GitHub.
* If local Git repository is preferred, IntelliJ allows the user to either clone the repository from GitHub and use locally or create a completely new project that is version controlled by Git locally.
* Git also allows the project being held locally and version controlled by Git to be pushed to remote repositories like GitHub.
* However, in order to get started with Git in IntelliJ IDE, the Git executable has to be downloaded to the local machine.
* The following method walks through the steps of creating a local Git repository:
    * Open the project that needs to version controlled.
    * Navigate to VCS | Import into Version Control | Create Git Repository.
    * In the Dialog Box that opens, specify the directory where Git local repository is to be created.
    * As needed, track the files of the project that need versioning.
    
* To explore ways to clone a remote Git repository, [click here] (https://www.jetbrains.com/idea/help/setting-up-a-local-git-repository.html).

## IntelliJ IDEA - Git Integration (II)
* Tracking unversioned files: After initializing the Git project, it allows the user to track files or keep the files in the project unversioned. 
* IntelliJ provides the Version Control window (Alt + 9), that has the Local Changes tab. Under Local Changes tab, all the files of the project that are tracked and untracked are differentiated. The following image shows the Version Control window with Local Changes tab selected. Under Local Changes tab, the untracked files are listed under Unversioned Files and the tracked Files are listed under the moniker Default. 

![Local Changes Window](https://github.com/rabin2360/Presentation2/blob/master/Presentation/localChangesTrackedUntrackedFiles.png)
* In order to track the unversioned files, in the Local Changes tab, select the Unversioned Files category. Under Unversioned Files category, select the file to be tracked. Right click the file name and select Add to VCS. In IntelliJ, files that are untracked and present locally appear brown in color. When the untracked files start getting tracked, they appear green in color. Another way to track a file is, select the untracked files that appear in the Project Tool window, right click the files, select Git | Add. This converts untracked files to tracked.

![Tracking A File](https://github.com/rabin2360/Presentation2/blob/master/Presentation/processOfTrackingAFile.png)
* In order to untrack a file, right click the file in the Project Tool window and select Git | Revert. The color of the file changes to brown in the Project Tool window indicating that the file is present locally and untracked.

![Untracking A File](https://github.com/rabin2360/Presentation2/blob/master/Presentation/revertingTrackedFile.png)

## IntelliJ IDEA - Git Integration (III)
* IntelliJ IDE and Git integration means the statuses of the file in a project a tracked compared to the last commit. Depending on the status of the file, the files in a project a different in color.
* File statuses in the IDE are tracked as following:
    * When a file is added to the project but has not been tracked, it is represented by brown color. For instance, the following screenshots have been created for the project and added to the folder where the presentation is being edited but have not been tracked yet. Hence, they appear brown in color.
    
    ![Filed added but not tracked](https://github.com/rabin2360/Presentation2/blob/master/Presentation/FileStatusBeforeTracked.png)
    
    * When a file is tracked, the color of the file changes from brown to green in color. It indicates that the file is being tracked but has not been committed yet.

    ![Filed added but not tracked](https://github.com/rabin2360/Presentation2/blob/master/Presentation/FileStatusAfterTracked.png)
        
    * When a file has been committed, it appears as black in color in the IntelliJ IDE.
    
    ![Filed added after committing](https://github.com/rabin2360/Presentation2/blob/master/Presentation/FileStatusAfterCommitting.png)
        
    * After a file has been committed, if it is modified the file appears a blue in color.
    
    ![Filed edited after committing](https://github.com/rabin2360/Presentation2/blob/master/Presentation/FileStatusAfterEditing.png)
        
* Similarly, each line in a file is also tracked. When a file is updated by adding a line, removing a life or editing a line, IntelliJ uses a color scheme to indicate the status of each line by coloring the gutter a different color.
* For line status in an editor:
    * The following picture shows the lines before editing, deleting and adding a line in the IntelliJ IDE.
    
    ![Gutter color before editing, deleting](https://github.com/rabin2360/Presentation2/blob/master/Presentation/GutterColorStart.png)
    
    * After committing a file, if a line in the committed file is change, the left gutter in the IntelliJ IDE turns blue in color as indicated by the following picture.
    
    ![Gutter color for modified line](https://github.com/rabin2360/Presentation2/blob/master/Presentation/GutterColorEditingLine.png)
    
    * After committing a file, if a line is added to the file, the left gutter in the IntelliJ IDE turns green in color as indicated by the following picture.
    
    ![Gutter color for adding a line](https://github.com/rabin2360/Presentation2/blob/master/Presentation/GutterColorNewLine.png)
        
    *  After committing a file, if a line is deleted from the file, the left gutter in the IntelliJ IDE displays a triangular sign as indicated by the following picture.
    
    ![Gutter color for deleting line](https://github.com/rabin2360/Presentation2/blob/master/Presentation/GutterColorDeletingLine.png)
    
##IntelliJ IDEA - Git Integration (IV)
* Pushing files to a local/remote repository using IntelliJ IDE: When committing a change from IntelliJ IDE, users have the option of either pushing the change to the local repository or to the remote repository. IntelliJ supports both functionality.
* In order to commit the changes to the local repository or remote repository,
    * Open the version control tool by performing one of the listed actions: Alt + 9 or following the sequence: View | Tools Windows | Version Control.
    * On the Local Changes tab window, display select the files to commit.
    [Picture]
    * Open the Commit Changes dialog box by performing one of the following actions:
        * On the tool window toolbar, select Commit Changes.
        * On the main menu, select VCS | Commit Changes.
        * On the main menu, select VCS | Git | Commit File.
    * The Commit Changes dialog box for IntelliJ looks like below where it allows the user to specify the author, perform actions like reformatting the code, performing code analysis, check to-do list, etc. before making the code commit. The Commit Changes Dialog box also contains the option to amend a commit, which erases the previous commit and replaces it with the new commit being made. The Commit Changes Dialog box looks like below:
     
     ![Commit Changes Dialog Box](https://github.com/rabin2360/Presentation2/blob/master/Presentation/CommitChangesDialogBox.png)
     
     * In the Commit Changes dialog box,  it also allows to compare the newly edited file to be compared to the last committed file. It shows areas where lines have been edited, added or deleted. Following pictures show how difference comparison works in IntelliJ:
     
     The following picture shows difference in comparison when lines in the previously committed file have been edited:
     ![Show diff editing lines] (https://github.com/rabin2360/Presentation2/blob/master/Presentation/DiffCompareEditedLines.png)

     The following picture shows difference in comparison when lines in the previously committed file have been added:
     ![Show diff new lines] (https://github.com/rabin2360/Presentation2/blob/master/Presentation/DiffCompareNewLines.png)

##IntelliJ IDEA - Git Integration (V)
* Pulling files from a local/remote repository using IntelliJ IDE: If the files being edited in the IntelliJ IDE are connected the remote Git repository, Git provides the Pull function that acts as the combination of Fetch and Merge.
* To pull changes into the local repository from remote Git repository, the following steps can be performed:
    * In the IntelliJ IDE, select VCS | Git | Pull. It opens the Pull Changes dialog box that looks like below:
    
      ![Pull Changes Dialog Box] (https://github.com/rabin2360/Presentation2/blob/master/Presentation/PullChangesDialogBox.png)
     
    * The Pull Changes dialog box contains the fields - Git root, current branch, remote, branches to merge and strategy:
        * Git Root: The drop down menu for Git root contains a list of paths to the local repository (i.e. folders in IntelliJ IDE). Select the path to the folder in which the files have to be updated. In the above dialog box, my Git Root is the folder containing Presentation 2.
        * Current Branch: The current branch is a read-only field in the Pull Changes dialog box. It shows the branch that is currently checked out in the local directory. When pulling the changes using IntelliJ IDE, the fetch and merge operation will be performed on the branch being displayed by the current branch field. In the above example, my current branch is master.
        * Remote: the drop-down list contains the link to the remote repository that are connected to the local folder in IntelliJ IDE. The refresh button next to the remote drop down menu refreshes the branches displayed in the Branches to Merge field. The branches displayed reflect the branches in the remote repository. In the above example, my remote repository is https://github.com/rabin2360/Presentation2.git
        * Branches to Merge: The check boxes next to the branches listed in the field allow the user to specify the branches to which changes should be applied (i.e. fetched and merged) when Pull function is completed by IntelliJ.
        * Strategy: The strategy drop down menu contains the following options:
            * Default: This is the option that is selected by default in the IDE.
            * Resolve: This option is selected when there are two HEADS - one HEAD in the current branch to which merge is applied to, another HEAD is the branch from which changes are being pulled.
            * Recursive: This option is selected, if only one branch needs to be pulled.
            * Octopus: This option is selected when pulling more than one branch at a time. This pull strategy does not work if it requires manual merges between the different branches.
            * Ours: This option is select if there is need to supersede old development history of side branches. This option allows merging any number of HEADS. All the HEADS are merged together with only the HEAD of the current branch persisting.
            * Subtree: This is modified recursive strategy.
        * No Commit: This allows the user to fetch the data from the remote repository without necessarily merging it. It allows the remote data to be fetched, inspected, make adjustments (if necessary) before finally merging into the local repository.
        * No Fast Forward: This allows the user to perform the fetch and merge operation where Git fast forward operation is not performed. To learn more about Git fast forward [click here](http://ariya.ofilabs.com/2013/09/fast-forward-git-merge.html).
        * Squash Commit: This allows the user to perform the Git squash function. Using squash commit, all the different branches are merged to the current branch as a single commit on top of the current HEAD. It exploits the Git squash feature.
        * Add log information: Selecting this option allows the user to augment the log information when pulling information. It allows the user to enter a one-line description in addition to capturing the name of the branches being merged.

##IntelliJ IDEA - Debugger (I)
* When writing a program, programmers usually run into three kinds of errors - syntax, runtime and logic errors.
* The syntax errors are caught by the IDE. They are very easy to find and fix.
* The logical errors are very difficult to find as the IDE does not recognize the fault in the logic. This is when using debugger in the IDE becomes extremely handy.
* Debugging features in IntelliJ IDE are comprehensive. Among all the features, the following will be discussed at length in the presentation.
    * Break points/ conditional breakpoints
    * Configuring the debugger
    * Inline Debugging
    * Exploring Frames

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

##IntelliJ IDEA - Debugging (III)
* Inline Debugging: IntelliJ IDEA also facilitates the debugging process by providing in line debugging that allows the values of the variables to be viewed in the source coude right next to the usage without forcing the user to look at the variables pane in the debugging window.
* To enable inline debuging in IntelliJ, follow the folloiwng steps:
    * Press ** View|Tool Windows| Debug** or Alt +5.
    * In the Debug tool window, click the Settings button and select **Show values in editor**.
      ![Enabling InLine Editor] (https://github.com/rabin2360/Presentation2/blob/master/Presentation/EnablingShowValuesInEditor.png)

* Using inLine debugging:

  ![Using inLine Debuggin](https://github.com/rabin2360/Presentation2/blob/master/Presentation/InLineDebugging.png)

##IntelliJ IDEA - Debugging (IV)
* Frames Window: When running the debugging session in IntelliJ idea, the local variables are created inside frames (also known as activation records) and pushed onto a stack. Hence, the frames that are created later are at the top of the stack. For instance, if a method call is made from the main method, the frames in IntelliJ will display both the main method and the method that is called from the main method. However, the called method is listed above the main method. On clicking the main method, all the variables that are present in the main method are displayed while, on clicking the called method, the variables that are visible within the scope of the called method are displayed in the Variables window.
* For the following code:
```    public static void main (String [] args)
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
