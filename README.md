# git-102

# Introduction
This is a resource mainly targeting to provide over all and general aspects of the git. The topic covers downlaoding, installtion, and working environment of git, and its related commands that could let the user to work with a version management operation.

# What is Git? 
-	It is a platform that could let a certain resource to be distributee across different people takig their won versions.

# What is version control? 
-	It is refering the different content that a certain shared resource has over the course time. such version control is  useful to work in teamand release the different version of the shared resource whenever a new version merges to the old one.


# Installtion of git
git can be downlaoded from the following link  as per the kind of operating system you have

	* https://git-scm.com/downloads
	* Follow up the prompt

# Checking the version of git
git --version
it will show you the installed version of the git. Example : - git version 2.22.0

# Configuration of git
This is a step to perform a configuration of git. The configuration is actually made providing the following information
	git config --gloabl user.name "userName "
	git config --gloabl user.email "userEmail@domainName.com"

# Already installed git 
The following link will provide the latest developmen verison for the git itself. Run the following command on the terminal
git clone https://github.com/git/git. It willautomatically update the git.


# Begin using the git
In order to begin using the git, the first thing that we shoudl do is  creating a folder using the command mkdir <folderName>
	Example : - mkdir git-102
	
# Running the git
In order to initilize and run the git, oepn the folder you jsut created, and type on the terminal the following command
-	cd <folderName>
-	git init
	it will create an empty Git repository locally. The following message is displayed
			** "Initialized empty Git repository in /Users/<userName>/git-102/.git" ** 

Inorder to make the Git concept clear enough , we should create a sample projet. The sample project has two file of html and css. The name of the files are as follow.
**index.html 
**style.css

# git status 
It shows the status of the branch. The message from the **git status** will tell you about what changes have been made on the branch, and not yet commited or untracked. It puts the files in color red or green.
	**red  file**
		colored files are those not tracket.
		
# git add fileName
It is a command which will make the file to add to the respository. The applicaiton of the git add is as folloe
	**git add "<fileName>"**	
	Looking again  through a command **git status** will show the following message
	On branch master

	No commits yet

		Changes to be committed:
 			 (use "git rm --cached <file>..." to unstage)

		new file:   index.html


# git rm --cached "<fileName>"
This is a command which is useful to unstage the change alreay added to the fiel from the latest git add. this will make the content to be one verion less from the last added feature.
	git rm --cached 'index.html'
	looking back again the git status , it will show the following result  
	On branch master

	No commits yet
	Untracked files:
 		 (use "git add <file>..." to include in what will be committed)
		index.html
	nothing added to commit but untracked files present (use "git add" to track)
	

# git commit -m "message use a title of commit "
This is a command used to commit the chnage already added to the local repository. The applciaiton of the command is as follow
	**git commit -m "commit messge"**
		git commit -m "Add header"
 		1 file changed, 10 insertions(+)
 		create mode 100644 index.html
	
	looking back again the status git master, it will show a message as follow
		git status
		On branch master
		nothing to commit, working tree clean
	
# git diff master branchName
This is a command used to show the differences among the chnages made in the documents. the changes are laneeld with two color one with red and green. The red color is actually used to indicate thosconsidred to changed, and gree are considered as changes done.

	git diff index.html 
	diff --git a/index.html b/index.html
	index 628f4e7..1164244 100644
	--- a/index.html
	+++ b/index.html
	@@ -10,8 +10,8 @@
     	<ul>
        	 <li>Right</li>
        	 <li>Left</li>
	-        <li>Top</li>
	-        <li>Bottom</li>
	+        <li>Top_Right</li>
	+        <li>Bottom_Right</li>
     	</ul>
 	</body>
 	</html>
# git checkout -- fileName
This is a command used to reject or discard the changes happened to the documents. This will return the document status to the last poistion status before the changes happened. The applciation of the command is follow
	git checkout -- index.html

# git log 
This is a commmand that could show a lost of commit made during the course of actions stating the author , the Date as well as the comments written along wi th the commit. The applicaiton of the command will as as follow
	git log
	commit d48403d3dd4fd3185043e7a89602ba12afdc2919 (HEAD -> master)
	Author: userName <user_emal@domain.com>
	Date:   Tue Sep 10 18:46:44 2019 +0200

    adding a lists
	commit 60765664be7b46cc6ea7831cddc670aca16a1b10
	Author: userName <user_emal@domain.com>
	Date:   Tue Sep 10 18:03:52 2019 +0200
    color & font weight
	commit 773db17ceb3c9574e1ab25926b7ca6bc13dea374
	Author: userName <user_emal@domain.com>
	Date:   Tue Sep 10 16:53:13 2019 +0200

    Add header
    
