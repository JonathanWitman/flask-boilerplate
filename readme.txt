1. make directory
2. ```git init```
3. get git ignore file
4. get setup.py file *a command for regular dependencies and dev dependencies
   ```
   extras_require={
       'test': [
           'pytest',
           'coverage',
       ],
   },
   ```
5. make venv ```python3 -m venv venv```
6. activate venv ```source venv/bin/activate```
7. make sure you're in env ```which python```
8. install required dependencies ```pip install -e .```
9. install developer dependencies ``` pip install -e '.[test]' ```
10. ```mkdir flask_boilerplate```
11. make flask_boilerplate/__init__.py file
```
from flask import Flask

def create_app():
    app = Flask(__name__)

    @app.route('/')
    def index():
        return 'Hello World!'

    return app
```
11. export FLASK_APP=flask_boilerplate
12. echo $FLASK_APP
13. ```flask run```
