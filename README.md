# Simple Flask Todo API

This is a simple api for a todo list app. It contains basic CRUD operations and handles user authorization.

| Method | Endpoint | Description | Parameters | Result |
| --- | --- | --- | --- | --- |
| GET | /user | get all users | --- | list of users | 
| GET | /user/<public_id> | get a single user | `public_id` | single user |
| GET | /user/<public_id> | promote user to admin | `public_id` | --- |
| GET | /user/<public_id> | deletes a user | `public_id` | --- |

