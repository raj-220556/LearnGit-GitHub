# Learn Git & Github

## What is Git?

Distributed Version control System (VCS) that helps developers track their codebases, collaborate with other and manage multiple versions of a project.

- Git is decentralized, which means you don't need a central server. Instead every developer has a full copy of the repo on their machine.
- Must have sill for every developer. you need to at least know the basics (add, commit, push etc).

Key Features of Git :
  - Distributed System
  - Version Tracking
  - Collaboration
  - Branching
  - Merging
  - Remote Repositories
  - Extensive Tooling
  - Staging Area
  - Speed
  - Open-Source & Free

## What is GitHub?
Web-based platform used for version control and collaboration. it hosts repositories and provides an interface to manage your code and do many other things.

- GitHub offers collaboration features like bug tracking, feature requests, task management & wikis.
- Git is the VCS and GitHub hosts repositories. There are many other platforms that can host Git repos, 
  Such as Gitlab & BitBucket.

### Installing Git:
URL : <https://git-scm.com/downloads>

### Git Workflow:


After Installing git:

```bash
$ git config --global user.name "Z3ncryptedbu9"
$ git config --global user.email "Z3ncryptedBu9@gmail.com"
```

for checking user name & email
```bash
$ git config --global user.name 
Z3ncryptedBu9
$ git config --global user.email
Z3ncryptedBu9@gmail.com
```
- seting default branch as main
```bash
$ git config --global init.defaultBranch main
```

### git init
```bash
$ git init
```
Initialized empty Git repository in `/home/raj-kumar/Desktop/Git&GitHub/`

Example `repo/.git/`

- Initialize new repository in your Working Directory (project folder)
- This creates a new hidden folder called .git

**To check:**
```bash
$ ls -a
```
**To Delete:**
```bash
$ rm -rf .git
```
- In VsCode files are shown in Untracked means they are in working directory

### git status
```bash
$ git status 
```
```
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Digitalclockbackground.png
        clock.css
        clock.html
        clock.js
```
nothing added to commit but untracked files present (use "git add" to track)

- It shows the status of each file

### git add
```bash
$ git add index.html
```
- add single file by name
or
```bash
$ git add .     
```
- Adds all the file

- Add your files to the "Staging Area"
- you specify the files or use a period for all files

### git commit
```bash
$ git commit -m 'Initial commit'
```
- `-m` : message


- Commit your files to local repository on your machine
- It goes as created a Local Repository
->you can commit as often as you would like


**Upto here all are local machine.**

--- 

### Making changes

- If we write any line of code that is commited in local repo then
- status as changed as Modified.

so,we can add the file again
```bash
$ git add .
$ git commit -m 'add console'
```

### git log
- It shows started with most recent one
```bash
$ git log
```
```
commit 43c161c3872c80c718db369ec9419951a06a5dfb (HEAD -> main)
Author: Z3ncryptedbu9 <Z3ncryptedBu9@gmail.com>
Date:   Mon Jul 21 17:57:55 2025 +0530

    Added Console

commit e7f2a93f39046ec283654fb779f4d07d9e2fd481
Author: Z3ncryptedbu9 <Z3ncryptedBu9@gmail.com>
Date:   Mon Jul 21 17:32:43 2025 +0530

    Initial commit Message
```  

## Remote Repository 
GitHub repo 
- push to your repository
- this could be Github or another service like Gitlab or BitBucket.

**Step 1**: Create a repository in GitHub profile

**Step 2** : run your system given commands
```bash
$ git remote add github https://github.com/N220556/LearnGit-GitHub.git
$ git branch -M main
$ git push -u github main
Username : N220556
Password : <token>
```
- We can enter password to generate token from github

**step 1**: go to url: https://github.com/settings/tokens

**step 2** : give name (Git Access)
	 set expire date(minimum) and select Scope (repo all)

**step 3** : Generate token
**step 4** : enter your token as password


### git pull
- pull changes from the remote repo to your local machine.
- Others users may make changes. You pull their changes to your machine
```bash
$ git pull
```
### .gitignore file
- anything puts in this file not belongs to repository.
- in our example it holds .env file which stores API_key

```bash
$ git commit -am "Without add direct"
$ git push
```
```bash
$ git add index.html && git commit -m "Single line commmand"
$ git push
```

**Downloading** : You can download a zip of the repo (can't do pull, add, commit with zip)

**git clone** : Get a copy of the full repo on to your machine.

**git pull** : Get the latesy changes from a repo

**git fetch** : Get latest changes without merging.

**forking** : Copy a repository into your own account.

## Branching
```bash
$ git checkout -b feature/newbranch
Switched to a new branch 'feature/newbranch'
$ git branch
* feature/newbranch
  main
```
```bash
$ git add .
$ git commit -m "New branch page"
$ git push -u github feature/main
```
### pull request & merge
- done github gui

### by locall
```bash
$ git merge feature/newbranch
# delete branch locally 
$ git branch -d feature/newbranch
```

## CI/CD Pipeline with vercel (for hosting projects)
- Hobby package is free one
- Deploy your repository, as a website.
- we change anything push into repo it directly goes to website.
