TODO List Delete Assignment
-----------------------------------

Learning Outcome Addressed
-------------------------------
 9. Build an application in React
--------------------------------------------

TODO List Delete Assignment
-----------------------------

React – Delete Items
The starter code for this activity creates a todo list application. The way this todo list app works is pretty simple. Type in a task or item into the input field displayed on the browser and press Add (or hit Enter/Return). Once you've submitted your item, you'll see it appear as an entry below the input field. Go ahead and try it! Note that the list starts out with three items already added.

The X button next to each item allows you to delete items from the list, but if you try it you'll notice that it doesn't work. In this task, you'll be building out that functionality.

Your task in this activity is to implement the delete functionality that allows users to remove specific items from the list.

The starter code for this activity is included in the todo.jsx file. Add code where instructed through code comments. Here's a description of the starter code:

TodoApp is the root component. It includes the SubmitForm and TodoList components

In the TodoApp component, it defines the handleSubmit function which adds a new item to the list
Similar to the handleSubmit function, you will write a function to handle removing an item from the list
SubmitForm is the form component. This defines a text field to collect the new item for the list, and a button to add that item to the list

The code to add new items to the list is already implemented for you. You shouldn't have to update this code
TodoList is the component responsible for displaying a list of todo items. It uses the ToDo component to display each item

The code to add new items to the list is already implemented for you. You shouldn't have to update this code
Todo is the component responsible for displaying a single todo item. It includes a delete button. The onClick event of this button fires off the onDelete event with the id of that specific item

The code to add new items to the list is already implemented for you. You shouldn't have to update this code
To accomplish this task, you need to do the following:

Inside the TodoApp component, define the handleDelete function. This function takes in an index representing the item to delete.
Use splice to remove the item from the state.
Set the new state using the function setState.


Documentation on SPLICE: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice
