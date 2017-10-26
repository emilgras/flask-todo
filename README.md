# Simple Flask Todo API

This is a simple api for a todo list app. It contains basic CRUD operations and handles user authentication and authorization.
</br>
</br>

## Installation

clone the repository

```sh

$ cd to/your/favorite/path

$ git clone https://github.com/emilgras/simple-flask-auth.git

$ cd simple-flask-aut

```

create and activate a local virtual environment

```sh

$ python3 -m venv venv

$ source venv/bin/activate

```

Install dependencies from `requirements.txt`

```sh

(venv) $ pip install -r requirements.txt

```
</br>

## Running the project

Start the python interpreter and create the database

```sh

(venv) $ python

>>> from api import db

>>> db.create_all()

>>> exit()

```

(optional) Start the sqlite3 command line and verify that 2 tables has been created `user` & `todo`

```sh

(venv) $ sqlite3

>>> .tables

```

Exit the sqlite command line

```sh

>>> .exit

```
Start the application 

```sh

(venv) $ python api.py

```
</br>

## Endpoints

Authentication routes

| Method | Endpoint | Description |
| --- | --- | --- |
| POST | /login | log's in a user |
| POST | /register | creates a new user with no access token |
</br>

Admin routes

| Method | Endpoint | Description | Parameters | Result |
| --- | --- | --- | --- | --- |
| GET | /user | get all users | --- | list of users | 
| GET | /user/<public_id> | get a single user | `public_id` | single user |
| PUT | /user/<public_id> | promote user to admin | `public_id` | --- |
| DELETE | /user/<public_id> | deletes a user | `public_id` | --- |
</br>

Todo routes

| Method | Endpoint | Description | Parameters | Result |
| --- | --- | --- | --- | --- |
| GET | /todo | get all users | --- | list of todo items | 
| GET | /todo/<todo_id> | get a single todo item | `public_id` | todo item |
| PUT | /todo/<todo_id> | complete todo item | `todo_id` | --- |
| DELETE | /todo/<todo_id> | deletes todo item | `public_id` | --- |

