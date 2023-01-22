Introduction To Component-Based Design
-------------------------------------------

Before you create a React component, it’s important to understand component-based design. 

What Is Component-Based Design?
Component-based design is not unique to React; many frameworks utilize this concept. But what is it? It is helpful to understand component-based design through the analogy of toy building blocks.


![image](https://user-images.githubusercontent.com/105542222/213900375-0ba3c15c-2df6-4826-959a-17d5562b9682.png)

https://www.stockvault.net/photo/131051/lego-toys

“Lego Toys” by Katherine Sparrow licensed under CC0
---------------------------

Suppose you are asked to build a model house. After completing this task, you are asked to build a model car. You can build a house with the toy build blocks, take it apart, and use those same blocks to build the car. This is similar to component-based design, where you can build an application out of components that can be reused in different ways. If you had built the model house out of wood, glue, and nails, you would not be able to repurpose those materials to build the car.

With component-based design, you can build small pieces of functionality, test them, and reuse what you create. Instead of building your web app in one file with thousands of lines of code, you can separate those lines of code into smaller files that are easier to read and maintain. This is the start of separation of concerns.

Separation Of Concerns
While separating your code from one file to multiple files is part of separation of concerns, it is only the start. The point of separation of concerns is to divide your codebase by functionality.

In the context of component-based design, the user interface (UI) and data of each piece of functionality are separate from one another. Instead of writing a log-in page with a form, navigation bar, and page footer, each of those elements would be separate components in separate files. Separating these components ensures that the data is only shared with the piece of functionality that is relevant to that data. In addition, separating the components makes maintenance easier. If you needed to update the navigation bar, you would not have to modify the log-in form or the page footer.

When working in the industry or reading online, you may come across the term “spaghetti code.” Spaghetti code reflects a bad practice, in which functionality is tightly coupled between multiple parts of your application, making it hard to read and maintain. If you design your applications with separation of concerns and employ component-based design, you will not fall into the trap of spaghetti code.

-------------------------------------------------

