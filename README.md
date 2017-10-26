# Simple Flask Todo API

This is a simple api for a todo list app. It contains basic CRUD operations and handles user authentication and authorization.
</br>

## Installation

clone the repository

```python

cd to/your/favorite/path

git clone https://github.com/emilgras/simple-flask-auth.git

cd simple-flask-aut

```

create your local virtual environment

```python

python3 -m venv venv

source venv/bin/activate

```

Install dependencies from `requirements.txt`

```python

pip install -r requirements.txt

```


## Running the project

Start the python interpreter and create the database

```python

$ python

>>> from api import db

>>> db.create_all()

>>> exit()

```

(optional) Start the sqlite3 command line and verify that 2 tables has been created `user` & `todo`

```python

$ sqlite3

>>> .tables

```

Exit the sqlite command line

```python

>>> .exit

```
Start the application 

```python

$ python api.py

```


* In the terminal type `python` and hit enter to start the Python interpreter

* Now type `from api import db` and hit enter

* finally type `db.create_all()` hit enter

* To exit the python interpreter type `exit()` then hit enter

* (optional) `sqlite3` to open up sqlite command line

* (optional) `.tables` to show a list of tables. You should see `todo` and `user` printed

* (optional) `.exit` to exit the sqlite command line

* `python api.py` to start the app. 

* Try it out using Postman or similar software
</br>


#### Authentication routes

| Method | Endpoint | Description |
| --- | --- | --- |
| POST | /login | log's in a user |
| POST | /register | creates a new user with no access token |


#### Admin routes

| Method | Endpoint | Description | Parameters | Result |
| --- | --- | --- | --- | --- |
| GET | /user | get all users | --- | list of users | 
| GET | /user/<public_id> | get a single user | `public_id` | single user |
| PUT | /user/<public_id> | promote user to admin | `public_id` | --- |
| DELETE | /user/<public_id> | deletes a user | `public_id` | --- |


#### Todo routes

| Method | Endpoint | Description | Parameters | Result |
| --- | --- | --- | --- | --- |
| GET | /todo | get all users | --- | list of todo items | 
| GET | /todo/<todo_id> | get a single todo item | `public_id` | todo item |
| PUT | /todo/<todo_id> | complete todo item | `todo_id` | --- |
| DELETE | /todo/<todo_id> | deletes todo item | `public_id` | --- |

