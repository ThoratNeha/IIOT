# Git
## Introduction
Git is a popular version control system. It was created by Linus Torvalds in 2005, and has been maintained by Junio Hamano since then. It is used for: Tracking code changes. Tracking who made changes.
Git  is a distributed version control system: tracking changes in any set of files, usually used for coordinating work among programmers collaboratively developing source code during software development.
### Important Git commands:
#### 1) Git config command:
This command configures the user. The Git config command is the first and necessary command used on the Git command line. This command sets the author name and email address to be used with your commits. Git config is also used in other scenarios.
#### Syntax
```
$ git config --global user.name "username"  
$ git config --global user.email "Email Id"  
```
#### 2) Git Init command
This command is used to create a local repository.

#### Syntax
```
$ git init Demo  
```
The init command will initialize an empty repository. See the below screenshot.<br>
![Screenshot (42)](https://user-images.githubusercontent.com/112370237/209502447-ba05ad4e-6f3d-496e-ad5d-dd86519913b2.png)<br>
#### 3) Git clone command
This command is used to make a copy of a repository from an existing URL. If I want a local copy of my repository from GitHub, this command allows creating a local copy of that repository on your local directory from the repository URL.

#### Syntax
```
$ git clone URL  
```
![Screenshot (44)](https://user-images.githubusercontent.com/112370237/209505476-dbf4ca9b-d556-43e3-9dbf-2d5e27897280.png)
#### 4) Git add command
This command is used to add one or more files to staging (Index) area.
#### Syntax

To add one file
```
$ git add Filename  
```
To add more than one file
```
$ git add*
```
![Screenshot (45)](https://user-images.githubusercontent.com/112370237/209506319-62657a42-faee-4288-baf7-acd4d04380d5.png)<br>

#### 5) Git commit command
Commit command is used in two scenarios. They are as follows.
***Git commit -m***


This command changes the head. It records or snapshots the file permanently in the version history with a message.

#### Syntax
```
$ git commit -m " Commit Message"  
```
***Git commit -a***

This command commits any files added in the repository with git add and also commits any files you've changed since then.

#### Syntax
```
$ git commit -a  
```
![image](https://user-images.githubusercontent.com/105771251/209516461-c8ec47bc-ae79-4864-b9b0-8b1afd59e69b.png)

#### 6) Git Status Command
The status command is used to display the state of the working directory and the staging area. It allows you to see which changes have been staged, which haven't, and which files aren?t being tracked by Git. It does not show you any information about the committed project history. For this, you need to use the git log. It also lists the files that you've changed and those you still need to add or commit.

#### Syntax
```
$ git status  
```

![image](https://user-images.githubusercontent.com/105771251/209516718-5a84aba2-357f-4583-bfbc-628f21f6f76e.png)

#### 7) Git push Command
It is used to upload local repository content to a remote repository. Pushing is an act of transfer commits from your local repository to a remote repo. It's the complement to git fetch, but whereas fetching imports commits to local branches on comparatively pushing exports commits to remote branches. Remote branches are configured by using the git remote command. Pushing is capable of overwriting changes, and caution should be taken when pushing.

Git push command can be used as follows.

#### Git push origin master

This command sends the changes made on the master branch, to your remote repository.

#### Syntax
```
$ git push [variable name] master  
```
![image](https://user-images.githubusercontent.com/105771251/209517654-7be46930-478e-4c92-9204-b728160c0c58.png)

![image](https://user-images.githubusercontent.com/105771251/209517681-2aec7f3b-3fa1-4db4-9799-101dab3b70fa.png)

![image](https://user-images.githubusercontent.com/105771251/209517696-934d90e1-4d4f-4474-9a57-247ade50f3b0.png)

![image](https://user-images.githubusercontent.com/105771251/209517718-ba2945fa-2d1a-48e2-b03f-1bb968fe76f5.png)

#### Git push -all

This command pushes all the branches to the server repository.

#### Syntax
```
$ git push --all  
```

![image](https://user-images.githubusercontent.com/105771251/209517907-c25de025-5c5e-4951-834f-373bd9f89495.png)


#### 8) Git Pull Command
Pull command is used to receive data from GitHub. It fetches and merges changes on the remote server to your working directory.

#### Syntax
```
$ git push URL  
```
![image](https://user-images.githubusercontent.com/105771251/209518314-08f4dbc4-2b64-4d72-a8a1-ae70314da6fb.png)

#### 9) Git Branch Command
This command lists all the branches available in the repository.

#### Syntax
```
$ git branch  
```
![image](https://user-images.githubusercontent.com/105771251/209518415-6a0fd9bf-943d-48d4-910c-9247abd2e601.png)

#### 10) Git Merge Command
This command is used to merge the specified branch?s history into the current branch.

#### Syntax
```
$ git merge BranchName  
```
![image](https://user-images.githubusercontent.com/105771251/209518537-d14d3da9-a6f1-4fdf-9b95-6a6cc00ec121.png)

#### 11) Git log Command
This command is used to check the commit history.

#### Syntax
```
$ git log  
```
![image](https://user-images.githubusercontent.com/105771251/209518644-1fa43148-2a6e-4495-b750-a541231467eb.png)

By default, if no argument passed, Git log shows the most recent commits first. We can limit the number of log entries displayed by passing a number as an option, such as -3 to show only the last three entries.
```
$ git log -3
```

#### 12) Git remote Command
Git Remote command is used to connect your local repository to the remote server. This command allows you to create, view, and delete connections to other repositories. These connections are more like bookmarks rather than direct links into other repositories. This command doesn't provide real-time access to repositories.

![image](https://user-images.githubusercontent.com/105771251/209518783-10971fb6-cbef-433d-a010-d7e9b511f4bb.png)

