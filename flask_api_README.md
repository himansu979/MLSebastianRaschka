## Step by step instructions for setting a Flask API

#### Directory structure for running Flask app as a python package

```
myFlaskUI/
  .flaskenv
  run_app.py
  venv/
  myFlaskApp/
    __init__.py
    routes.py
    templates/
```
**myFlaskUI/** is top level directory. **myFlaskApp/** is python package as it contians ``__init__.py`` file. <br>
`.flaskenv` defines the environmental variable **FLASK_APP**. <br>
contents of `.flaskenv`. It tells Flask to run this python module.
```
>> .flaskenv
FLASK_APP=run_app.py
```
`run_app.py` is the python module that just imports the **app** variable (which is instance of the Flask class) from the python package.
```
>>> run_app.py
from myFlaskApp import app
```
`__init__.py` defines the **app** object of FLASK class.
```
>> __init__.py
from flask import Flask
app = Flask(__name__)
from myFlaskApp import routes
```
inside `routes.py` python module define all routes of the UI.
```
>>> routes.py
from myFlaskApp import app
@app.route('/')
def home():
   return("This is Homepage")
```

#### How to run?
When inside the top level directory `myFlaskUI/`, type `python -m flask run` or just `flask run`. <br>
For more info : `python -m flask run --help`




#### Environment variables in windows
```
set --> list of all environment variables
help set --> scroll towards the end for more variables
echo %path% or path
echo %USERNAME%, echo %cd%, echo %time%
```
How to set a new environment variable
```
set FLASK_ENV=development
echo %FLASK_ENV%
```
get windows enviroment variable from python
```
import os
os.environ ---> gives all vaiables in a dictionary
os.environ["PATH"] or os.environ.get("PATH")
os.environ.get("FLASK_ENV") ---> development
>>>> 'FLASK_ENV': 'development'
```
If you don't want to set in windows
```
set FLASK_ENV=
echo %FLASK_ENV% --> nothing
import os; os.environ.get("FLASK_ENV") --> will give nothing
os.environ["FLASK_ENV"] --> keyError
os.environ["FLASK_ENV"] = "development"
```




```
mkdir mysampleUI
virtualenv venv ---> create virtual environment
venv\Scripts\activate --> activate venv
pip freeze --> no libraries yets
where python
pip install Flask; pip freeze
Click==7.0
Flask==1.0.2
itsdangerous==1.1.0
Jinja2==2.10
MarkupSafe==1.1.1
Werkzeug==0.15.1

python myapp.py

```

```
>>> python app.py
 * Serving Flask app "app" (lazy loading)
 * Environment: development
 * Debug mode: on
 * Restarting with stat
 * Debugger is active!
 * Debugger PIN: 300-022-090
 * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
```

### Install the packages

```
pip install Flask            ----> for web api 
pip install Flask-JWT        ---> for authentication
pip install Flask-RESTful    ---> API mapping
pip install Flask-SQLAlchemy ---> easier to work with SQLAlchemy
```

### Flask Tutorial Resources
https://pythonspot.com/flask-web-app-with-python/ <br>
https://www.tutorialspoint.com/flask/ <br>
https://blog.miguelgrinberg.com/post/the-flask-mega-tutorial-part-i-hello-world/page/10 <br>
https://medium.freecodecamp.org/how-to-build-a-web-application-using-flask-and-deploy-it-to-the-cloud-3551c985e492 <br>
https://damyanon.net/post/flask-series-structure/





