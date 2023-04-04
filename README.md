# Git-Tutorials

Here, We will be learning about how to use Git and many other things like.


### Table of contents

- [Chapter 1 - How to download or install Git](#chapter1)
- [Chapter 2 - How to get the current branch name in Git ?](#chapter2)
- [Chapter 3 - How to create git repository in local and connect to Github, Gitlab, Bitbucket project.](#chapter3)
- [Chapter 4 - How to create a branch in a repository.](#chapter4)
- [Chapter 5 - How to remove or delete branch from git repository using command line](#chapter5)
- [Chapter 6 - How to clone a git repository using command line.](#chapter6)
- [Chapter 7 - How to check current git repository name using command line..](#chapter7)
- [Chapter 8 - How to get all remote branches present in Git repository using command line](#chapter8)
- [Chapter 9 - How to change remote git repository using command line](#chapter9)
- [Chapter 10 - How to add SSH Key in Gitlab](#chapter10)
- [Chapter 11 - How to Rename a Git Branch](#chapter11)
- [Chapter 12 - How to checkout to previous working git branch](#chapter12)
- [Chapter 13 - How can I get a list of Git branches ordered by most recent commit ?](#chapter13)
- [Chapter 14 - How to check or set username and email address in git using cmd](#chapter14)


 

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


---
<a name="chapter6">
<h1>Chapter 6 -  How to clone a git repository using command line.</h1>
</a>



In this post, you will be learning how to clone a git repository using command line.

Basically clone git repository means that when you want to download an existing git repository to your local computer or system and can start working on it.

Cloning a repository using the command line
Go to your git repository and copy the HTTPS repo link and paste in your git clone command as follows:

Syntax:
```
$ git clone {repository URL}
```

Example: 
```
$ git clone https://github.com/my-project.git
```

Thanks for reading.


---
<a name="chapter7">
<h1>Chapter 7 -  How to check current git repository name using command line.</h1>
</a>

In this post, you will be learning how to check the working Git Repository name, by the following command:

Step 1: Check your Git Repository name: 
```
$   git remote -v
```
you are done.!

Thanks for reading.

---
<a name="chapter8">
<h1>Chapter 8 -  How to get all remote branches present in Git repository using command line.</h1>
</a>

How to check all branches in git
In this article, we are going to learn about getting or Listing all the remote branches names from your git repository using command line. 

There are many methods to check the remote branches  (git branches) name as follows:

Method 1: Listing all remote branches name by mentioning current branch with astric symbol (*):
```
$   git branch -a
```
Output:
```
HP@HP-PC MINGW64 /c/xampp/htdocs/project
$ git branch -a
* current_branch
    remotes/origin/HEAD -> origin/current_branch
    remotes/origin/branch2
    remotes/origin/branch3
```

Method 2: Listing all remote branches name:
```
$   git branch -r
```
Output:
```
HP@HP-PC MINGW64 /c/xampp/htdocs/project
$ git branch -r
    remotes/origin/HEAD -> origin/current_branch
    remotes/origin/branch2
    remotes/origin/branch3
```
Method 3: Listing all remote branches name with its origin:
```
$   git remote show origin
```
Output:
```
HP@HP-PC MINGW64 /c/xampp/htdocs/project
$ git remote show origin
remote: 
* remote origin
  Fetch URL: git@gitlab.com:username/project.git
  Push  URL: git@gitlab.com:username/project.git
  HEAD branch: current_branch
  Remote branches:
    current_branch  tracked
    branch2 tracked
```

Method 4: Listing all remote branches name:
```
$   git branch --all
```
Output:
```
HP@HP-PC MINGW64 /c/xampp/htdocs/project
$ git branch --all
* current_branch
    remotes/origin/HEAD -> origin/current_branch
    remotes/origin/branch2
    remotes/origin/branch3
```

Thanks for reading.

---
<a name="chapter9">
<h1>Chapter 9 -  How to change remote git repository using command line.</h1>
</a>
In this article, we will be learning about how to change remote git repository using command line. Which means How do I rename a Git repository as simple?

So, Let's get started with it:



Step 1: Let's check current remote git repository name as follows: 
```
$ git remote -v
```
Output:
```
HP@HP-PC MINGW64 /c/xampp/htdocs/project  
$ git remote -v  
  origin  git@gitlab.com:user/repository1.git (fetch)
  origin  git@gitlab.com:user/repository1.git (push)
  ```
  
if you use HTTPS URL repository link, you will have to provide username and password with it.



Step 2: Now, lets change the remote git repository using the command line.
```
$ git remote set-url origin git@gitlab.com:user/repository2.git
```

if you use HTTPS URL remote repository link, then you will be asked to provide the username and password. 



That's it. Now, you can start your project as flow with git pull and git push.

Thanks for reading.

---
<a name="chapter10">
<h1>Chapter 10-  How to add SSH Key in Gitlab.</h1>
</a>

In this article, we are going know about how to add ssh key to your GitLab account from system.



Step 1: Lets go to gitlab.com and  open your profile or setting, and search SSH Keys in Sidebar, click on it.

Step 2: SSH Key page opens, then you will find an option to generate one SSH Key or you can use old SSH Key.

Step 3: You can create and configure ED25519 Keys for SSH - so use the following command on your CMD / Terminal / GitBash as follows:
```
$ ssh-keygen -t ed25519 -C "<comment>"
```
The -C which is quoted as comment, there you can put your email address like: -C "example@email.com" to label or name your generated SSH Key.

Once the command is successful. OUTPUT will be as follows:
```
HP@HP-PC MINGW64 /c/xampp/htdocs/project (master)
$ ssh-keygen -t ed25519 -C "example@email.com"
Generating public/private ed25519 key pair.
Enter file in which to save the key (/c/Users/HP/.ssh/id_ed25519):
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /c/Users/HP/.ssh/id_ed25519
Your public key has been saved in /c/Users/HP/.ssh/id_ed25519.pub
The key fingerprint is:
SHA256:sdfgsdfgfglsdfdgufussfdsf+ARU example@email.com
The key's randomart image is:
```

Step 4: After your SSH key generated as above, now need to copy that generated ED25519 Key known as SSH Key as follows: 
```
$ cat ~/.ssh/id_ed25519.pub
```

OUTPUT:
```
$ cat ~/.ssh/id_ed25519.pub
ssh-ed25519 asdasdasdasdasdasd/pwb4bcc7sdfsdfsfddsfsdfsd/Jtt2adadadadsXfs example@email.com
```

Step 5: Finally we 


---
<a name="chapter11">
<h1>Chapter 11-  How to Rename a Git Branch.</h1>
</a>

Git Rename Branch
To rename a Git branch, run the following command: git branch -m <old> <new>.This will change the name of the branch you are viewing to the new name you specify.  The “old” is the name of the branch you want to rename and “new” is the new name for the branch.

Command:
```
$ git branch -m <old> <new>
```


Note : You don't need to specify the old branch name if you want to rename the current branch you are in.
```
HP@HP-PC MINGW64 /c/xampp/htdocs/myproject (my-branch-name)
$ git branch -m my-new-branch-name
 ```
after running the above command, your branch will look like shown below:
```
HP@HP-PC MINGW64 /c/xampp/htdocs/myproject (my-new-branch-name)
$ 
```

To Check all your branch List you created:
```
HP@HP-PC MINGW64 /c/xampp/htdocs/myproject (my-branch-name)
$ git branch
```



Thanks for reading...
 
 
---
<a name="chapter12">
<h1>Chapter 12-  How to checkout to previous working git branch.</h1>
</a>

How to checkout to previous working git branch


In this article, you will learn how to move to previous working branch in git, which means git checkout to previous branch.



1. If you want to move or checkout to exactly to the previous git branch, you can follow as:
```
$ git checkout -
 ```
2. Here, you can checkout to your previous git branch according to your branch list.
```
$ git checkout @{-1}
 ```
in above command git checkout @{-1} , you can change with another number. @{-N}, N is number where need to move to branches list point or position.



Thanks for reading.
 
  
---
<a name="chapter12">
<h1>Chapter 13-  How can I get a list of Git branches ordered by most recent commit ?</h1>
</a>
 
 How to get a list of Git branches ordered by most recent commit


In this article, you will be learn how to get a list of Git branches ordered by ascending and descending wise.

Let's see how to get all the git branches as follows:

1. get list of git branches in Descending:
```
git branch --sort=-committerdate
```

2. get list of git branches in Ascending:
```
git branch --sort=committerdate
```



Thanks for reading.
