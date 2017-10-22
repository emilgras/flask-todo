# Simple Flask Todo API

This is a simple api for a todo list app. It contains basic CRUD operations and handles user authentication and authorization.


#### Running the project

* `cd your/favorite/path/here`

* `git clone `


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

