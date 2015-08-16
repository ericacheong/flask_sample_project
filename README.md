# Flask sample project structure

This project is a sample flask project structure. A script to switch between development and production modes is available.

## Features
- Separate views and models
- Use of instance folder to hold sensitive data
- Three config modes are available: default, development, production

## File structure
```
\sample
    \config
        __init__.py
        default.py
        development.py
        production.py
    \instance
        config.py
    \sample
        \static
            style.css
        \templates
            index.html
            layout.html
            login.html
        __init__.py
        models.py
        views.py
    .gitignore
    README.md
    runserver.py
    start.sh
```

## Setup
1. Clone the project
2. Change the two folder names from 'sample' to 'yourappname'
3. Change 'from sample import app' to 'from yourappname import app' in runserver.py
4. Change 'import sample.views' to 'import yourappname.views' in \yourappname\yourappname\views.py
5. Change the SECRET_KEY in instance/config.py
6. Add 'instance\' to .gitignore to exclude config.py from version control

## Usage
1. Change the APP_CONFIG_FILE variable to the correct absolute path of config file in your system (default.py or development.py or production.py)
2. Chmod and make start.sh executable
```
$ chmod a+x start.sh
```
3. Run start.sh
```
$ ./start.sh
```

## Language
- Python

## Platform
- Linux

## Reference
1. https://exploreflask.com/organizing.html
2. http://flask.pocoo.org/docs/0.10/config/