# git lg
This is also another command that could demonstrate all the commit including the commit message, date, author as part of each commit. The application of the commands are as follow
	**command
		git lg
	**Outcome
		* d48403d - (HEAD -> master) adding a lists (2 minutes ago) <userName>
		* 6076566 - color & font weight (45 minutes ago) <userName>
		* 773db17 - Add header (2 hours ago) <userName>

# What is Branching?

This is a feature supported in git and has a role of creating inline path along with the master. The inline path helps developers to do their work separatly and contribue their work to the master environment inorder to merge it.

# Creating Branch - git branch branchName
In order to create a branch, there is a command 
	**command
		git branch "branch_name"

# Listing out branching - git branch
This is a command used to list out all the created branches along with the master branch.
	**commands
		git branch
	**outcomee
		branch-01-add-log
		* master

# checking out branch - git checkout branchName
This is a command used to checkout to the branch that the dev's created to do its parts. The command is applied as follow
	**command
		git checkout branchName
		
# Creating and checking out branch - git checkout -b branchName
This is a command used to create at the same time checking out. The command is applied as follow
	git checkout -b branchName

# Adding and Committing changes
The same command is used to add as well as commit the change at local branch of the dev.
	**git add "fileName"
	**git commit -m "commit_message"

# Checking out master - git checkout master
This is also the same command of checking out to any branch. The applicaiton of the command is as follow
	**command
	git checkout master
	
# Looking the difference Master Verse Local branch
This is a command used to check the difference between the branch committed verse the master branch
	**command
	git diff master branchName

	git diff master branch-01-add-log
		diff --git a/index.html b/index.html
		index 628f4e7..b4a6ae0 100644
		--- a/index.html
		+++ b/index.html
		@@ -10,8 +10,8 @@
     <ul>
       	 	<li>Right</li>
        	 <li>Left</li>
	-        <li>Top</li>
	-        <li>Bottom</li>
	+        <li>Top-On</li>
	+        <li>Bottom-Down</li>
     </ul>
 </body>
 </html>
 	**Note , The - sign is refering those to be changes and The + are those to be added(changes made).
	
# Mergging the changes to the master
This is a command used to merge the changes after seeing the difference. The command will be applied as follow
	**command
		git checkout master
		git merger --no-ff branchName

# Deleting a branch - git branch -d branchName
This is a command which has a purpose of deleting a branch. The developer ussually delete the branch that develped his work after the merge to the master branch. In order to delete the branch, the following command is used
	**command
		git branach -d branchName
		git branch -D branchName //Alternatively, This is applied in the case the branch is not fully merged.
		
# Waht is Remote 
This is actuall a cloud place where different developers share their work and contribute together to accomplishe a certain development or application. The first step to create a remote is to go to git and create a respository.

# Checking a remote repository - git remove -v
This is a command used to check that whether i have a remote repository or not.
	**command
		git remote -v
	if there are remote repository already configured, a list of possible repository will be listed out as follow
		origin	https://github.com/gitdegu/git-102.git (fetch)
		origin	https://github.com/gitdegu/git-102.git (push)
		
# Creating a remote repository
	Under a git reposotories section, Click the New button and provide the name of the repository.
	1. Click on Create Repository
	2. The following commands are useful to create a remote repository
	3. git remote add origin https://github.com/gitdegu/-git-102_.git
	4. applying the above command will show you the expected outcome "git remote -v"
		origin	https://github.com/gitdegu/git-102.git (fetch)
		origin	https://github.com/gitdegu/git-102.git (push)
	
# Remove remote respository - git remote rm origin
This is a sommand used to remove a remote repository.  The command is going to excusted as follow
	**git remote rm origin 
	
# Pushing to a remote repository - git push -u origin master
This is a command used to push a local master committed change to a remote master. the following are the outcome obtained after running the **git push -u origin master**
	
		Enumerating objects: 43, done.
		Counting objects: 100% (43/43), done.
		Delta compression using up to 4 threads
		Compressing objects: 100% (41/41), done.
		Writing objects: 100% (43/43), 10.17 KiB | 1.69 MiB/s, done.
		Total 43 (delta 12), reused 0 (delta 0)
		remote: Resolving deltas: 100% (12/12), done.
		To https://github.com/gitdegu/git-102.git
		 * [new branch]      master -> master
		Branch 'master' set up to track remote branch 'master' from 'origin'.

# git pull
This is a command used to get the latest code from the remote branch. This could give a chance locally ro  resolve any changes or conflict . The **git pull** has the following results

	Merge made by the 'recursive' strategy.
 	README.md | 248 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
 	1 file changed, 248 insertions(+)
 	create mode 100644 README.md
	
**Note** 
 Remember that change in local master need to pull the chanes from remote master repository before publishing anything. 
 Any working branches from a local directory needs to have adjust itself from the local master to have the same status.

	
# git diff origin/master
	This is a command used to compare the local master with the remote master branch. 
	The changes are colored as red and green light to let us what has been removed and added locally comapre to the remote master.

