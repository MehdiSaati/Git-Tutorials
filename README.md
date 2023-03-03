# Git-Tutorials

Here, We will be learning about how to use Git and many other things like.


### Table of contents

- [Chapter 1 - How to download or install Git](#chapter1)
- [Chapter 2 - How to get the current branch name in Git ?](#chapter2)
- [Chapter 3 - How to create git repository in local and connect to Github, Gitlab, Bitbucket project.](#chapter3)
- [Chapter 4 - How to create a branch in a repository.](#chapter4)
- [Chapter 5 - How to remove or delete branch from git repository using command line](#chapter5)
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

---
<a name="chapter2">
<h1>Chapter 2 -  How to get the current branch name in Git ?</h1>
</a>

In this post, we will be learning how to determine or get the name of the current branch in Git.

So, there are several ways to get the name of the current branch in Git:

Method 1: git branch with no arguments displays the Current branch marked with an asterisk (*) in front of it:

Command: 
```
$ git branch
```
after typing the above command you will get the following result:
```
HP@HP-PC MINGW64 /c/xampp/htdocs/project
$ git branch
* your_branch_name
```
Method 2: We will show the current branch name directly without any argument by using the following command:

Command:
```
$ git branch --show-current
```
after typing the above command you will get the following result:

HP@HP-PC MINGW64 /c/xampp/htdocs/project
```
$ git branch --show-current
  your_branch_name
```

Method 3: this is another method of showing that how to find which git branch I am on, so you will get directly the branch name using the following command:

Command: ( Git 2.22 and above )
```
$ git name-rev --name-only HEAD
```
after typing the above command you will get the following result:

HP@HP-PC MINGW64 /c/xampp/htdocs/project
```
$ git name-rev --name-only HEAD
  your_branch_name
```

Method 4: how to see what branch you are on.! so you will get your branch name by the following command:
```
$ git rev-parse --abbrev-ref HEAD
```
after typing the above command you will get the following result:
```
HP@HP-PC MINGW64 /c/xampp/htdocs/project
$ git rev-parse --abbrev-ref HEAD
  your_branch_name
```
---

<a name="chapter3">
<h1>Chapter 3 -  How to create git repository in local and connect to Github, Gitlab, Bitbucket project.</h1>
</a>


How to create git repository in local and connect to Github, Gitlab, Bitbucket project.


In this post, we will be learning about how to create a git repository in localhost and connect to gitlab, github project.

Step 1: Let's create a git repository by following command:
```
$ git init
```

Step 2: Let's add our localhost project file into the this git initialized by following command:
```
$ git add .
```
this above git add . command, which has a dot at last (git add .) where this dot - (.) means all files to added into git init repo.

Step 3: After successfully adding files into git repo, now lets commit the file git commit with the message -m.
```
$ git commit -m "First Commit"
```

Step 4: Now, you have no repository to store or push your local git repository, so go to your Gitlab and create a project example: myproject and let's come to our terminal of your project, let's add the gitlab project repository path in local by following command: 
```
$ git remote add origin git@gitlab.com:username/myproject.git
```

Step 5: After successfully running the above command, you have setup the Git repo and now you can push the files. but before that lets check repository which we added is correct or not.? by the following command:
```
$ git remote -v
```
Now, you have got your repository result.

Step 6: Finally, we have correctly setup with it and let's push the file into our myproject gitlab repository into our default branch named master  by the following command: 

$ git push origin master
This last word named master. This is a branch in your gitlab repository. so you have to push the file in your working branch
```
Example:
$ git push origin <master> or <your_branch>
```

Thanks for reading.
---
<a name="chapter4">
<h1>Chapter 4 -  How to create a branch in git repository in gitlab using command line.</h1>
</a>
 


In this post, we will be learning about how to make a branch in git repository so lets begin with it.

First, we need check that in which repository or branch we are working on it. So to check repository and branch use following commads:

1. To check your git repository name:
```
$ git remote -v
```

2. To check your branch in git repositry: you will be able to see all your branches by following command:
```
$ git branch --all
After checking all the thing that you are in a right git repository and branch, Lets begin with creating a branch in gitlab
```


Step 1: Type the below command to Create a branch in repository in gitlab by following:
```
$ git checkout -b your_new_branch
```
So, here in this command line -b is the main thing which creates your new branch into the repository.



Step 2: Check your branch by the above Point 2 command, so that you can be in a correct branch. If you are not into your correct branch, follow the below command:

How to Move or Change from one branch to another branch by following command: 
```
$ git checkout your_branch
```

Step 3: After successfully creating a new branch and moving into your new branch. Let's push your files in new branch by following below commands:
```
//To Add all the Files
$ git add .

// To commit with message
$ git commit -m "My New Branch Commit"

// To push the file into repo
$ git push origin your_branch
```

That's it. You are Done.

---
<a name="chapter5">
<h1>Chapter 5 -  How to remove or delete branch from git repository using command line.</h1>
</a>


In this post, we will be learning about how to delete a branch from git repository using command line.

Step 1: Let's check the branch first, which we want to delete the branch from git repository by following: 

Checking the Branch:
```
$ git branch --all
```


Step 2: Now, check your correct branch which you want to delete it and lets delete the branch by following command:
```
$ git push origin --delete your_branch_name
```
In this command --delete is the main code for deleting the branch from your git repository by calling its branch name.



You are done.

Thanks for reading. 
