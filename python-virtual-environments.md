## Virtual Enviroments in Python
#### Isolates Python and dependency versions for a project. We will use ```pipenv``` to manage virtual environments.

#### Steps
- cd into directory for the project
- ```pipenv install```
    - creates a ```Pipfile``` and ```Pipfile.lock```
- ```pipenv shell``` 
    - opens a shell specific to the project using the ```Pipfile```
- ```pipenv install <package>```
    - adds a dependency to your virtual environment and updates the Pipfile
- ```exit```
    - takes you out of the virtual environment

