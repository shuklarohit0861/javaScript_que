Introduction
What versions of React and Angular are you using?
React 18. Angular 17
HTML
In HTML, if I write a button, html has an onclick attribute. What is the difference if we add a function to onclick versus adding an event handler for click?
Using onclick:
Inline, plain and simple, suitable for prototypes

Drawbacks: No separation of concern, not maintainable, can only assign one function, no event delegation
<button onclick="alert('Button clicked!')">Click me</button>
Using event handler:

Separation of concerns: Keeping JS separate.
Event Delegation: have more control on the flow of events with event delegate and capture
Flexibility: can add event listeners to all the buttons in a container. Can even listen to other events.
<button id="myButton">Click me</button> <script> document.getElementById('myButton').addEventListener('click', function() { alert('Button clicked!'); }); </script>
Even in case of a complex example, html will be free of js logic and js completely takes care of event handling (identifying the button and listening to events)


CSS
We have a parent div (500px X 500px) and a child div (200px X 200px) what are the options to center align the child div both horizontally and vertically.
Flexbox, css grid, position absolute
| .parent { display: flex; justify-content: center; align-items: center; height: 500px; width: 500px; } | .parent { display: grid; place-items: center; height: 500px; width: 500px; } | .parent { position: relative; height: 500px; width: 500px; }
.child { position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%); width: 200px; height: 200px; background-color: lightblue; } | | --- | --- | --- |


JavaScript
What is the difference between functional and object oriented programming?

JavaScript, you can mix both Functional Programming (FP) and Object-Oriented Programming (OOP) paradigms depending on your use case. Here's a summary of the differences:

FP: Focuses on functions, immutability, pure functions, and higher-order functions.
OOP: Focuses on objects, classes, encapsulation, and inheritance.

Polyfills

Write a polyfill for map method.
https://stackblitz.com/edit/stackblitz-starters-dyqcntc5?file=polyfills%2Ffilter.js

What are Promises? What problem does it solve?

Explain promises and callback hell

On load of an application, you have to fetch personal information from one server, medical information from another server and reports data from a third server. All the information are inter-related. How do you use promises to solve this?

Promise.All

JS is a single threaded language. How is JS handling, waiting for data and executing other tasks.

Explain Event Loop

What is the output of the below code

Follow up question, I’m not using new keyword, we are not instantiating anything. How does this work?

React

In functional components, how can you count the number of render cycles.
For a particular component within a span of 5 minutes of user interaction, 
I want to know how many times the component has gone through a render cycle.

Follow up, How are going to determine that the component is being rendered?

Can you write a custom hook for window.location.hash.
My component shows some inputs on the hash updates.
I want to use a custom hook for it. Any time the hash changes it has to update the component.

Node.js
What is the difference between node js and browser environment?
What is the window equivalent in node js
Any experience in improving the performance of a page. What factors would you consider, what changes would you make?
When it comes to front end, users will see the page as a whole, performance is from a user’s perspective?


Micro Front Ends

You have a page that is one Micro Front end.
How would you handle , if the micro front end fails to load?

I want to display the weather as a micro front end.
The micro front end itself fails to load. How can you handle it?

VDOM versus incremental DOM
In what scenario would you pick one over the other?
You open a tab on google chrome, you type in www.google.com. From the moment you hit enter till the page loads and you are able to search something. What happens within the browser?





