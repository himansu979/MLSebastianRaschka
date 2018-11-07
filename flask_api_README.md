#### About Flask API
Environment variables in windows
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
>>> python app.py
 * Serving Flask app "app" (lazy loading)
 * Environment: development
 * Debug mode: on
 * Restarting with stat
 * Debugger is active!
 * Debugger PIN: 300-022-090
 * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
```
