# react-capabilities-few-demos
#### by Ambar Prajapati
[Note: Current css shall be replaced with a better one soon.]
### Demo-1:
#### Build single view app containing `nested react component hierarchy` using state, props, javascript array methods, and conditional styles

> In this demo, we create a single-view To-Do list app. The to-do list is capable of creating, deleting, updating and completing tasks. 
> 
> A task in To-do list is an object with properties: `id`, `title`, `description`, and `completed`.
> 

#### Functional Objectives:

* A user must be able to create a task.
  * A user must not be able to create a task with no title.
* A user must be able to delete a task.
* A user must be able to complete a task.
  * A user must be able to see a visual representation of a completed task.
  * The complete button should be disabled if the task is completed.
* A user must be able to see a list of all their tasks.
* The `add-task` input field must clear after adding a task.
* After adding a new task, the task must be added to the list of visible `tasks`.

#### Technical Objectives:

* Create a react app from scratch using `create-react-app`.
* Components.
* State.
* Props.
* <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map?v=example">Map</a>.
* Classes ( at least 1 )
* In-line styles ( at least 1 )
* Conditional Classes

#### Screenshot:
<kbd>
<img src="https://github.com/ambarprajapati/react-capabilities-few-demos/blob/master/todo1.jpg"/>
</kbd>

### Demo-2: 
#### Redux: Implement `Redux : Actions, Reducers, Components and Dispatchers`

> In this demo, we use the repository made in demo-one and modify the logic to use Redux - Actions, Reducers, Components and Dispatchers

#### Functional Objectives:

* To-do list with all functionality achieved in demo-one

#### Technical Objectives:

* Tasks in the to-do list are now tracked using `redux`.
* The action creators with redux handle Create, Complete, and Delete tasks.

#### Screenshot:
<kbd>
<img src="https://github.com/ambarprajapati/react-capabilities-few-demos/blob/master/todo2.jpg" />
</kbd>

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
  
  
### A quick note on using `redux-thunk` over `redux-saga`

`redux-thunks` may be quickly implemented for async API server calls. They are intuitive and time tested. `redux-thunks` are flexible for all use-cases, supported in official docs and _one size fits all_ kind of remedy.

However excessive and un-mindful use of `redux-thunks` may quickly lead a solution into *callback hell* and render an application completely - unmanageable.

`redux-sagas` solve the -callback hell- problem of thunks. Sagas use declarative style and go beyond - components, reducers and actions. They make a complex async logic look simpler, more transactional  and make unit testing easy.
