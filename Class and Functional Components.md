Class and Functional Components
-----------------------------

In React, there are two types of components: class and functional.

Class components came before functional components, and you will find most projects and tutorials use functional components.

The concepts in this lesson are explained in detail in the official React documentation. Reading this documentation is strongly recommended.



Components and Props
https://reactjs.org/docs/components-and-props.html

State and Lifecycle
https://reactjs.org/docs/state-and-lifecycle.html

Introducing Hooks
https://reactjs.org/docs/hooks-intro.html

Hooks at a Glance
https://reactjs.org/docs/hooks-overview.html

Using the State Hook
https://reactjs.org/docs/hooks-state.html

Using the Effect Hook
https://reactjs.org/docs/hooks-effect.html

Class and Functional Component Examples
To start, here are simple examples of each type of component.

Both are used the same way <Welcome name="Pierre" /> and render the same HTML <h1>Hello, Pierre</h1>.

Class Component Example**
import React from 'react';

class Welcome extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
Functional Component Example
import React from 'react';

const Welcome = (props) => {

  return <h1>Hello, {props.name}</h1>;

};
Class vs. Functional Components
There are key differences between class components and functional components.

Class components are typically used in conjunction with lifecycle methods, whereas functional components are used with hooks.
Class components use a render function, where functional components return the JSX directly.
Class components access props via this, where functional components access props via the components argument, which also supports object destructuring.
To define class components, you use the class keyword, where functional components use a JavaScript function and arrow function syntax is also supported.
Here is some documentation if you'd like to learn more on the topic.

REactComponents: https://reactjs.org/docs/react-component.html

Six REasons to use Hooks :  https://blog.bitsrc.io/6-reasons-to-use-react-hooks-instead-of-classes-7e3ee745fe04

State — Set Initial Values
In the first example, we showed off using props to display "Hello, Pierre", but now we embed the name via state into the component. Now you use the component without specifying a prop and receive the same results <Welcome />, which render the HTML <h1>Hello, Pierre</h1>.

State in Class Component
class Welcome extends React.Component {
  constructor(props) {
    super(props);
    // Set an initial value 
    this.state = {
      name: 'Pierre'
    };
  }

  render() {
    return (
      <div>
        <h1>Hello, {this.state.name}</h1>
      </div>
    );
  }
}
State in Functional Component
import React, { useState } from 'react';

const [count, setCount] = useState(0);

function Welcome() {
  // Set an initial value
  const [name, setName] = useState('Pierre');

  return <h1>Hello, {name}</h1>;
}
State — Change Values
Now that we have set initial values, how can those?

This example is simple as there isn't much value in changing a static value to another static value, but this is the foundation to completing much more valuable operations. For example, we can use the techniques displayed here to display a placeholder name, such as "Name", and then fetch the user's name from an API and display it.

Update State in Class Component
class Welcome extends React.Component {
  constructor(props) {
    super(props);
    // Set an initial value 
    this.state = {
      name: 'Pierre'
    };
  }

  // Change the initial value on render
  componentDidMount() {
    this.state.name = 'Sidney'
  }

  render() {
    return (
      <div>
        <h1>Hello, {this.state.name}</h1>
      </div>
    );
  }
}
Update State in Functional Component
import React, { useState } from 'react';

const [count, setCount] = useState(0);

const Welcome = (props) => {

  return <h1>Hello, {props.name}</h1>;

};

function Welcome() {

  // Set an initial value

  const [name, setName] = useState('Pierre');

  // Change the initial value on render

  useEffect(() => {

    setName('Sidney');

  }, []);

  return <h1>Hello, {name}</h1>;

}
You will see both functional and class components in this module. On the next page, you will see an example of a functional component and practice using React hooks.

