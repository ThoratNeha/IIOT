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

![image](https://user-images.githubusercontent.com/105771251/209518783-10971fb6-cbef-433d-a010-d7e9b511f4bb.png)<br>
#### Git Flow / Git Branching Model
Git flow is the set of guidelines that developers can follow when using Git. We cannot say these guidelines as rules. These are not the rules; it is a standard for an ideal project. So that a developer would easily understand the things.

It is referred to as Branching Model by the developers and works as a central repository for a project. Developers work and push their work to different branches of the main repository.

![image](https://user-images.githubusercontent.com/105771251/209536597-ba925ce2-2e99-4805-b0ec-b460e3835b2b.png)

There are different types of branches in a project. According to the standard branching strategy and release management, there can be following types of branches:

#### Master
#### Develop
#### Hotfixes
#### Release branches
#### Feature branches

Every branch has its meaning and standard. Let's understand each branch and its usage.

#### The Main Branches

Two of the branching model's branches are considered as main branches of the project. These branches are as follows:

#### master
#### develop

![image](https://user-images.githubusercontent.com/105771251/209536753-05656a55-e426-415e-8dc4-b06a24117f2a.png)

#### Master Branch
The master branch is the main branch of the project that contains all the history of final changes. Every developer must be used to the master branch. The master branch contains the source code of HEAD that always reflects a final version of the project.

Your local repository has its master branch that always up to date with the master of a remote repository.

It is suggested not to mess with the master. If you edited the master branch of a group project, your changes would affect everyone else, and very quickly, there will be merge conflicts.

#### Develop Branch
It is parallel to the master branch. It is also considered as the main branch of the project. This branch contains the latest delivered development changes for the next release. It has the final source code for the release. It is also called as a "integration branch."

When the develop branch reaches a stable point and is ready to release, it should be merged with master and tagged with a release version.

#### Supportive Branches
The development model needs a variety of supporting branches for the parallel development, tracking of features, assist in quick fixing and release, and other problems. These branches have a limited lifetime and are removed after the uses.

The different types of supportive branches, we may use are as follows:
#### Feature branches
#### Release branches
#### Hotfix branches

Each of these branches is made for a specific purpose and have some merge targets. These branches are significant for a technical perspective.

#### Feature Branches
Feature branches can be considered as topic branches. It is used to develop a new feature for the next version of the project. The existence of this branch is limited; it is deleted after its feature has been merged with develop branch.

![image](https://user-images.githubusercontent.com/105771251/209537032-3a3f4322-8c00-4ea5-9c5f-40a695bdc959.png)

#### Release Branches
The release branch is created for the support of a new version release. Senior developers will create a release branch. The release branch will contain the predetermined amount of the feature branch. The release branch should be deployed to a staging server for testing.

Developers are allowed for minor bug fixing and preparing meta-data for a release on this branch. After all these tasks, it can be merged with the develop branch.
When all the targeted features are created, then it can be merged with the develop branch. Some usual standard of the release branch are as follows:

Generally, senior developers will create a release branch.
The release branch will contain the predetermined amount of the feature branch.
The release branch should be deployed to a staging server for testing.
Any bugs that need to be improved must be addressed at the release branch.
The release branch must have to be merged back into developing as well as the master branch.
After merging, the release branch with the develop branch must be tagged with a version number.

#### Hotfix Branches
Hotfix branches are similar to Release branches; both are created for a new production release.

The hotfix branches arise due to immediate action on the project. In case of a critical bug in a production version, a hotfix branch may branch off in your project. After fixing the bug, this branch can be merged with the master branch with a tag.

![image](https://user-images.githubusercontent.com/105771251/209537213-90cc3625-b59f-4827-a0c9-cec47c9ada08.png)

## Git Cheat Sheet

## 1) Git configuration
#### Git config
Get and set configuration variables that control all facets of how Git looks and operates.
#### Set the name:
$ git config --global user.name "User name"
#### Set the email:
$ git config --global user.email "himanshudubey481@gmail.com"
#### Set the default editor:
$ git config --global core.editor Vim
#### Check the setting:
$ git config -list

#### Git alias
Set up an alias for each command:
$ git config --global alias.co checkout
$ git config --global alias.br branch
$ git config --global alias.ci commit
$ git config --global alias.st status

## 2) Starting a project
#### Git init
#### Create a local repository:
$ git init
#### Git clone
Make a local copy of the server repository.
$ git clone

## 3) Local Changes
### Git add
#### Add a file to staging (Index) area:
$ git add Filename
#### Add all files of a repo to staging (Index) area:
$ git add*

### Git commit
Record or snapshots the file permanently in the version history with a message.
$ git commit -m " Commit Message"

## 4) Ignoring Files

### .gitignore
Specify intentionally untracked files that Git should ignore. Create .gitignore:
$ touch .gitignore List the ignored files:
$ git ls-files -i --exclude-standard

## Remote
### Git remote
#### Check the configuration of the remote server:
$ git remote -v
#### Add a remote for the repository:
#### $ git remote add Fetch the data from the remote server:
$ git fetch
#### Remove a remote connection from the repository:
$ git remote rm
#### Rename remote server:
$ git remote rename
#### Show additional information about a particular remote:
$ git remote show
#### Change remote:
$ git remote set-url
### Git origin master
#### Push data to the remote server:
$ git push origin master Pull data from remote server:
$ git pull origin master

## Git Fork

A fork is a rough copy of a repository. Forking a repository allows you to freely test and debug with changes without affecting the original project. One of the excessive use of forking is to propose changes for bug fixing. To resolve an issue for a bug that you found, you can:

##### Fork the repository.
##### Make the fix.
##### Forward a pull request to the project owner.
##### Forking is not a Git function; it is a feature of Git service like GitHub.

#### When to Use Git Fork

Generally, forking a repository allows us to experiment on the project without affecting the original project. Following are the reasons for forking the repository:

i)  Propose changes to someone else's project.
ii) Use an existing project as a starting point.

##### Let's understand how to fork a repository on GitHub?

### How to Fork a Repository?

The forking and branching are excellent ways to contribute to an open-source project. These two features of Git allows the enhanced collaboration on the projects.

Forking is a safe way to contribute. It allows us to make a rough copy of the project. We can freely experiment on the project. After the final version of the project, we can create a pull request for merging.

It is a straight-forward process. Steps for forking the repository are as follows:

i) Login to the GitHub account.
ii) Find the GitHub repository which you want to fork.
iii) Click the Fork button on the upper right side of the repository's page.

