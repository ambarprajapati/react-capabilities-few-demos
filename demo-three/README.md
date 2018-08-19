### Demo-3:
#### `Asynchronous thunks with REST API`: 
#### Implement asynchronous REST API using `thunk` , `super-agent` , `Redux` and `React`. Implement dynamic routing, using `react-route`.

> * Re-design view using Material UI
> * Use redux for handling API-store
> * Implement all functionality and properties of a task namely :  `id`, `title`, `description`, `completed`.
> * Perform CRUD operation over http on the API given below

<details>

<summary> REST API for CRUD operations (click to expand)</summary>

<br />

* GET - `https://practiceapi.devmountain.com/api/tasks`
  * Returns an array of all tasks.
* POST - `https://practiceapi.devmountain.com/api/tasks`
  * Creates a new task.
  * Requires a `title` property on the request body that equals a string.
  * Returns an array of all tasks.
* PATCH - `https://practiceapi.devmountain.com/api/tasks/:id`
  * Updates a task.
  * Requires an id parameter of the task you want to patch.
  * Requires a request body with a property or properties you want to update.
    * Valid properties: `title` - string, `description` - string, `completed` - boolean
  * Returns an array of all tasks.
* DELETE - `https://practiceapi.devmountain.com/api/tasks/:id`
  * Deletes a task.
  * Requires an id parameter of the task you want to delete.
  * Returns an array of all tasks.
* PUT - `https://practiceapi.devmountain.com/api/tasks/:id`
  * Marks a task as completed.
  * Requires an id parameter of the task you want to complete.
  * Returns an array of all tasks.

</details>
<br />

#### Functional Objectives:

* A user should be able to click on a task to be taken to a detailed view of that task:
  * A user should be able to modify the title of a task.
  * A user should be able to add/modify the description of a task.
  * A user should be able to save changes to a title/description:
    * This should navigate the user to the main list of tasks after saving changes.
  * A user should be able to cancel text changes:
    * This should set the input fields' values back to their original value.
  * A user should be able to delete a task:
    * This should navigate the user back to the main list of tasks after deleting a task.
  * A user should be able to complete a task:
    * This should navigate a user back to the main list of tasks after completeing a task.
* A user should be able to click on a link to be taken back to the main list of tasks from the detailed view.

#### Technical Objectives:

* Use `Material-UI` (Current Version) for user interface components
* Use the API to manage tasks.
* Use `redux-thunk`, `Redux`, and `super-agent` to create, fetch, update, complete, and delete tasks.
* Use `react-router-dom` to create a new route to a detailed view of a task:
  * This route should use route parameters to know which task it is working with.
  * This route should be able to handle refreshing ( data should not be lost on refresh ).

#### Screenshot:  
  <img src="https://github.com/ambarprajapati/react-capabilities-few-demos/blob/master/todo3.jpg" />

### Other notes:

* integrates with given api and works to create, fetch, update, complete, and delete tasks from server instantly.
* uses current Material UI.
* double click on a to-do task enables editing of that task.
* hitting enter commits save or edit.
* clicking a row on main-task-list opens up a Task-Detail View.
* User can modify or delete a title in Task-Detail View. After modify or delete, user navigates to main-task-list. 
* User can use `Toggle Complete` button on the main task list and Task-Detail view to mark a Task complete and incomplete
* `Cancel` and `Back to Tasks` button navigates user back to main-task-list.

#### Ambar Prajapati
