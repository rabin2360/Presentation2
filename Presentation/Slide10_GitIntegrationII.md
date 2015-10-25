## IntelliJ IDEA - Git Integration (II)
* Tracking unversioned files: After initializing the Git project, it allows the user to track files or keep the files in the project unversioned. 
* IntelliJ provides the Version Control window (Alt + 9), that has the Local Changes tab. Under Local Changes tab, all the files of the project that are tracked and untracked are differentiated. The following image shows the Version Control window with Local Changes tab selected. Under Local Changes tab, the untracked files are listed under Unversioned Files and the tracked Files are listed under the moniker Default. 

![Local Changes Window](https://github.com/rabin2360/Presentation2/blob/master/Presentation/localChangesTrackedUntrackedFiles.png)
* In order to track the unversioned files, in the Local Changes tab, select the Unversioned Files category. Under Unversioned Files category, select the file to be tracked. Right click the file name and select Add to VCS. In IntelliJ, files that are untracked and present locally appear brown in color. When the untracked files start getting tracked, they appear green in color. Another way to track a file is, select the untracked files that appear in the Project Tool window, right click the files, select Git | Add. This converts untracked files to tracked.

![Tracking A File](https://github.com/rabin2360/Presentation2/blob/master/Presentation/processOfTrackingAFile.png)
* In order to untrack a file, right click the file in the Project Tool window and select **Git | Revert**. The color of the file changes to brown in the Project Tool window indicating that the file is present locally and untracked.

![Untracking A File](https://github.com/rabin2360/Presentation2/blob/master/Presentation/revertingTrackedFile.png)

[Previous](Slide9_GitIntegrationI.md)  [Next](Slide11_GitIntegrationIII.md)
