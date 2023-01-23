# Troubleshooting and FAQ

This page is to help you get up and running again when stuck with one of the python/flask/arduino-tasks in semester 1 course based.

## Strategy to tackle a problem

You *will* get stuck now and then, so it makes sense to have a more or less structured way to cope with that. So try to be aware of what you do when solving a problem. It will help you get better in time. 

Several short tips:

- What was your last change? Could it have caused the problem you are now facing?
- Is there an error or other kin of message that tries to tell you what's wrong?
- Can you put a breakpoint somewhere and start debugging?
- If you were doing a tutorial or other instruction: did I understand what action I was performing (and why)?

## Check if everyting is installed correctly

[Check installation/configuration](install)

## Python: What is a ‘venv’ / virtual environment, and do I need it?

No, you do not need to use them. You will be working mostly with 1 version of Python and with the same set of dependencies, so having 1 sole installation is fine.

What are they?  
When you run many python applications on your device, it could be that you might need more than 1 version of python or libraries. To overcome conflicts, you could use virtual environments. Each environment will get its own set of libraries/dependencies. To install them, you would need to activate that environment first.  
  
Caution:  
Be aware when you start searching for solutions to bugs or errors you are facing, since sometimes the answers are using the context of such an environment. So do not blindly copy paste the solutions, but tailor them to your situation.

## Visual Studio Code is not allowed to run scripts or cannot find commands

Your Visual Studio (Code) is not installed correctly. It is probably installed in a ‘user account’ (you probably chose the option: For this environment only). You can solve this by reinstalling you VS Code in the right account by making sure it is installed for everybody using your laptop.  
  
In general it is wise to give IDEs like Visual Studio more privileges. Developing Software often requires more access or rights than regular user accounts permits.