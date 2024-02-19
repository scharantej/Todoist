## Flask Application Design for a Todo List Application

### HTML Files

- **index.html**: This will serve as the main interface for the todo list application. It will display a list of current tasks and provide a form to add new tasks.
- **task_form.html**: This will be a partial HTML template used to render the form for adding new tasks. It will contain the necessary input fields and a submit button.

### Routes

- **"/"**: This route will handle GET requests for the main page of the application. It will render the `index.html` template and populate it with the list of tasks retrieved from the database.
- **"/add-task"**: This route will handle POST requests for adding a new task to the database. It will receive the task's title and description from the form submission, create a new `Task` object, add it to the database, and redirect the user back to the main page.
- **"/delete-task/<int:task_id>"**: This route will handle GET requests for deleting a task from the database. It will accept the ID of the task to be deleted as a path parameter, remove the task from the database, and redirect the user back to the main page.
- **"/edit-task/<int:task_id>"**: This route will handle GET requests for editing a task's details. It will accept the ID of the task as a path parameter, retrieve the task from the database, and render a form pre-populated with the task's current details.
- **"/update-task/<int:task_id>"**: This route will handle POST requests for updating a task's details. It will accept the ID of the task as a path parameter, receive the updated details from the form submission, modify the task in the database, and redirect the user back to the main page.