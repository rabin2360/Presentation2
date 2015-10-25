##IntelliJ IDEA - Git Integration (V)
* Pulling files from a local/remote repository using IntelliJ IDE: If the files being edited in the IntelliJ IDE are connected the remote Git repository, Git provides the Pull function that acts as the combination of Fetch and Merge.
* To pull changes into the local repository from remote Git repository, the following steps can be performed:
    * In the IntelliJ IDE, select **VCS | Git | Pull**. It opens the Pull Changes dialog box that looks like below:
    
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

[Previous](Slide12_GitIntegrationIV.md) [Next](Slide14_DebuggerI.md)
