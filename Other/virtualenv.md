# Virtual environments (python3)
## Making a virtual environment
Make sure to be situated at the place where you want the environment to be 
(use ```cd pathofdirectory``` to do so). Typing the following command in a terminal creates a virtual environment:
```py 
python -m venv nameofenv
```
'nameofenv' refers to the name you want to give your virtual environment, edit this to the name you want it to be.
## Starting a virtual environment
To start a virtual environment you need the path to the folder of the environment, for example: /users/burrito/myenvironment.
In the command, you add /bin/activate to this path. The command to start the virtual environment in this example is the folowing:
```py
source /users/burrito/myenvironment/bin/activate
```
The name of the environment should now show at the following line in your terminal in between brackets, for example (myenvironment).
