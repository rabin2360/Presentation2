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

* Way(s) to replace inheritence with delegation in IntelliJ:
      1. In the code editor, place the cursor in the child class method name.
      2. From the menu select **Refactor | Replace Inheritence with Delegation**.
      3. In the Replace Inheritence with Delegation box, 
        * specify the parent object in the field 'Replace with delegation inheritence from'.
        * in the 'Inner Class Name' field, specify the name for the inner class.
        * in the 'Delegate members' area, select the methods that will be delegated through the inner class.
        * finally, select 'Refactor'.
       
[Previous](Slide7_CodeRefactoring.md)  [Next](Slide9_GitIntegrationI.md)
