# Git and Github

### What is Source/Version control?
* A way of tracking your files progress over time or a view of how your project progressed over time
* It is usually saved in a series of snapshots and branches,which you can move back and forth between.
* Allows distribute ur file changes over time.
* prevent against data loss/damage by creating backup snapshots.
* manage complex project structures easily.
  
### What is Git?
* Git is a source control.
* popular 
* lot of docs and support
* lots of integration with other application eg github,


### Difference between git and github
* Github is an application allowing to store remote repositories(hub to git).
* Github can interact with local machine through push/pull system on ur local machine.
* Github used primarily to allow other people to add to the project (ex open source projects).
* Github allows more people than just you to see and interact with the repository.
* Github is sort of platform to use git.
* Git is version control software allowing you to take snapshots & distribute yout creation and modifications over time.
* Github is an application allowing you to store and interact with ur repositories on a remote server as well as adding more features () eg: publicity,license,collaboartors.
* Git is bones and flesh of SC while github gives u the platform to work with ur repository easier.

### Installing Git
* We need kind of shell or a command prompt
* https://git-scm.com/downloads
* gitbash
![gitbash](https://user-images.githubusercontent.com/43897511/50851841-92e92400-1343-11e9-9f1b-fc0461ba74dd.PNG)
* Test git is working or not
  * Open gitbash
  * git --version  (_version of git installed_)
  
### Repositories
* data storage and full history and source control of projects
* can be hosted either locally or on a shared server such as github
* most repository are stored on github , while contributors make copies of the repo on their machine and update the repository using the push/pull system
* any repository stored somewhere other than locally is called a remote repository
* repository is timelines of entire project including all previously changes whereas directories or wrkng directoris are projects at their current state in timelines
* any local directory interacting with a repo is technically a repository itself,however call it as local repository

### Git workflow
* before git tracks any change , it goes through a long chain of operations and tasks
	* working directory(projects at their current state in timelines) 
	* changes/modification
	* Staging area(bundle of all modifications to the project that are going to be commit)
	* commit(similar to taking snapshot of the current state of the project , then storing it on a timelines)
	* local repository 
	* push 
	* remote repository

### Creating new repository

* Add a text file in the folder "learngit.txt"
* Create a local directory "Projects/Learning"
* Move to the terminal and go to the path "/c/Users/leo_a/Documents/Projects/Learning"

### Initializing and adding git repository to staging area
* now we try to add the file using git 

![gitaddnostagingarea](https://user-images.githubusercontent.com/43897511/50918794-d48ed300-1406-11e9-8087-a5f5a4e7e368.PNG)
_no repository is initialized,we need to initialize it_

* ![gitinit](https://user-images.githubusercontent.com/43897511/50918966-3cddb480-1407-11e9-8176-81979b6e86e3.PNG)
new git repository initialized which have all detail about the project 

![initfolder](https://user-images.githubusercontent.com/43897511/50919075-7f06f600-1407-11e9-93d9-268d849b0425.PNG)
* Check staging area current status
![gitstatus](https://user-images.githubusercontent.com/43897511/50919300-0ce2e100-1408-11e9-8885-0b6353c7aff8.PNG)
_staging area have no commits_

* Add a file in staging area
"git add learngit.txt"

* Check staging area status 
![addstatus](https://user-images.githubusercontent.com/43897511/50919439-706d0e80-1408-11e9-8f42-d2556e8f7996.PNG)
_one file added for commit in staging area_

### Working with  multiple files
*  
![1](https://user-images.githubusercontent.com/43897511/50919782-5ed83680-1409-11e9-8330-e836587d9d0c.PNG)
Adding/Deleting/Updating in the staging area
![2](https://user-images.githubusercontent.com/43897511/50919835-83cca980-1409-11e9-9e2a-d406efe11018.PNG)
![3](https://user-images.githubusercontent.com/43897511/50919866-9c3cc400-1409-11e9-895c-d67146f17964.PNG)
![4](https://user-images.githubusercontent.com/43897511/50919872-a1017800-1409-11e9-837a-9d5213043b78.PNG)

### Removing file from directory 
* "git rm <filename>" or 
* force remove "git rm -f <filename>"
*  Untrack some files/ignore files or just remove files from staging area(do not delete from directory) 
	*"git rm --cached <filename>"
  
### User name and user email git global configuration

*  Commit (takes a snapshot of all the changes done at the time and store them in a tree)
 ![gitcommitbefrusername](https://user-images.githubusercontent.com/43897511/50920926-52a1a880-140c-11e9-9d10-5331e45c0b13.PNG)
  * _no username and account assigned, we have assign that before any commit , its juts one time process_
  * _git config --global user.email <user email>_
  * _git config --global user.name <user name>_
  
### Commit 
  ![commit](https://user-images.githubusercontent.com/43897511/50921245-2d616a00-140d-11e9-9ed5-3a9715210358.PNG)
  * _ m flag is for message , you can put any message according to your wish_
  * If you want to commit only tracked files use
  * _git commit -a - m "Your message"
  * commit untracked files
  
### Git log
  * See history of changes
  * git log
  * if we want to see changes in a single line
  * git log --oneline
  ![oneline](https://user-images.githubusercontent.com/43897511/50929867-fe0a2780-1423-11e9-995b-5be95db47129.PNG)
  ![log](https://user-images.githubusercontent.com/43897511/50921441-b082c000-140d-11e9-833f-a7b8087c8abf.PNG)
  
### Moving between commits
  * _git checkout <commit ID> (you can find it by git log)_
  * _git checkout master_ (goes back in time you will see all commits)
  
### Revert
    * _git revert <commit ID> (revert changes)
	* reverting revert
		* _git checkout master
		* _git revert <comit ID>
  ![revert](https://user-images.githubusercontent.com/43897511/50929735-a23f9e80-1423-11e9-862a-f1278fe10f24.PNG)
  
### Reset
	* Reset goes all the way back in time and stays there , once done there's no going back
    * reset works in 3 different stages 
		* soft(only goes back in time in the commit tree, sort of checkout ), 
		* mixed and 
		* hard(going back in time in the working directory and stays there)
		
    * _git resert --hard <commitID>
  ![hard reset](https://user-images.githubusercontent.com/43897511/50929952-3c074b80-1424-11e9-8240-2e06e01a1f92.PNG)
  
### Git ignore 
	* files which you do not want to track eg: auto-build files
    * create a gitignore file 
		* _touch .gitignore
    * A file is created in the folder with no name 
    * Open it and add the name of the file which you do not want to track
  ![badfile](https://user-images.githubusercontent.com/43897511/50930461-af5d8d00-1425-11e9-8e3a-e71a129deadd.PNG)
    * By checking the git status , we see we have the .gitignore in the untracked files
  ![aftergitignore](https://user-images.githubusercontent.com/43897511/50930480-be443f80-1425-11e9-8ec9-8df5f719c909.PNG)
  
##### HEAD is a reference to the last commit in the currently check-out branch.
##### You can have only one checked out commit at a time.

### Git Branches
    * A branch is a chain of commits that are on a separate timeline from the master, therefore, they do not have conflicting timelines.
    * Allows you to create separate development paths without overriding or creating copies of your project
    * Branches can be added, deleted and merged just like regular commits
    * creates separate branches for each stage of development (release , development,fixes,master)
    * You have to make an initial commit before creating branches , else your development brach will be considered your master branch
		* creating branch
  ![branch](https://user-images.githubusercontent.com/43897511/50932246-9c00f080-142a-11e9-8b60-1734f20083e7.PNG)
		*creates and checkouts a new branch
  ![branch1](https://user-images.githubusercontent.com/43897511/50932248-9e634a80-142a-11e9-9d61-2b1ebdcb1eb0.PNG)
		* Lists all branch
  ![listall branch](https://user-images.githubusercontent.com/43897511/50932273-b4710b00-142a-11e9-922c-c3c6cbe9bc8a.PNG)
		* Delete a branch
  ![deletebranch](https://user-images.githubusercontent.com/43897511/50932296-c3f05400-142a-11e9-94c1-337ae455958e.PNG)
	* _you cannot delete a branch in which you are currently.
	* merging only takes last commit of source branch
  
### Github 
  * An host for git
  * fork in github : A fork is a copy of a repository. It allows to freely experiment with changes.
  * clone in github : cloning helps to create a local repository on your computer from remote repository and sync between two locations.
  * forking a repository creates a copy of the repository under your Github ID . Any changes made will reflect only your forked repository . But if you want to make any changes to your forked repository you will have to explicitly create a pull request to original repository and once approved by admin , then only you can commit changes  or merge with the existing original repository.
  
### Creating remote repository github
     * create a repository in github
      ![new repo](https://user-images.githubusercontent.com/43897511/50949186-cffc0600-146a-11e9-9e17-ca7a561f2783.PNG)
     * copy the https link 
     ![https](https://user-images.githubusercontent.com/43897511/50949223-f621a600-146a-11e9-81c4-72f10c6363f9.PNG)
     * create a new directory 
     * initialize the new directory
     * connect remote repository
    	* _git remote add origin <https link>
      ![remoteconn](https://user-images.githubusercontent.com/43897511/50949237-09347600-146b-11e9-956d-08cae423e52c.PNG)
		* connected our repository
    
### Push, Pull ,fetch
    * fetch is pulling information from your repository
    * push information from our local repository to the host or shared server that we are using
    * pull remote repository to local repository
    * after modifying and committing the changes in the files we do a git push
    ![newpush](https://user-images.githubusercontent.com/43897511/50949275-28330800-146b-11e9-9c8e-02ff0ed98e24.PNG)
    * it asks for username and password of the github account
    * We can see changes on the github account after this
	
##### you can push only one branch at a time to a remote repository

### Working with Branches
    * creating a sample c++ file on github
    * Pull the same from github using terminal 
  ![pull sample file](https://user-images.githubusercontent.com/43897511/50953926-7ac7f080-147a-11e9-863d-1a2d867f29ee.PNG)
    * create a new branch then we will fix errors or do modification
    * Then add the same in staging area and commit
    ![branchadd](https://user-images.githubusercontent.com/43897511/50953956-916e4780-147a-11e9-919e-98cf0bc7781b.PNG)
    * Now we will merge the changes 
      * switch to master branch
      * merge the branch 
    ![merge](https://user-images.githubusercontent.com/43897511/50953972-a054fa00-147a-11e9-86d1-030a15546112.PNG)
      * you can check the history of changes using git log
     ![newgitlog](https://user-images.githubusercontent.com/43897511/50953999-b367ca00-147a-11e9-8773-af36033c5bf3.PNG)
      * also the changes are visible on github repository
     ![githubseechange](https://user-images.githubusercontent.com/43897511/50954025-d3978900-147a-11e9-8d72-ae1f7d8981e9.PNG)
     ![twobranch](https://user-images.githubusercontent.com/43897511/50954038-e14d0e80-147a-11e9-8b3e-36d94cf0a06d.PNG)
    * Now we will delete the remote branch
      * git push origin --delete <branch name>
    ![deletebranch1](https://user-images.githubusercontent.com/43897511/50954054-f1fd8480-147a-11e9-862c-72f453b4831e.PNG)
  
 ### Using Git GUI
    * Github is a GIT GUI allowing you to interact with your repositories through a graphical interface.
    * github desktop is used as an altertnative to the terminal when using Git
    * download github desktop from [!link] https://desktop.github.com/
    * File -> Options -> Accounts -> sign in to your github account
   ![signin](https://user-images.githubusercontent.com/43897511/50954893-4dc90d00-147d-11e9-802d-9e25e86dcd8b.PNG)
    * Create a new repository
   ![gitgui1](https://user-images.githubusercontent.com/43897511/50954919-5cafbf80-147d-11e9-9277-08a74901f230.PNG)
    * created new files in the new repository
      * we would be able to see the new files in the changes tab
   ![zoom1](https://user-images.githubusercontent.com/43897511/50955185-1149e100-147e-11e9-8e90-db96615252f1.PNG)
    * you can do push, pull fetch , create branch all other things from here
    * to push the repository you can simply publish repository
    
