JSX Introduction
-----------------------

What Is JSX?
---------------------
https://reactjs.org/docs/introducing-jsx.html JSX 
------------------------------------
is a JavaScript syntax extension that allows HTML-like code to be written in JavaScript. With JSX, you can put HTML-like syntax inside of JavaScript code to render an HTML element and give it functionality.

Unlike Angular and Vue, which use HTML templates, React uses JSX to combine the UI code and logic in one place.

Introduction To JSX Syntax
Review the example of JSX below:

const title = 'Hello World';

const element = <h1>{title}</h1>;
Notice how the <h1> elements and reference to the title variable are assigned to the element variable. In this example of JSX, the HTML elements are assigned to a JavaScript variable.

If the element variable was rendered by React, the web page would display the text “Hello World” in h1 (header) tags.