We can't fork our own repository. Only shared repositories can be fork. If someone wants to fork the repository, then he must log in with his account. Let's understand the below scenario in which a user pune2016 wants to contribute to our project GitExample2. When he searches or put the address of our repository, our repository will look like as follows:

![image](https://user-images.githubusercontent.com/105771251/209540718-2e165dac-286e-46a4-abf5-06ddc0bbf1ab.png)

The above image shows the user interface of my repository from other contributors. We can see the fork option at the top right corner of the repository page. By clicking on that, the forking process will start. It will take a while to make a copy of the project for other users. After the forking completed, a copy of the repository will be copied to your GitHub account. It will not affect the original repository. We can freely make changes and then create a pull request for the main project. The owner of the project will see your suggestion and decide whether he wants to merge the changes or not. The fork copy will look like as follows:

![image](https://user-images.githubusercontent.com/105771251/209540740-4076f67b-a491-44dd-b18e-7020ccd43292.png)

As you can see, the forked repository looks like pune2016/GitExample2. At the bottom of the repository name, we can see a description of the repository. At the top right corner, the option fork is increased by 1 number.
Hence one can fork the repository from GitHub.

### Fork vs. Clone
Sometimes people considered the fork as clone command because of their property. Both commands are used to create another copy of the repository. But the significant difference is that the fork is used to create a server-side copy, and clone is used to create a local copy of the repository.

There is no particular command for forking the repository; instead, it is a service provided by third-party Git service like GitHub. Comparatively, git clone is a command-line utility that is used to create a local copy of the project.

Generally, people working on the same project clone the repository and the external contributors fork the repository.

A pull request can merge the changes made on the fork repository. We can create a pull request to propose changes to the project. Comparatively, changes made on the cloned repository can be merged by pushing. We can push the changes to our remote repository.

## Git Fetch
Git "fetch" Downloads commits, objects and refs from another repository. It fetches branches and tags from one or more repositories. It holds repositories along with the objects that are necessary to complete their histories to keep updated remote-tracking branches.

![image](https://user-images.githubusercontent.com/105771251/209540919-fee37c62-47a9-4323-b060-1dd3d7b2cadd.png)

### The "git fetch"command
The "git fetch" command is used to pull the updates from remote-tracking branches. Additionally, we can get the updates that have been pushed to our remote branches to our local machines. As we know, a branch is a variation of our repositories main code, so the remote-tracking branches are branches that have been set up to pull and push from remote repository.

### How to fetch Git Repository
We can use fetch command with many arguments for a particular data fetch. See the below scenarios to understand the uses of fetch command.

### Scenario 1: To fetch the remote repository:
We can fetch the complete repository with the help of fetch command from a repository URL like a pull command does. See the below output:

#### Syntax:
```
$ git fetch< repository Url> 
```

#### Output:

![image](https://user-images.githubusercontent.com/105771251/209541070-ca7e989f-6171-49d9-9da7-29cc79a74ce5.png)
In the above output, the complete repository has fetched from a remote URL.

### Scenario 2: To fetch a specific branch:
We can fetch a specific branch from a repository. It will only access the element from a specific branch. See the below output:

#### Syntax:
```
$ git fetch <branch URL><branch name> 
```
#### Output:
![image](https://user-images.githubusercontent.com/105771251/209541179-1ed5d4de-18e1-4947-bef0-6eed58a3077a.png)

In the given output, the specific branch test has fetched from a remote URL.

### Scenario 3: To fetch all the branches simultaneously:
The git fetch command allows to fetch all branches simultaneously from a remote repository. See the below example:

#### Syntax:
```
$ git fetch -all > 
```

#### Output:
![image](https://user-images.githubusercontent.com/105771251/209541288-01d3adb2-7f10-4d92-8533-8b4f531bc1ce.png)

In the above output, all the branches have fetched from the repository Git-Example.

### Scenario 4: To synchronize the local repository:
Suppose, your team member has added some new features to your remote repository. So, to add these updates to your local repository, use the git fetch command. It is used as follows.

#### Syntax:
```
$ git fetch origin  
```
#### Output:
![image](https://user-images.githubusercontent.com/105771251/209541402-8db29d0d-d167-4353-a74d-b47583f917a2.png)

In the above output, new features of the remote repository have updated to my local system. In this output, the branch test2 and its objects are added to the local repository.

The git fetch can fetch from either a single named repository or URL or from several repositories at once. It can be considered as the safe version of the git pull commands.

The git fetch downloads the remote content but not update your local repo's working state. When no remote server is specified, by default, it will fetch the origin remote.

### Differences between git fetch and git pull
To understand the differences between fetch and pull, let's know the similarities between both of these commands. Both commands are used to download the data from a remote repository. But both of these commands work differently. Like when you do a git pull, it gets all the changes from the remote or central repository and makes it available to your corresponding branch in your local repository. When you do a git fetch, it fetches all the changes from the remote repository and stores it in a separate branch in your local repository. You can reflect those changes in your corresponding branches by merging.

So basically,

#### Syntax:
```
git pull = git fetch + git merge  
```

## Git Pull / Pull Request
The term pull is used to receive data from GitHub. It fetches and merges changes from the remote server to your working directory. The git pull command is used to pull a repository.
![image](https://user-images.githubusercontent.com/105771251/209542656-aba94bd5-5471-4a97-8c61-55dd2b828aad.png)

Pull request is a process for a developer to notify team members that they have completed a feature. Once their feature branch is ready, the developer files a pull request via their remote server account. Pull request announces all the team members that they need to review the code and merge it into the master branch.

The below figure demonstrates how pull acts between different locations and how it is similar or dissimilar to other related commands.

![image](https://user-images.githubusercontent.com/105771251/209542678-f56bd66a-f898-4554-954e-cc13c9ced4cf.png)

### The "git pull" command

The pull command is used to access the changes (commits)from a remote repository to the local repository. It updates the local branches with the remote-tracking branches. Remote tracking branches are branches that have been set up to push and pull from the remote repository. Generally, it is a collection of the fetch and merges command. First, it fetches the changes from remote and combined them with the local repository.

#### The syntax of the git pull command is given below:

#### Syntax:
```
$ git pull <option> [<repository URL><refspec>...]   
```

### How to use pull:

It is essential to understand how it works and how to use it. Let's take an example to understand how it works and how to use it. Suppose I have added a new file say design2.css in my remote repository of project GitExample2.

To create the file first, go to create a file option given on repository sub-functions. After that, select the file name and edit the file as you want. Consider the below image.
![image](https://user-images.githubusercontent.com/105771251/209543390-33d5c34a-9db0-4404-a7b3-2175eb58d2df.png)

Go to the bottom of the page, select a commit message and description of the file. Select whether you want to create a new branch or commit it directly in the master branch. Consider the below image:
![image](https://user-images.githubusercontent.com/105771251/209543408-068d647e-4d77-4d1a-8345-0d27983d9ba4.png)
Now, we have successfully committed the changes.

To pull these changes in your local repository, perform the git pull operation on your cloned repository. There are many specific options available for pull command. Let's have a look at some of its usage.

### Default git pull:
We can pull a remote repository by just using the git pull command. It's a default option. Syntax of git pull is given below:
#### Syntax:
```
$ git pull  
```

#### Output
![image](https://user-images.githubusercontent.com/105771251/209543531-6e4c990b-6e05-4820-88da-e60c50b00e9d.png)

In the given output, the newly updated objects of the repository are fetched through the git pull command. It is the default version of the git pull command. It will update the newly created file design2.css file and related object in the local repository. See the below image.
![image](https://user-images.githubusercontent.com/105771251/209543554-256c989a-744e-4f06-b04a-ab3b9ff79fae.png)
As you can see in the above output, the design2.css file is added to the local repository. The git pull command is equivalent to git fetch origin head and git merge head. The head is referred to as the ref of the current branch.

### Git Pull Remote Branch
Git allows fetching a particular branch. Fetching a remote branch is a similar process, as mentioned above, in git pull command. The only difference is we have to copy the URL of the particular branch we want to pull. To do so, we will select a specific branch. See the below image:
![image](https://user-images.githubusercontent.com/105771251/209543591-2967e2e1-c2f8-48c0-acae-44413688f43f.png)

In the above screenshot, I have chosen my branch named edited to copy the URL of the edited branch. Now, I am going to pull the data from the edited branch. Below command is used to pull a remote branch:

#### Syntax:
```
$ git pull <remote branch URL>   
```

#### Output:
![image](https://user-images.githubusercontent.com/105771251/209544054-8fda6332-914c-44cc-a453-b4b85d63439c.png)

### Git Force Pull

Git force pull allows for pulling your repository at any cost. Suppose the below scenario:

If you have updated any file locally and other team members updated it on the remote. So, when will you fetch the repository, it may create a conflict.

We can say force pull is used for overwriting the files. If we want to discard all the changes in the local repository, then we can overwrite it by influentially pulling it. Consider the below process to force pull a repository:

Step1: Use the git fetch command to download the latest updates from the remote without merging or rebasing.
#### Syntax:
```
$ git fetch -all 
```

Step2: Use the git reset command to reset the master branch with updates that you fetched from remote. The hard option is used to forcefully change all the files in the local repository with a remote repository.

#### Syntax:
```
$ git reset -hard <remote>/<branch_name>
$ git reset-hard master  

```
#### Consider the below output:
![image](https://user-images.githubusercontent.com/105771251/209544369-de294294-65fd-463e-9745-ec087dad3ab5.png)
It will overwrite the existing data of the local repository with a remote repository.

You can check the remote location of your repository. To check the remote location of the repository, use the below command:

#### Syntax:
```
$ git remote -v  
```

The given command will result in a remote location like this:
#### Syntax:
```
origin  https://github.com/ImDwivedi1/GitExample2 (fetch)  
origin  https://github.com/ImDwivedi1/GitExample2 (push)   
```

#### Output:
![image](https://user-images.githubusercontent.com/105771251/209544521-7a0f5dae-2a98-47f5-b4b0-ea0c700351c1.png)

### Git Pull Request
Pull request allows you to announce a change made by you in the branch. Once a pull request is opened, you are allowed to converse and review the changes made by others. It allows reviewing commits before merging into the main branch.

Pull request is created when you committed a change in the GitHub project, and you want it to be reviewed by other members. You can commit the changes into a new branch or an existing branch.

Once you've created a pull request, you can push commits from your branch to add them to your existing pull request.

### How to Create a Pull Request
To create a pull request, you need to create a file and commit it as a new branch. As we mentioned earlier in this topic, how to commit a file to use git pull. Select the option "create a new branch for this commit and start a pull request" from the bottom of the page. Give the name of the new branch. Select the option to propose a new file at the bottom of the page. Consider the below image.
![image](https://user-images.githubusercontent.com/105771251/209544579-3c1bda8c-32a4-4cd9-bd93-d2ddec27227d.png)

In the above image, I have selected the required option and named the file as PullRequestDemo. Select the option to propose a new file. It will open a new page. Select the option create pull request. Consider the below image:

![image](https://user-images.githubusercontent.com/105771251/209544601-60c0382c-afb7-412b-baf9-195c2e61e849.png)

Now, the pull request is created by you. People can see this request. They can merge this request with the other branches by selecting a merged pull request.



