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
