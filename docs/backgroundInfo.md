# General info about this material

## Context behind these pages
- 202211: When students were installing Python/Flask, without explanation, they got some commands to do on the CLI (Command Line Interface), which led to a lot of students not being able to do so themselves, also involving a lot of teacher effort to get it right. A few weeks later, students got an instruction about using git (done by a student). For that also, the CLI was used, but was (still) new to most of them. When doing Python, most students only knew how to edit/run programs from VS Code. They did not really know about the files or how to run Python from the CLI (or even that it could be done from CLI).

## Considerations
The following paragraphs contain considerations when working with a CLI.

### Use PowerShell over Command Prompt on Windows
Between all the command line interfaces across operating systems, the Command Prompt on Windows is the only interface that has slightly different commands for doing mundane operations, like displaying a list (`dir` instead of `ls`) or removing a directory (`rmdir` instead of `rm`).
PowerShell has integrated most of the commands that were missing in Command Prompt. Considering all Windows devices have PowerShell, it is advised to let students work with PowerShell instead of the Command Prompt.

Alternatively, students can also make use of the Git Bash application after installing Git. Git Bash allows Windows users to use a command line interface that resembles an interface from a Unix operating system, like Linux or macOS.

### Use git from the CLI instead of other graphical user interfaces 
We see new GUI-apps for using git every year. There is one 'constant' way to use git: the command line. Furthermore: from the CLI you can use *all* of its functionality, which is not true for all GUIs. We think every Software Engineer should have at least 'some' idea of how to use the command line.  

This is not to say we should enforce using Git from the terminal. Students should be aware that Git is a tool that is originally created for the command line. However, the goal for the start semester is to get students familiar with the basics of Git. If they prefer to use a graphical user interface, then they may definitely use it.

