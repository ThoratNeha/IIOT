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
