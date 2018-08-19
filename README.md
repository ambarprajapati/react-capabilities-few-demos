# react-capabilities-few-demos
## Demonstrating React Capabilities
#### by Ambar Prajapati

This repository demonstrates the use of  
1. React Components with `props` and `state` and utilize Javascript Object Array, 
2. Use `Redux` with `React`
3. Use `thunk` , `super-agent` to access asynchronous logic in `Redux` and `React`


### Objective Demo-1: Demonstrate making React Components with `props` and `state` and utilize Javascript Object Array
#### Level: Simple
<img src="https://github.com/ambarprajapati/react-capabilities-few-demos/blob/master/image1.jpg" />

In the following Demonstration, we break down the process of building a to-do list. The to-do list is capable of creating, deleting, updating and completing tasks. 

A task is an object with these properties: `id`, `title`, `description`, and `completed`.

The to-do list is created  using `create-react-app` and accomplishes functionlity as described below. All the functionality is available to the user on the same view.

### Functionality in detail:

* A user must be able to create a task.
  * A user must not be able to create a task with no title.
* A user must be able to delete a task.
* A user must be able to complete a task.
  * A user must be able to see a visual representation of a completed task.
  * The complete button should be disabled if the task is completed.
* A user must be able to see a list of all their tasks.
* The `add-task` input field must clear after adding a task.
* After adding a new task, the task must be added to the list of visible `tasks`.

### Used: React and Javascript array data-structure 

* Created a react app from scratch using `create-react-app`.
* Components.
* State.
* Props.
* <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map?v=example">Map</a>.
* Classes ( at least 1 )
* In-line styles ( at least 1 )
* Conditional Classes


### Objective Demo-2: Demonstrate using `Redux` with `React`
#### Level: Moderate

<img src="https://github.com/ambarprajapati/react-capabilities-few-demos/blob/master/image2.jpg" />

In the following Demonstration, we use the repository made in demo-one and modify the logic to use Redux 

### Functionality

* To-do list with all functionality achieved in demo-one

### React and Redux Capabilities utilized

* Tasks in the to-do list are now tracked using redux.
* The action creators with redux handle Create, Complete, and Delete tasks.

### Objective Demo-3: Demonstrate using `thunk` , `super-agent` to access asynchronous logic in `Redux` and `React`
#### Level: Advanced

<img src="https://github.com/ambarprajapati/react-capabilities-few-demos/blob/master/image3v3.jpg" />

Perform CRUD operation over http on the API given below:

<details>

<summary> ## API for CRUD operations </summary>

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

In this demo- utilize all functionality and properties of a task namely :  `id`, `title`, `description`, `completed`.



### Functionality

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


### Capabilities utilized: `thunk` , `super-agent` , `Redux` with `React`, `Material-UI`

* Use Material-UI (Current Version) for user interface components
* Use the API to manage tasks.
* Use `redux-thunk`, `Redux`, and `super-agent` to create, fetch, update, complete, and delete tasks.
* Use `react-router-dom` to create a new route to a detailed view of a task:
  * This route should use route parameters to know which task it is working with.
  * This route should be able to handle refreshing ( data should not be lost on refresh ).
