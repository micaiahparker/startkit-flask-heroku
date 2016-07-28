# Getting Started With Flask/Heroku

First make sure that [Python](https://python.org), [Heroku Toolbelt](https://toolbelt.heroku.com), and [git](https://git-scm.com) are installed on your machine.

This tutorial assumes Python 3.5.1 will be used. If you are using a different version of Python edit the `runtime.txt` file from this project repo. Be sure to check if your version is [supported by](https://devcenter.heroku.com/articles/python-runtimes) Heroku.

Create the project repo folder.

```
mkdir <your-app-title>
cd <your-app-title>
git init
```

Log into Heroku and create app.

```
heroku login
heroku create <your-app-title> --buildpack heroku/python
```

Pull the starting files from this repo.

```
git pull https://micaiahparker/starkit-flask-heroku.git
git add .
git commit -m "init"
git push heroku master
```

If everything worked properly then you should be able to go to `https://<your-app-title>.herokuapp.com` and see Hello, World!

For further development you will want to create a Python virtual environment and install the project requirements. 


`python -m venv <virtual-env>`

Linux/OSX: `bash <virtual-env>/scripts/activate.sh`

Windows: `<virtual-env>\Scripts\activate.bat`

`pip install -r requirements.txt`

Afterwards add your virtual environment to the `.gitignore`.

Anytime you add a new Python package be sure to install it from your virtual environment and update your `requirements.txt` with:

`pip freeze > requirements.txt`

For local testing run:

Linux/OSX: `heroku local`

Windows: `heroku local -f Procfile.windows`




