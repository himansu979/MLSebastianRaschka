### common python commands
To know python version, packages installed.
```
python --help or python -h
python --version or python -V
python freeze > requirement2.txt
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
To install a python package
```
pip install urllib3 --> Requirement already satisfied
pip install --upgrade urllib3 --> Requirement already up-to-date
```
To know the location of python executable
```
import sys; sys.executable --> 'C:\\Users\Local\\Continuum\\anaconda3\\python.exe'
```
Creating python virtual environment
```
pip install virtualenv
virtualenv --version ---> 16.1.0

virtualenv venv  ---> will create new directory **venv** with directories Include, Lib, Scripts, tcl
.\venv\Scripts\activate --> see (base) is changed to (venv)
check the python executable path: 
where python or import sys; sys.executable
deactivate --> will leave venv
```
