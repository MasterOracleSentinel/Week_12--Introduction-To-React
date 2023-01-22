Destructuring allows you to unpack values from arrays or properties from objects and assign them to different variables.

Assigning Properties Without Destructuring
Review the example that assigns an object’s properties without destructuring below.

Imagine you have an object called product containing three properties: name, cost, and inStock.

let product = {name: 'pear', cost: 2, inStock: 7};
Now suppose you create two new variables, one for the product’s name property and the other for the product’s inStock property.

Without destructuring, you would handle it like this:

let name = product.name;
let inStock = product.inStock;
Assigning Properties With Destructuring
With destructuring, you can assign the properties with just one line of code.

Start by creating a new variable with let, var, or const. Instead of adding a single variable name, you can add multiple variable names inside curly brackets.

let { name, inStock } = product;
This tells JavaScript to create a variable called name and assign it to the property inside of product called name. It also tells JavaScript to create a variable called inStock and assign it to the property inside of product called inStock.

If you print those variables to the console, you will see the data.

console.log(name);    // 'pear'
console.log(inStock); // 7
It’s important to know that the name inside the curly brackets must match the property name inside the object you are looking at. So, for example, if you use the same code above but add another variable called ordered, it will look like this:

let { name, inStock, ordered } = product;
The variable ordered would be undefined because there is no property called ordered inside the product object.

Destructuring allows you to save time by writing less code. While you only saw how to use destructuring with an object in this example, you can also use it with arrays and function parameters.

Review:

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment

to see all the different ways you can use destructuring and their corresponding examples.
