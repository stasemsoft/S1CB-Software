# Python environment setup

You will be learning the basics of programming with
[Python](https://www.python.org/).

We will describe the following steps to get started:

1. Install Python
2. Install Visual Studio Code
3. Install the FHICT Python package

## 1. and 2. Python and Visual Studio Code

For the first two steps: follow the instructions fromand
[this tutorial](https://code.visualstudio.com/docs/python/python-tutorial),
which will tell you how to install Python itself and also
`Visual Studio Code`, an editor to write Python code in.

## 3. Install the FHICT Python package

The following page shows you how to install a [Python package](https://realpython.com/python-modules-packages/).
You will need this package during the first 9 weeks of the start semester.

You should have Python already installed.
Furthermore `miniconda` or `anaconda` are not required. Feel free to uninstall these applications if you don't know what these do.

### Steps

1. Open a Command Line Interface (see [here](../cli) for more information)
2. Run the following command:

```bash
python -m pip install fhict-cb-01  
```
on MacOS and *Nix or 
```bash
py -m pip install  fhict-cb-01 
```
on some Windows Python installs.

## Troubleshooting
If you get an error as follows : `ModuleNotFoundError: No module named 'fhict_cb_01'"`
Make sure that you installed the FHICT Python package in the same environment that you are trying to run it in. In Visual Studio Code check the bottom of the window and check the interpreter. You may have multiple python environments on your computer and you might have installed the package in another environment. Also make sure that install the pip package as above did not give an error message.
![Screenshot-image](https://user-images.githubusercontent.com/91896373/223751545-68d37197-30e5-4797-a42c-7a55e24e733a.png)

