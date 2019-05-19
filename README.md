# Hello World Python Web App
This is my first app developing in Python and Flask. Aiding in this journey there is also Visual Studio Code.

## How to run
Download source code and run the following commands from the project root folder:

1. Create virtual environment
   `python3 -m venv env`
2. Install required modules
   `pip3 install -r requirements.txt`
3. Run application
   `python3 -m flask run`
Please note that running like this will tell Flask that it is in a production environment. You can change this behavior by setting the environment variable `FLASK_ENV` first like bellow:
```
FLASK_ENV=development python3 -m flask run
```

## Debugging
Here follow instructions for debugging with VS Code:
1.  Open VS Code into project root folder, press Ctrl+Shift+P and select `Debug: Open launch.json`
2.  Add the following config:
```javascript
        {
            "name": "Python: Flask",
            "type": "python",
            "request": "launch",
            "module": "flask",
            "env": {
                "FLASK_APP": "app.py",
                "FLASK_ENV": "development",
                "FLASK_DEBUG": "0"
            },
            "args": [
                "run",
                "--no-debugger",
                "--no-reload"
            ],
            "jinja": true
        }
```
