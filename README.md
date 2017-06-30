# ToDoApp_MEANStack

Functionality: 
- tasks are stored inside an array field "list" and each task
  is a document with an id created by code. The id is generated using
  getTime() function because this returns milliseconds, this way
  the id is unique (because tasks are deleted by id this was important)

- tasks also contain an optional "date" field. Tasks display as follows:
	* if the task is due that same day, it will show in red
	* if the task is due in one or two days, it will show yellow
	* otherwise, it will show in black

- encrypts password and stores encrypted password only

- when user logs on, queries database to make sure username/password match
  if mismatch, prompts user without popups

- when user registers, queries database and checks if the username matches first, 
  then it checks if the password matches, this way it can notify the user which
  one needs modification

- session management was successfully executed, so you cannot access information after
  logging out through URL or back button (back button had to be handled separately)

- collection is only loaded until after user successfully signs in. This is because
  not the entire collection is loaded, only the collection of the particular user
  who is active
