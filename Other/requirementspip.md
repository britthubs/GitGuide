# Making a requirements.txt file (for python and pip)

## What?
A requirements.txt file contains a list of the libraries, packages and other dependencies used in your project, as well as the versions of each dependecy. 
In this case it's only used for python and pip.

## Why?
Those who want to download your project (or if you are coming back to the project) will want to also download the dependencies 
and their respective versions that were used for the project which are not automatically included. Installing each seperately can be time-consuming. If you make a requirements.txt
file, the only thing the other person (or future you) has to do is activate an environment and install the requirements.txt file.

If the environemnt hasn't been created yet, you can check out [this guide](/Other/virtualenv.md) on how to create and activate virtual environments (python3).

Finally, to install the dependencies with the requirements.txt file, write following command in the terminal:

```pip install -r requirements.txt```


## How? 
1. Make sure to activate your project environement (python) before making the requirements.txt file, if you haven't made one yet, make one and activate it. (See [this guide](/Other/virtualenv.md) for explanation)
2. Before making the requirements.txt file, make sure to find the right location for it. This file should be in the directory of your project.
3. To make the requirements.txt file, type the following in the terminal (at the right location):
  
   ```pip freeze > requirements.txt```

## An example of a requirements.txt file
An example of what the file looks like can be seen here:

```txt
MouseInfo==0.1.3
PyAutoGUI==0.9.53
PyGetWindow==0.0.9
PyMsgBox==1.0.9
pyperclip==1.8.2
PyRect==0.2.0
PyScreeze==0.1.28
python3-xlib==0.15
pytweening==1.0.4
```
The lay-out is: package_name==version
