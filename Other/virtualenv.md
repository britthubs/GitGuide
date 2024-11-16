# Virtual environments (python3)
## Creating a virtual environment
Make sure that you're situated at the location where you want the environment to be 
(use ```cd pathofdirectory``` to do so). Typing the following command in a terminal creates a virtual environment:
```
python -m venv nameofenv
```
'nameofenv' refers to the name you want to give your virtual environment, edit this to the name you want it to be.
## Activating a virtual environment
To activate a virtual environment you need the path to the folder of the environment, for example: /users/burrito/myenvironment.
In the command, you add /bin/activate to this path. The command to activate the virtual environment in this example is the folowing:
```
source /users/burrito/myenvironment/bin/activate
```
The name of the environment should now show at the following line in your terminal in between brackets, for example (myenvironment).
## Deactivating a virtual environment
To deactivate the currently active environment, following command can be used:
```
deactivate
```
## Listing the packages already installed in the environment
To list the already installed packages in your environment, the following command can be used while the virtual environment is activated:
```
pip freeze --local
```
or
```
pip list --local
```
An empty environment will have something like the following output after calling the command:
```
Package    Version
---------- ------- 
pip        19.2.3 
setuptools 41.2.0
```
