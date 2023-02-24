# Git-Tutorials

Here, We will be learning about how to use Git and many other things like.

1. How to install Git.

2. How to setup Git and Sign Up and SingIn

3. How to create a project or repository in Git

4. How to create a branch in a repository.

5. How to check your repository, branch and sub-branch.

6. How to re-initialize repository with another repository.

7. How to merge push and pull your code (project) in GIT.

8. many more things we will be learning in it... as you are able to see in left sidebar, your tutorials continues....

### Table of contents

- [Chapter 1 - How to download or install Git](#chapter1)
- [Chapter 2 - How to setup Git and Sign Up and SingIn](#chapter2)
- [Chapter 3 - How to create a project or repository in Git](#chapter3)
- [Chapter 4 - How to create a branch in a repository.](#chapter4)
- [Chapter 5 - How to check your repository, branch and sub-branch.](#chapter5)
- [Chapter 6 - How to re-initialize repository with another repository.](#chapter6)
- [Chapter 7 - How to merge push and pull your code (project) in GIT.](#chapter7)
- [Chapter 8 - many more things we will be learning in it... as you are able to see in left sidebar, your tutorials continues](#chapter8)
 

<a name="chapter1">
<h1>Chapter 1 -  How to download or install Git</h1>
</a>
 Download Git for Windows

Step 1: Goto the official Git website: https://git-scm.com/downloads

Step 2: Click the download link for Windows and allow the download to complete.

Step 3: After downloading the file successfully, goto its location and extract the File & now you will see the Git file (Installer). Double click on it and start the installation & complete as per your need.

Step 4: Now your Git is installed successfully. Press your Windows Key button and search Git Bash and check the git is installed or not on your machine.

Step 5: Check your Git Version: 
 ```
$   git --version

```
Step 6: Now you configure your git credentials to get started with your github or gitlab or bitbucket etc..



Short Cuts: (Git Cheat Sheet) -

1. Get all the branches : 
  ```
$   git fetch -all

```
2. Check in which branch you are and how many branches are there :
  ```
$   git branch

$   git branch -alll

```
3. Check to Current Branch : $ git branch --show-current
 ```
$   git branch -show-current

```
4. Check your current repository name :
```
$   git remote -v
```


5. Check your current repository full detailed status (Username & password will be asked):
```
$   git remote show origin
```


6. How to add Git or Re-initialise Git :
```
$   git init
```


7. If you want to change the repository from one to another :
```
$   git remote add origin your_repo_path
```
eg: https://gitlab.com/your-repository.git



8. Create a branch :
```
$   git checkout -b <name-of-branch>
```


9. Switching from ONE Branch to ANOTHER branch
```
$   git checkout <name-of-branch>
```
eg: $ git checkout master



10. Push Changes of files to your Git Repository:
```
$   git add .
 
$   git commit -m "First Commit"

$   git push origin <master> or <your_branch_name>
```


11. Create a branch in your repository and pushing to Git:
```
$   git checkout -b <name-of-branch>

$   git add .

$   git commit -m "First Commit"

$   git push origin <master> or <your_branch_name>
```
   

12. How to Clone a Git Repository -

Via HTTPS:
```
$   git clone https://gitlab.com/gitlabtest/sample-project.git
```
Via SSH: 
```
$   git clone git@gitlab.com:gitlab-test/sample-project.git
```


13. How to Clone a Git Branch
```
$   git clone -b <branch_name> <remote_repo>
```


14. How to Remove or Delete Branch from your repository
```
$   git push origin -delete <master>  or <your_branch_name>
```
