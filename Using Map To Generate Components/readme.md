Using Map To Generate Components
-------------------------------------

Whenever you have to create an unknown number of similar components based on an array, you use the JavaScript .map() method.

Imagine you have a screen, and it's your job to build a table that will list every product your company sells. Each row in that table will be its own component and display the same information about each product, its name, and its cost. Thus, you create a function that gets an array containing every product from the company's database, and now you have to display that in your table. Here are two possible methods.

One option would be to hard code the same number of row components as there are products in the database, so if there are ten products in the database, you will create ten components. This is a terrible practice for two reasons:

1. If you ever want to change how the row looks or what information is displayed, you’ll need to edit every row component.
2. Your code will break if you add new products to the database. You’ll have to update the code every time the number of products changes.


The other option, the .map() method, is much better. Using .map() works well because you can loop through each product and generate a new component unique to each one. Any edits you make have to be done in only one place.

--------------------------

Review this article to see more examples about how

https://dev.to/britneys/creating-reusable-react-components-with-map-4823

creating React components with map() 
can save time and a lot of code
