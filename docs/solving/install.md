# Checking installations

Let's check some installations/configurations

## Python

To check whether *python* is installed correctly. 
In windows: open a  [CLI](../cli), type: 

```bash
py
```

and press enter.  If the commmand is known that's OK! If it is NOT: open a browser on [python.org](https://python.org), download the python installation. 
While running this installion make sure you twice(!) select that the PATH variable has to be set! Open a new CLI, check `py` is now recognized!

Also `python` should be recognized:

```bash
python
```

(or `python3`)

- Python command not recognized:
Check your PATH variable setting (advanced system settings) to see if python and the scripts are correctly configured.

## Flask

On a CLI, type 

```bash
flask --version
```

If that's recognized that means *flask* is installed. 
If not, use:

```bash
pip install Flask
```

## Some more things that could help you trouble shoot:

- Flask not working:
Check if you have the correct virtual env 'activated'
Have you installed it correctly in the environment?
- Flask not working in Visual studio code:
    Flask run command not working:
        Are you using the correct command? This can very among versions. Check version by running 'flask --version'
    Flask not showing HTML template:
        make sure to put the templates in a folder called 'templates'.

## External Links

[ionos: troubleshooting common python problems](https://www.ionos.com/digitalguide/websites/web-development/troubleshooting-common-python-problems/)
[python.org: Python on windows FAQ](https://docs.python.org/3/faq/windows.html)


