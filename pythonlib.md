### common python commands
To know python version, packages installed.
```
python --help or python -h
python --version or python -V
pip freeze > requirement2.txt
pip install -r requirements.txt
python
>>> import requests; requests.__version__
```
To know the list of all packages installed.
```
pip list
conda list
conda list request ---> give individual package info, both through conda and pip
```
To install a python package through pip
```
pip --help
pip --version --> 18.1
pip install --upgrade pip --> Requirement already up-to-date: pip 
pip install urllib3 --> Requirement already satisfied
pip install --upgrade urllib3 --> Requirement already up-to-date
pip uninstall flask --> only uninstall flask, not its dependencies
pip list
pip freeze
```
To know the location of python executable
```
import sys; sys.executable --> 'C:\\Users\Local\\Continuum\\anaconda3\\python.exe'
```
Creating python virtual environment :
https://packaging.python.org/guides/installing-using-pip-and-virtualenv/
```
pip install virtualenv
virtualenv --version ---> 16.1.0

virtualenv venv  ---> will create new directory **venv** with directories Include, Lib, Scripts, tcl
.\venv\Scripts\activate --> see (base) is changed to (venv)
check the python executable path: 
where python or import sys; sys.executable
deactivate --> will leave venv
```
Before you will start installing any packages
```
>>> pip list
Package    Version
---------- -------
pip        18.1
setuptools 40.5.0
wheel      0.32.2

>>> pip freeze ---> no dependicies installed, will output nothing
```




