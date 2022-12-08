# Getting started with a CLI

The following page describe basic commands to get familiar in working with a CLI.

## Contents

- [Getting started with a CLI](#getting-started-with-a-cli)
  - [Contents](#contents)
  - [Where am I?](#where-am-i)
  - [How do I see a list of files and directories?](#how-do-i-see-a-list-of-files-and-directories)
    - [Additional parameters](#additional-parameters)
  - [How do I create a new directory?](#how-do-i-create-a-new-directory)
  - [How do I move around in a CLI?](#how-do-i-move-around-in-a-cli)
    - [Go back to your user folder (home)](#go-back-to-your-user-folder-home)
    - [Go up a directory](#go-up-a-directory)
    - [Go to the previous directory](#go-to-the-previous-directory)
  - [How to create or open a file?](#how-to-create-or-open-a-file)
    - [Creating an empty file with bash](#creating-an-empty-file-with-bash)
    - [Creating an empty file with PowerShell](#creating-an-empty-file-with-powershell)
    - [Opening a file with a 'dedicated' program](#opening-a-file-with-a-dedicated-program)
  - [Optional: Some references](#optional-some-references)

## Where am I?

After having started your CLI the way it was explained before, a good idea is to see 'where' we are: A CLI points to a so-called `working directory`. Type `pwd` to, well, Print the Working Directory or Dir:

```bash
pwd
```

(`enter` always executes the command, as you probably know, so we will not repeat that. Remember: we will not repeat that)

Some people nowadays say `Folder` instead of `Directory`, that is mainly just another word... For details fire up your favorite search engine and search for 'directory vs folder'.

The answer to `pwd` will be a *path*, like:

```text
/Users/frens
```

> Note that in Windows, paths look different than other operating system. In this case, the path will be **C:/Users/frens**

## How do I see a list of files and directories?

After knowing 'where' we are, we want to enjoy the view, by asking for a `list of files and directories` in the current working directory:

```bash
ls
```

### Additional parameters

> Note that the following parameters do not work in PowerShell

A lot of commands have endless variations if we add `parameters`, like `-l`, you will get 1 item per row:

```bash
ls -l
```

or `-a` (All) to also show hidden items:

```bash
ls -a
```

and you can also combine parameters:

```bash
ls -al
```

## How do I create a new directory?

```bash
mkdir MyVeryOwnDir
```

If you do 'ls' again you will see there is a new item in the list with the name you chose.

## How do I move around in a CLI?

We can move to a directory using the `cd`(change directory) command:

```bash
cd MyVeryOwnDir 
```

Once you a couple of characters, the CLI will often be able to complete it for you when you hit the `TAB` key.

### Go back to your user folder (home)

Sometimes it is convenient to go back to the home directory. This the directory that is connected to the account you are logged in to. To go to your Home directory, type the following command:

```bash
cd ~
```

(there is a `space` after `cd`)


### Go up a directory

If you are currently in `/Users/frens` and you want to go *up* to `/Users`, use `..`:

```bash
cd ..
```

### Go to the previous directory

If you are currently in the `/Users/frens/repos/project` directory, but you want to back to your previous directory `/User/frens/Downloads`, use `-`:

```bash
cd -
```

## How to create or open a file?

### Creating an empty file with bash

```bash
touch someSillyFilename.py
```

### Creating an empty file with PowerShell

```bash
New-Item someSillyFilename.py
```

### Opening a file with a 'dedicated' program

```bash
open someSillyFilename.py
```

In Windows you can open any file with Notepad by using `notepad`:

```bash
notepad someSillyFilename.py
```

To open Visual Studio Code to edit this file you may need to do some
[work](https://techstacker.com/how-to-open-vscode-terminal-command-line/)
, but afterward you can:

```
code someSillyFilename.py
```


## Optional: Some references

- [Getting started with Linux and Bash](https://learn.microsoft.com/en-us/windows/wsl/tutorials/linux)
