# Simple Flask Todo API

This is a simple api for a todo list app. It contains basic CRUD operations and handles user authentication and authorization.


#### Running the project

* `cd your/favorite/path/here`

* `git clone https://github.com/emilgras/simple-flask-auth.git`

* `cd simple-flask-auth`

* `pip install -r requirements.txt`

* In the terminal type `python` and hit enter to open the Python interpreter

* Now type `from api import db` and hit enter

* finally type `db.create_all()` hit enter

* To exit the python interpreter type `exit()` then hit enter

* (optional) 


#### Authentication

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

