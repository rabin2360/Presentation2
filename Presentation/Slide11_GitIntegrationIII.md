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

[Previous] (Slide10_GitIntegrationII.md) [Next](Slide12_GitIntegrationIV.md)
