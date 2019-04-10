# Starting The Server

<p align="center">
  <img width="600" src="https://raw.githubusercontent.com/OkkarMin/CMSAPI.github.io/master/docs/static/StartingTheServer.svg?sanitize=true">
</p>

Before starting the server there are two dependencies required
1. [Python3.7.X](https://www.python.org/downloads/) 
2. [Pipenv](https://pipenv.readthedocs.io/en/latest/#install-pipenv-today)

## Clone The Repository

!> Currently our project is in PRIVATE mode. Only allowed contributers are able to clone the repo. To request for access please email cms3003@gmail.com

```bash
git clone https://github.com/jwngo/CMS3003.git
```

After it has been cloned

```bash
cd CMS3003
```

Install all python dependencies from Pipfile

!> [Pipenv](https://pipenv.readthedocs.io/en/latest/#install-pipenv-today) need to be installed globally

```bash
pipenv install
```

## Starting Localhost

To run the server on localhost

```bash
pipenv shell
cd cms
python manage.py runserver
```

Go to [localhost:8000](http://localhost:8000) in browser of your choice

## Copy Pasta

```bash
git clone https://github.com/jwngo/CMS3003.git
cd CMS3003
pipenv install
pipenv shell
cd cms
python manage.py runserver
```
