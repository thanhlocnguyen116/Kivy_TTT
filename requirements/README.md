# This folder contains requirements and environments files to get the Kivy app running on any machine with Python

## All the instructions below assume that you have cloned this repo and have a directory name "Kivy-Game" on your machine. It is also assumed that you are using some kind of a Terminal to carry out your appropritate instructions. And it is also assumed that you have your preferred environment manager installed on your machine (conda/pipenv/virtualenv) except if you are using venv which comes with the Standard Library

## Please try `python3` if using `python` doesn't work for your machine (most likely occurs on Mac and Linux)

## Run with a Conda environment

If you have Anaconda or Miniconda installed and you use Conda to manage your packages and virtual environments, then you can simply use the YAML file to create a new environment that has all the Kivy requirements:

* Navigate to the cloned directory.
* `conda env create -f requirements/kivy-development.yml`
* `conda activate kivy-development`
* `conda list` to see all the libraries installed to your Conda environment
* Move up to the cloned directory and run `python main.py`

## Run with Pipenv

If you use Pipenv then you can use the requirements.txt file included to run the Kivy app

* Navigate to the cloned directory
* Make a new directory named "kivy-pipenv" with `mkdir "kivy-pipenv"` and navigate to that directory.
* To create an environment in the "kivy-pipenv" directory and install Kivy and its dependencies from the requirements.txt file at once run:

**If using Command Promt**:

* `pipenv install -r ..\requirements\requirements.txt`

**If using Linux/Mac/Git Bash on Windows/WSL/or any Unix terminal**:

* `pipenv install -r ../requirements/requirements.txt`  

This directory should now contain Pipfile and Piplock files.

* Run `pipenv shell` while you are still in "kivy-pipenv" directory to activate the virtual environment
* Then move up one directory and simply run `python main.py` to run the game

## Run with Virtualenv

If you use virtualenv to manage and create your enviroments then follow these instructions

* Navigate to the cloned directory
* Run `virtualenv kivy-virtualenv` to create a new environment directory.
* Don't navigate to the new "kivy-virtualenv" directory and while still in the cloned directory, run:

**On Windows (using Command Prompt)**:

* `kivy-virtualenv\Scripts\activate`

**On Windows (using Git Bash or WSL)**:

* `source kivy-virtualenv/Scripts/activate`  (If it doesn't work, try without `source`)

**On Mac/Linux**:

* `source kivy-development/bin/activate`

Once activated, run:

**If using Command Prompt**:

* `pip install -r requirements\requirements.txt`

**If using Linux/Mac/Git Bash on Windows/WSL/or any Unix terminal**:

* `pip install -r requirements/requirements.txt` 
* Then run `python main.py` to run the game

## Run with Venv

If you don't have or use Conda or Pipenv and would like to use the env manager built-in to the Python stdlib then these are the instructions to get the game running with Venv

* Navigate to the cloned directory
* Run `python -m venv venv`. You should see a new directory in you cloned one named "venv". By convention, the environment you want to create with Venv should be named "venv".
* Don't navigate to the "venv" directory and while still in the cloned directory run the following to activate the envrionment:

**On Windows (using Command Prompt)**:

* `venv\Scripts\activate.bat`

**On Windows (using Git Bash or WSL)**:

* `venv/Scripts/activate.bat`

**On Mac/Linux**:

* `source venv/bin/activate`

Once activated, run the following to get Kivy and its dependencies:

**If using Command Prompt**:

* `pip install -r requirements\requirements.txt`

**If using Linux/Mac/Git Bash on Windows/WSL/or any Unix terminal**:

* `pip install -r requirements/requirements.txt`

* Lastly, run `python main.py` to run the game.