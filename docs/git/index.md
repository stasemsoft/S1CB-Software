# Getting started with Git 

## Why? 

One of the most important tools in every Software Engineers' toolbox is version control! Nowadays we use ***git*** as a default for that. In git one can create a so-called `repository`. This is a storage that keeps track of changes made to files and directories. It gives you control to add/inspect/revert changes and helps with collaboration. 



FHICT has its own git-server for students which you can find via StudentSquare or directly: 
[git.fhict.nl](https://git.fhict.nl). A popular server where you can share your projects to the whole world is 
[github.com](https://github.com).  



## git basic concepts

When reading the story below you can use this as a cheat sheet (you don't have to understand the terms before reading the text below, they will be introduced along the way): 
+ working directory: The folder in which you will work.
+ repository:        A storage system that keeps track of the changes per file. Each client has their own local repository and the server is considered the remote repository.
+ staging:            select which changed files should be committed.
+ CLI:                Command line interface.
+ clone:             make local copy of the repository. 
+ checkout:          apppoint one version to your current 'working directory'
+ commit:            register selected changes (that were made to files in the working directory) on the local repository. 
+ push:              upload the locally committed changes to the remote repository. 
+ pull:             Take all new changes that are on the server (typically
  changes made by other developers) and add to your local repository.
+ status:           Ask git what the status is of the local repository compared to the remote and which changes are staged, and unstaged.

The first concept we have to grasp is that of a `repository`: you could see a
repository like a datastore, where files can be stored in directories. Below you see a diagram that depicts a typical setup for git. The 'remote' rectangle represents a server that serves as redundant copy and mediator between clients, 'Laptop 1' and 'Laptop 2' are two possible clients that collaborate on the development of a system.

![](figures/gitpictures-0%20-%20Start.jpg "git start")

Suppose there is a `repository` on a `git server` containing a project you are going to work on. To start working on it you first `clone` the project: this means `git` will create a local copy of the repository, including the history of all files in the project. The last version of the files will be appointed as `working dir`. You can edit your files locally in this working directory the way you normally do: you can edit files with your favorite editor/IDE (Integrated Development Environment). The following diagram depicts this process. The Git database will contain version 1 of the system after cloning.

![](figures/gitpictures-1%20-%20Clone.jpg "git clone")

In the background, the GIT clone command will (probably) already do a checkout. This means that working copies of the files are being loaded from the database and stored on disc so they are ready to be edited. If this is not yet the case, you can manually perform the checkout. In the diagram below you see that the checkout generates the latest version of the system in the working directory.

![](figures/gitpictures-2%20-%20Checkout.jpg "git checkout")

When you made some changes to your local working directory you may want to `commit` those changes to the local history. Look at the following 2 diagrams to see what happens:

![](figures/gitpictures-3%20-%20Change.jpg "git change")
![](figures/gitpictures-4%20-%20Commit.jpg "git commit")

After committing, you can `push` the new versions to the git server. 

![](figures/gitpictures-5%20-%20Push.jpg "git push")

When changes are pushed to the server other developers can `pull` your changes to their local versions, so they are synchronized. While `pull` is the conventional way of doing this. In the background it consists of two commands called: `fetch` and `merge`. While we don't discuss `fetch`, you can read about the `merge` command below.

![](figures/gitpictures-6b%20-%20Pull.jpg "git pull")

Next time you don't need to create a new clone, but before creating new changes yourself it is wise to `pull` possible changes made by other people (and pushed by them to the server) from the git server to your local repository and point your working working dir to this version. After that you can (again) develop until you have changes that commit and push to the server again. 

Sometimes you create a local change, commit it locally, and when pushing it turns out that someone else pushed a change to the server. After pulling their changes from the remote repository (if changes were made in the same file) you may have a `merge conflict`: before you will be able to push your changes to the server, you first have to `merge` the changes created by the other person into your working version. After that you can push your changes to the server. 


When using a language that has `source files` (like '.cs'-files) and `compiled files` (like '.exe'-files) then normally you will only want to add the source files to your git repository. By  creating a so-called `.gitignore`-file git will know which files to ignore, so these will not be added to the repository. Examples can be found at 
[gitignore-examples](https://www.golinuxcloud.com/gitignore-examples/). 


## Git command line

When you have installed git, you will have a git command line interface (CLI) tool available. An example CLI is `git bash`. We will explain how to perform the basic actions from this CLI. After that you could look into using some GUI-Git-tool (for example Git Kraken, Git Desktop, Git GUI, Git Extensions, Git Tortoise, SmartGit). Also a lot of IDE's have Git built-in. 



### Create a repository

![](figures/git_newproject.png "new project")

A repository is a place where your code and all previous versions of it are stored. We will now create a repository in the so-called *git-lab* environment at FHICT (only available for FHICT-students;
An alternative would be creating a repository at *GitHub.com*, which is very similar, but then the whole world can potentially see what you are doing)
Use a browser to go [https://git.fhict.nl](https://git.fhict.nl) and create a git repository.
Copy the https-url to your clipboard, we need it in a few moments.

![](figures/gitHttpsUrl.png "git https")

In Git you typically have a `repository` on a network somewhere where
all files of your project are stored, including the history of
`commits` to those files.
Furthermore you have a  `local repository` with all source code versions
which you regularly `synchronize` (using `push` and `pull`) with
the remote repository on a server.
Other people in your team sync with the same remote repository.

### Clone the repository

Next step is creating a so-called `clone` locally on your laptop.
This will be your workspace where you can develop.
By keeping it up to date with the server
(`pulling` the changes of other developers from the server and `pushing` your changes to the server)
you can work together with other developers.

You can choose between several *tools* to do the `pulling`
and `pushing`,
some created to be easy to use and some more advanced.
Here the *command line* is used: the advantages being that **all**
`git`-functionality is available from the command line or CLI. 
[Sarters-info on the CLI](../cli)

So start a `terminal` or `bash` shell.
Go to the `directory` where you want your workspace to be.
In the starters info you find explained how to create a directory with `mkdir`, change your working dir with `cd`.  

So, to create dir 'myProject' in an already existing dir 'Documents' you could type the commands:

```
cd Documents
mkdir myProject
cd myProject
```

Most of the time you don't have to type whole names like *Documents*:
just type *Doc* and
press the *tab* key and probably the *shell* will complete the name.

![](figures/gitbash1.png "bash")

In the CLI 'clone' the git-repository from the server
to your local directory by typing:

```
git clone pasteYourGitUrlHere
```

After that (you will be asked for your 'username'/'password')
you now have a local copy ('clone') of the entire history of this repository
(for a just created project this is still empty).
To go inside the local 'repository-directory',
which after a 'clone' contains the 'latest' version of the files,
use

```
cd dirname
```

Do you want to know what the status of git is? 

```bash
git status
```

This command tells you the status of your local repository: what flies/folders changed and what is selected (staged) for committing. In addition it shows with how many commits it differs from the server. Currently it will show there is nothing to commit (because you did not make local changes to the repository).

After this you can start editing your files in your fancy-editor-of-choice (IDE). 
For this info-page that means we'll have an intermission until you have changes
that you want to commit to git. 

[Intermission](https://www.youtube.com/watch?v=O0wOD9TWynM)

We now assume you have some changes you want to commit (locally) and then push to the server. 
Most often you can do that from your IDE: and that is a valid option! On this
page we will continu describing how to do it from the CLI. 

```bash
git status 
```

Before committing we have to `stage` the changes (telling git what has to be
committed): 

```bash
git add * 
```

or (to explicitly `stage` a specific file): 

```bash
git add theFilename
```

If you want to see what will be committed you can of course always: 

```bash
git status 
```

Ready to commit?

```bash
git commit -m "adding some comment"
```

The '-m' tells git that the string after it is the description of what is in the commit: add some comment there that describes your changes. Commit messages are very important in collaborative setups because this tells your colleagues who are working on the same system what has changed. It also helps you find specific commits in your commit history if you want to trace bugs or revert to a specific version! In a collaborative setup you should agree on a commit message standard. 

```bash
git status 
```

In the status info you see that you are 1 commit ahead of the server. This means
that you have 1 commit locally (in your local copy of the repository) that still
has to be `push`ed to the git server: 

```bash
git push
```

If noone pushed changes to the server than your commit will succesfully be pushed to the server, which we can check (again) with `git status`. If someone *did* push changes to the server then the push will fail. Git will tell you to first pull these changes before pushing. After pulling and possibly merging you are allowed to push. 

## Next development session

When you start working on new changes it is wise to start with a 

```bash
git pull
```

so you get all the changes pushed to the server in the meanwhile. 


Remark: The way-of-work described on this page is a simpel one: a lot of developers
use some kind of so-called branch-based workflow, but that's out of our scope
for now.   



![](figures/gitgud.png "git gud")


## Optional: some resources

+ [Downloadable Git Commic](figures/Git%20Commic.pdf)
+ [githowto.com](https://githowto.com/)
+ [gitlab university user_training](https://docs.gitlab.com/ee/university/training/user_training.html)
+ [Git book (very thorough!)](https://git-scm.com/book/en/v2)
+ [FHICT-git-server https://git.fhict.nl/](https://git.fhict.nl/)

