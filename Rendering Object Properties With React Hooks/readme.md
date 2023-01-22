Rendering Object Properties With React Hooks
--------------------------

Learning Outcomes Addressed
 1.Render object properties using JSX

 2.Destructure an object with ES6 syntax

 3.Use string interpolation to construct a string with object property values

--------------------------------------

Rendering Object Properties With React Hooks In JSX
------------------------

Rendering Object Properties With JSX
JSX is a JavaScript extension that allows you to treat HTML elements as JavaScript variables in the same file. It's used in conjunction with React to keep code intuitive and efficient by making it clear what elements on your DOM are connected to variables within the logic of your application.

In this exercise, you'll use JSX to do a few operations that you have already done using JavaScript and ES6. You'll render object properties on your page to display in the form of a constructed sentence that uses all the state object properties. The steps to achieve this include updating the state, taking those values out of the state within the render function, constructing a string, and then using the template code provided to show that string in the DOM using the React.createElement function.

Here's an exercise in which you will:

Render object properties on your page using some basic JSX
Use ES6 object deconstruction syntax
Construct a string with object property values inside using string interpolation
A file called reactIntro.jsx is provided (notice the file extension is not .js as in previous activities). This file uses the React functionality to show the string (or element) returned by the render function in the DOM.

Task Instructions
Step 1: Initialize State

First you'll need to edit the initializeState function in order to update the state with the following values:

Set the initialized field to equal the Boolean value true
Set the productName field to equal the string "Rice Krispies"
Set the productDescription field to equal the string "a cereal made of popped rice"
Set the productPrice field to equal the string "$3.00"
You'll need to update the state, which is initialized with the following code block:

let [state, setState] = useState({
  initialized: false,
  productName: null,
  productDescription: null,
  productPrice: null,
});
Use the setState function, which is initialized with React.useState. In the code block above:

state is the variable name of the state object that is accessible from anywhere in the component.
setState is a function into which you will pass an argument to replace the value of state.
You'll learn more about state next week. For now you only need to know that when changed, state is an object that triggers a re-render of a web page. An example of how to use the setState function to update the state is as follows:

setState({ initialized: true });
Note that using setState will replace whatever previous value was within the state variable with the new object. In the example above, it would be {initialized: true}.

Additionally, it's important that you follow the above syntax when setting the state, and you should not access the variable directly as below:

state = newStateVariable;
This is because the setState() function updates it in such a way that React knows to re-render the component.

Step 2: Constructing A Sentence With String Interpolation

Next, you'll use ES6 syntax in the render function. Already provided in the render function is the deconstruction of state to define the variable initialized within render. You'll deconstruct the remaining values (productName, productDescription, and productPrice) from the state object.

Finally, using the ES6 feature of string interpolation, you'll use the values from state to construct the following sentence to be stored in the stringToReturn variable.

The product name is Rice Krispies, product description is a cereal made of popped rice, and product price is $3.00.

An example of string interpolation can be seen below:

const name = "Bob", time = "today";
`Hello ${name}, how are you ${time}?
In the desired state of this activity, the page loads with a button with the text Click here to initialize your state. After clicking the button, it will be replaced by the sentence stored in the stringToReturn variable.

Hint:

This exercise can be completed using the examples provided and editing them to the specifications of the instructions.
