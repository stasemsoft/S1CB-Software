# First steps with the CLI

## Where am I? 

After having started your CLI the way it was explained before, a good idea is to see 'where' we are: A CLI points to a so-called `working directory`. Type `pwd` to, well, Print the Working Directory or Dir: 

```
pwd
```
(`enter` always executes the command, as you probably know, so we will not repeat that. Remember: we will not repeat that)

Some people nowadays say `Folder` instead of `Directory`, that is mainly just another word... For details fire up your favorite search engine and search for 'directory vs folder'. 

The answer to `pwd` will be a `Path`, like:

```
/Users/frens
```

## List of files and dirs

After knowing 'where' we are, we want to enjoy the view, by asking for a `list of files and dirs` in the current (working) dir: 

```
ls
``` 

## Making a dir  

```
mkdir MyVeryOwnDir
```

If you do 'ls' again you will see there is a new item in the list with the name you chose. 

## Change Dir: Moving around

Now we can change the working directory with Change Dir: let's go into the dir we created: 

```
cd MyVeryOwnDir 
```
once you type the first characters of the dir name the CLI will often be able to complete it for you: hit the 'TAB' key. 

You may want to know where we are now: remember `pwd`? 

To go to  your Home dir (connected to the account you are logged in with):
```
cd ~
``` 

To change the dir to a directory one step higher in the dir structure: 

```
cd ..
``` 


## Creating and Editing a file 

```
touch someSillyFilename.py
```
creates an empty file, which you of course can check using `ls`. Opening the file with the 'dedicated' program for it: 

```
open someSillyFilename.py
``` 

To open Visual Studio Code to edit this file you may need to do some 
[work](https://techstacker.com/how-to-open-vscode-terminal-command-line/)
, but afterward you can:

```
code someSillyFilename.py
``` 


## Parameters

A lot of commands have endless variations if we add `parameters`, like `-l` (to get 1 List of items)

```
ls -l
```

or `-a` (show All, which adds '.' (which denotes the current dir), '..' (the parent dir), and hidden files (which names astart with a '.') to the list): 

```
ls -a
```

and you can also combine parameters: 

```
ls -al
``` 

## Optional: Some references 

- [Getting started with Linux and Bash](https://learn.microsoft.com/en-us/windows/wsl/tutorials/linux)
