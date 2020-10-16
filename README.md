# React Questions & Answers

## General React – Questions

1. ### What is React?

* React is an **open-source frontend JavaScript library** developed by Facebook in 2011 which is used for building user interfaces         especially for single page applications. <br>
* It is used for handling view layer for web and mobile apps. <br>
* React was created by [Jordan Walke](https://github.com/jordwalke), a software engineer working for Facebook.<br> 
* React was first deployed on Facebook's News Feed in 2011 and on Instagram in 2012.<br>
* It follows the component based approach which helps in building reusable UI components.<br>
* It is used for developing complex and interactive web and mobile UI.<br>

2. ### What are the features of React? 

* It uses the virtual DOM instead of the real DOM.<br>
* It uses server-side rendering.<br>
* It follows uni-directional data flow or data binding.<br>
* Uses reusable/composable UI components to develop the view.<br>

3. ### Differentiate between Real DOM and Virtual DOM.

      <table>
        <tr style="bgcolor : blue">
          <th>Real DOM</th>
          <th>Virtual  DOM</th>
        </tr>
        <tr>
          <td>1. It updates slow.</td>
          <td>1. It updates faster.</td>
        </tr>
        <tr>
          <td>2. DOM manipulation is very expensive.</td>
          <td>2. DOM manipulation is very easy.</td>
        </tr>
        <tr>
            <td>3. Can directly update HTML.</td>
            <td>3. Can’t directly update HTML.</td>
        </tr>
        <tr>
            <td>4. Creates a new DOM if element updates.</td>
            <td>4. Updates the JSX if element updates.</td>
        </tr>
        <tr>
            <td>5. Too much of memory wastage.</td>
            <td>5. No memory wastage.</td>
        </tr>
      </table>

4. ### List some of the major advantages of React.

* It increases the application’s performance.
* It can be conveniently used on the client as well as server side.
* Because of JSX, code’s readability increases.
* React is easy to integrate with other frameworks like Meteor, Angular, etc.
* Using React, writing UI test cases become extremely easy.
* Boost community base.

5. ### What are the limitations of React?
* React is just a view library, not a full framework.
* Its library is very large and takes time to understand.
* It can be little difficult for the novice programmers to understand.
* Integrating React into a traditional MVC framework requires some additional configuration.
* Coding gets complex as it uses inline templating and JSX.
* Too many smaller components leading to over engineering or boilerplate.

6. ### What is JSX?
* JSX stands for JavaScript XML.
* JSX allows us to write HTML in React.
* This is a type of file used by React which utilizes the expressiveness of JavaScript along with HTML like template syntax.
* This makes the HTML file really easy to understand.
* This file makes applications robust and boosts its performance.

    In the example below text inside `<h1>` tag return as JavaScript function to the render function.
    
    ```jsx harmony
    class App extends React.Component {
      render() {
        return(
          <div>
            <h1>{'Welcome to React world!'}</h1>
          </div>
        )
      }
    }
    ```
7. ### Why can’t browsers read JSX?
* Browsers can only read JavaScript objects but JSX is not a regular JavaScript object. so, browsers can't understand JSX code.
  Thus to enable a browser to read JSX, first, we need to transform JSX file into a JavaScript object using JSX transformers like Babel   and then pass it to the browser.The most widely used transpiler right now is Babel.

8. ### How is React different from Angular?

      <table>
        <tr style="bgcolor : blue">
          <th>TOPIC</th>
          <th>REACT</th>
          <th>ANGULAR</th>
        </tr>
        <tr>
          <td>1. ARCHITECTURE</td>
          <td>Only the View of MVC</td>
          <td>Complete MVC</td>
        </tr>
        <tr>
          <td>2. DOM</td>
          <td>Uses virtual DOM</td>
          <td>Uses real DOM</td>
        </tr>
        <tr>
           <td>3. DATA BINDING</td>
           <td>One-way data binding</td>
           <td>Two-way data binding</td>
        </tr>
        <tr>
          <td>4. RENDERING</td>
          <td>Server-side rendering</td>
          <td>Client-side rendering</td>
        </tr>
        <tr>
           <td>5. DEBUGGING</td>
           <td>Compile time debugging</td>
           <td>Runtime debugging</td>
        </tr>
        <tr>
           <td>6. AUTHOR</td>
           <td>Facebook</td>
           <td>Google</td>
        </tr>
      </table>


      React Components – React Questions


9. ### What do you understand from “In React, everything is a component.”

* Components are like functions that return HTML elements.<br>
* Components are the building blocks of a React application’s UI.<br>
* These components split up the entire UI into small independent and reusable pieces.<br>
* Then it renders each of these components independent of each other without affecting the rest of the UI.<br>

     Components come in two types, Class components and Function components

10. ### How to create components in React?

  #### There are two possible ways to create a component.	

#### Function Components: 

* This is the simplest way to create a component.<br>
* We can create a function that takes props(properties) as input and returns what should be rendered.<br>
* Function components are those components which don’t have any state at all, which means you can’t use this.setState inside these components.<br>
* It is like a normal function with no render method. It has no lifecycle, so it is not possible to use lifecycle methods such as componentDidMount and other hooks.<br> 
* When react renders our stateless component, all that it needs to do is just call the stateless component and pass down the props.
The functional component is also known as a stateless component because they do not hold or manage state.<br>

```jsx harmony
function Greeting({ message }) {
  return <h1>{`Hello, ${message}`}</h1>

}
```

#### Class Components: 

* You can also use ES6 class to define a component.<br>
* A class component requires you to extend from React.Component and create a render function which returns a React element.<br>
* The class component is also known as a stateful component because they can hold or manage local state.<br>
* You can pass data from one class to other class components.<br> 
* You can create a class by defining a class that extends Component and has a render function.<br> 
* All lifecycle hooks are coming from the React.Component which you extend from in class components.So if you need lifecycle hooks you should probably use a class component.<br>
 Valid class component is shown in the below example.<br>

```jsx harmony
class Greeting extends React.Component {
  render() {
    return <h1>{`Hello, ${this.props.message}`}</h1>
  }
}
```

11. ### There are some other key differences between these 2 components.

A * stateless component * is usually associated with how a concept is presented to the user.It is similar to a function in that, it takes an input (props) and returns the output (react element).<br> 

A * stateful component * is always a class component.It is created by extending the React.Component class.A stateful component is dependent on it’s state object and can change it’s own state.The state gets initialized in the constructor. The component re-renders based on changes to it’s state, and may pass down properties of it’s state to child components as properties on a props object.<br>

#### When would you use a stateless component??
1. When you just need to present the props.<br>
2. When you don’t need a state, or any internal variables.<br>
3. When creating element does not need to be interactive.<br>
4. When you want reusable code.<br>

#### When would you use a stateful component?
1. When building element that accepts user input.<br>
2. ..or element that is interactive on page.<br>
3. When dependent on state for rendering, such as, fetching data before rendering.<br>
4. When dependent on any data that cannot be passed down as props.<br>

#### Functional Component(Stateless)

```jsx harmony
import React from 'react';
 
function StateLessExample(props) {
 
    return(
 
        <div>
 
        <p>{props.first_name}</p>
 
        <p>{props.last_name}</p>
 
        </div>
 
    )
 
}
export default StateLessExample;
```

#### Class Component(Stateful)

```jsx harmony
import React, { Component } from 'react';
 
class StateLessExample extends Component {
 
   constructor(){
 
       super();
 
       this.state={
 
           first_name: 'Sagar',
 
           last_name: 'Ramoliya'
 
       }
 
   }
 
   render(){
 
       return (
 
           <div>
 
    		<p> Class Component </p>
 
               <p>{this.state.first_name}</p>
 
               <p>{this.state.last_name}</p>
 
           </div>
 
       )
 
   }
 
}
export default StateLessExample;
```

12. ### Explain the purpose of render() in React.

* Each React component must have a render() mandatorily.<br> 
* It returns a single React element which is the representation of the native DOM component.<br> 
* If more than one HTML element needs to be rendered,then they must be grouped together inside one enclosing tag such as <form>, <group>,<div> etc.<br> 
* This function must be kept pure i.e., it must return the same result each time it is invoked.<br>

13. ### What is Props?

* “Props” is a special keyword in React, which stands for properties and is being used for passing data from one component to another.<br>
* They are always passed down from the parent to the child components throughout the application.<br>
* Furthermore, props data is read-only, which means that data coming from the parent should not be changed by child components.<br>
* This help in maintaining the unidirectional data flow and are generally used to render the dynamically generated data.<br>


14. ### What is a state in React and how is it used?

* States are the heart of React components. 
* States are the source of data and must be kept as simple as possible. 
* Basically, states are the objects which determine components rendering and behavior. 
* They are mutable unlike the props and create dynamic and interactive components. They are accessed via this.state().
* Has setState() method to modify properties.
* Writeable/Mutable

#### Let's create an user component with message state,

```jsx harmony
class User extends React.Component {
  constructor(props) {
    super(props)

    this.state = {
      message: 'Welcome to React world'
    }
  }

  render() {
    return (
      <div>
        <h1>{this.state.message}</h1>
      </div>
    )
  }
}
```


15. ### Differentiate between states and props.

* Both props and state are plain JavaScript objects.<br> 
* Props are immutable i.e. once set the props cannot be changed, while State is an observable object that is to be used to hold data that may change over time and to control the behavior after each change.<br>
* States can only be used in Class Components while Props don’t have this limitation.While Props are set by the parent component, State is generally updated by event handlers.<br>
* Props get passed to the component similar to function parameters whereas state is managed within the component similar to variables declared within a function.<br>

<table>
  <tr>
    <th>Conditions</th>
    <th>State</th>
    <th>Props</th>
  </tr>
  <tr>
    <td>Receive initial value from parent component</td>
    <td>Yes</td>
    <td>Yes</td>
  </tr>
  <tr>
    <td>Set initial value for child components</td>
    <td>Yes</td>
    <td>Yes</td>
  </tr>
  <tr>
    <td>Set default values inside component</td>
    <td>Yes</td>
    <td>Yes</td>
  </tr>
  <tr>
    <td>Parent component can change value</td>
    <td>No</td>
    <td>Yes</td>
  </tr>
  <tr>
    <td>Changes inside component</td>
    <td>Yes</td>
    <td>No</td>
  </tr>
  <tr>
    <td>Changes inside child components</td>
    <td>No</td>
    <td>Yes</td>
  </tr>
</table>

16. ### What are the different phases of React component’s lifecycle?

#### There are four different phases of React component’s lifecycle:

* 1 Initialization: This is the stage where the component is constructed with the given Props and default state. This is done in the constructor of a Component Class.<br>

* 2 Mounting: Mounting is the stage of rendering the JSX returned by the render method itself.<br>

* 3 Updation: Updation is the stage when the state of a component is updated and the application is repainted.<br>

* 4 Unmounting: As the name suggests Unmounting is the final step of the component lifecycle where the component is removed from the page.<br>

#### Now let us describe each phase and its corresponding functions.<br>

#### 1 Initialization: 

* In this phase the developer has to define the props and initial state of the component this is generally done in the constructor of the component. The following code snippet describes the initialization process.<br>

```jsx harmony
class Clock extends React.Component { 
    constructor(props) 
    {    
        // Calling the constructor of  
        // Parent Class React.Component 
        super(props);  
          
        // Setting the initial state 
        this.state = { date : new Date() };  
    } 
}
```

#### 2 Mounting: 

* Mounting is the phase of the component lifecyle when the initialization of the component is completed and the component is mounted on the DOM and rendered for the first time in the webpage.<br> 
* Now React follows a default procedure in the Naming Conventions of this predefined functions where the functions containing “Will” represents before some specific phase and “Did” represents after the completion of that phase.<br> 
Mounting phase consists of two such predefined functions as described below.

* componentWillMount() Function: As the name clearly suggests, this function is invoked right before the component is mounted on the DOM i.e. this function gets invoked once before the render() function is executed for the first time. <br>
* componentDidMount() Function: Similarly as the previous one this function is invoked right after the component is mounted on the DOM i.e. this function gets invoked once after the render() function is executed for the first time. <br>


#### 3 Updation:

* React is a JS library that helps create Active web pages easily. Now active web pages are specific pages that behave according to its user.<br>
* Updation is the phase where the states and props of a component are updated followed by some user events such as clicking, pressing a key on keyboard etc.<br>

#### The following are the descriptions of functions that are invoked at different points of Updation phase.

* componentWillRecieveProps() Function: This is a Props exclusive Function and is independent of States. This function is invoked before a mounted component gets its props reassigned. The function is passed the new set of Props which may or may not be identical to the original Props. Thus checking is a mandatory step in this regards. The following code snippet shows a sample use-case. <br>

```jsx harmony
componentWillRecieveProps(newProps) 
{ 
	if (this.props !== newProps) { 
		console.log(" New Props have been assigned "); 
		// Use this.setState() to rerender the page. 
	} 
}
``` 

* shouldComponentUpdate() Function: By default, every state or props update re-render the page but this may not always be the desired outcome, sometimes it is desired that on updating the page will not be repainted. The shouldComponentUpdate() Function fulfills the requirement by letting React know whether the component’s output will be affected by the update or not. shouldComponentUpdate() is invoked before rendering an already mounted component when new props or state are being received. If returned false then the subsequent steps of rendering will not be carried out. This function can’t be used in case of forceUpdate(). The Function takes the new Props and new State as the arguments and returns whether to re-render or not. <br>

* componentWillUpdate() Function: As the name clearly suggests, this function is invoked before the component is rerendered i.e. this function gets invoked once before the render() function is executed after the updation of State or Props. <br>
* componentDidUpdate() Function: Similarly this function is invoked after the component is rerendered i.e. this function gets invoked once after the render() function is executed after the updation of State or Props.

#### 4. Unmounting: 

This is the final phase of the lifeycle of the component that is the phase of unmounting the component from the DOM. The following function is the sole member of this phase.

* componentWillUnmount() Function: * This function is invoked before the component is finally unmounted from the DOM i.e. this function gets invoked once before the component is removed from the page and this denotes the end of the lifecycle.

```jsx harmony
import React from 'react'; 
import ReactDOM from 'react-dom'; 

class LifeCycle extends React.Component { 
	constructor(props) 
	{ 
		super(props); 
		this.state = { hello : "World!" }; 
	} 

	componentWillMount() 
	{ 
		console.log("componentWillMount()"); 
	} 

	componentDidMount() 
	{ 
		console.log("componentDidMount()"); 
	} 

	changeState() 
	{ 
		this.setState({ hello : "Sagar!" }); 
	} 

	render() 
	{ 
		return ( 
			<div> 
			<h1>GHello{ this.state.hello }</h1> 
			<h2> 
			<a onClick={this.changeState.bind(this)}>Press Here!</a> 
			</h2> 
			</div>); 
	} 

	shouldComponentUpdate(nextProps, nextState) 
	{ 
		console.log("shouldComponentUpdate()"); 
		return true; 
	} 

	componentWillUpdate() 
	{ 
		console.log("componentWillUpdate()"); 
	} 

	componentDidUpdate() 
	{ 
		console.log("componentDidUpdate()"); 
	} 
} 

ReactDOM.render( 
	<LifeCycle />, 
	document.getElementById('root'));
``` 


17. How are forms created in React?

* React forms are similar to HTML forms. But in React, the state is contained in the state property of the component and is only updated via setState(). Thus the elements can’t directly update their state and their submission is handled by a JavaScript function. This function has full access to the data that is entered by the user into a form. <br>

```jsx harmony
import React from 'react';

class App extends React.Component {
   constructor(props) {
      super(props);
      
      this.state = {
         textdata: ''
      }
     
   }

    handleSubmit = (event) => {
        alert("Form Data is " + this.state.textdata);
        event.preventDefault(); //Function Will Print Data as it is
    }
   
   render() {
      return (
         <div>
             <form onSubmit={this.handleSubmit}>
               <input type = "text" placeholder='Enter data' value = {this.state.textdata} />
               <input type="submit"></input>
             </form>
            <h4>{this.state.textdata}</h4>
         </div>
      );
   }
}
export default App;
```

#### 18. How many Ways to Optimize Performance of your React App ?

#### 19. Where we can use class component and function component in react js?

#### 20. How to Pass data between react components ? Redux, props, context api In which case we can use?

#### 21. Explain Redux Thunk and Redux saga ?

#### 22. Explain React LifeCycle method?

#### 23.  
