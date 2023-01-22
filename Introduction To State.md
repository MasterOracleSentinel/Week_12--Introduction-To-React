Introduction To State
--------------------------

Managing data with React
React components contain a state object, which allows developers to store and keep track of data. When a component’s state changes, the component re-renders itself.

Rendering the data from state 
Suppose you created a component that displays a list of users and their user IDs in a table. In the state object, you have an array of objects called users that contains the user ID and username for all registered users.

```

state = {

 users: [ 

{ userID: 1, username: “peter.parker” }, 

{ userID: 2, username: “bruce.wayne” },

{ userID: 3, username: “t’challa” },

{ userID: 4, username: “diana.prince” },

  ]

}

```

The data from the component’s state is being used to display a table on the DOM when the component renders for the first time.


User ID     Username
1	          peter.parker
2	          bruce.wayne
3	          t’challa
4	          diana.prince

Reacting to a change in state 
React components will re-render when their state is updated in the correct way (React provides certain functions, such as setState(), to update the state in a way that lets React know to re-render the page). Suppose that a new user registered for your site. Their user ID and username are added to the users’ array inside the state. 

```

state = {

users:  [ 

{ userID: 1, username: “peter.parker” }, 

{ userID: 2, username: “bruce.wayne” },

{ userID: 3, username: “t’challa” },

{ userID: 4, username: “diana.prince” },

{ userID: 5, username: “dr.strange” }

  ]

}

```

This change causes the React lifecycle to update, re-rendering the DOM. React is declarative, which means that when the state (or data) is changed, React updates the interface accordingly.


User ID     Username
1	          peter.parker
2	          bruce.wayne
3	          t’challa
4	          diana.prince
5	          dr.strange

-------------------------------------
Tracking component-level data
-------------------------------------
Each React component has access to its own state object. If you reuse a component across an application, each component can keep track of its own data through its state object. Let’s explore an example to illustrate this concept.

Imagine that you created a counter component. The component contains a display of the count, which is stored in the component’s state object, and a button that users can press to increment the count by one. You use the counter component in two places in your application and in both instances, the counter’s state initializes at zero. 

------------------------

```         ```
state = {   state = {
  count: 0    count: 0 
}            }
```         ```

![image](https://user-images.githubusercontent.com/105542222/213900542-9f5f62b1-f34e-4afb-a504-9c37da03d2ef.png)

Using what you know about state and components, what would happen if you incremented one of the counters? 

 

If you predicted that only the counter instance that the user selected would increment, you are correct. The component’s state is internal, and multiple instances of the component do not share the same state. 

 

```         ```
state = {   state = {
  count: 0    count: 1 
}            }
```         ```

![image](https://user-images.githubusercontent.com/105542222/213900557-ee2aadbd-8ecc-4ecd-a6ca-a09e63789eca.png)

To enforce the same state between multiple components or instances of components, there are two common patterns in React: lifting the state to a common parent component or a centralized state store such as Redux that can be made available to any component. You will learn more about this in Module 16.


