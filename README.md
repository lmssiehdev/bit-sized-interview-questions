[setTimeout]

setTimeout is a JavaScript function designed to schedule the execution of a function once, after a specified delay. It takes two parameters: the first is the function to be executed, and the second is the delay time in milliseconds. It also returns a Timeout ID, which can be used to cancel the timeout when it's no longer needed.

[setInterval]
setInterval is a Javascript function designed for repeatedly excute a specified function at a fixed time interval. It takes two parameters, the function to be excuted and the interval time (in milliseconds) between each execution. It also returns an intervalID that can be used to clean the interval once it's no longer needed, to avoid performance problems.

[script]

<script> tag is used for embeding javascript code, when encoutered, it halts the HTML parsing, fetch and excute the script before continuing the parsing.

<script async> allow loading scripts in parallel with parsing, but script will excute as soon as they load and not in the order they appear in the document, this is an issue if the script depends on other scripts or rely on the dom.

<script defer> is similar to async in the sense that it loads the script concurrently, but it will excute scripts in the order they appeared in and will also wait for the DOM to finish parsing before excuting. 

the script tag is used for embeding javascript in an HTML document, whenever the browser encounters a script tag it have to stop parsing the HTML in order to fetch the content, that's not what we want, we usally want the script in parallel with the parsing, luckily there is two attributes for that, async which allows the scripts to be loaded cuncerentlly, but the scripts don't excutes in order, and they do before the document is done parsing. these can be huge problems, especially if your scripts depend on each other or if the script relies on the dom. luckily there is the defer attribute for that.

[loose equality vs strict equality]

Loose equality coerces values into the same type before comparing them. For example, '5' == 5 evaluates to true. On the other hand, strict equality compares both the type and value, ensuring a more predictable and safer comparison.


// NaN doesn't equal to itself.
// +0 and -0 aren't eqaul
// use Object.is to handle these.

[null, undefined, undeclared]

A variable is undefined when it is declared in the local scope but has not been assigned a value. On the other hand, null is a value that you can intentionally assign to a variable to signify the absence of any object value. The term 'undeclared' refers to when you attempt to reference a non-existent variable, resulting in a ReferenceError.

[this]

In JavaScript, the this keyword refers to different values in different contexts. In the global context, it points to the global object (e.g., window in browsers). Inside a function, its value depends on how the function is called - if it's a simple function call, it refers to the global object; if it's a method of an object, it refers to that object. Arrow functions inherit this from the surrounding scope. In event handlers, this often represents the DOM element that triggered the event. The key takeaway is that this is dynamically scoped and its value is determined at runtime based on the execution context.


[.call & .apply]

.call and .apply are methods available to all functions, used to invoke a function with a specified 'this' value that is accepted as the first argument. The difference between them is that 'call' accepts arguments individually, while 'apply' accepts the arguments in an array.


[Hoisting]

Hoisting in JavaScript refers to the behavior where functions and variables declared with the 'var' keyword are moved to the top of their respective scope during the compilation phase. This allows you to use them before their explicit declaration in the code.

[Closure]

In JavaScript, a closure occurs when an inner function accesses the outer function's variables after the outer function has finished executing. This enables useful patterns, like maintaining state across function calls, as demonstrated in debounce.

[Event Bubbling]

When an event occurs on a specific element, it is first handled by that element's event handler and then propagates upwards through its parent elements in the DOM. This is particularly useful when dealing with a large number of nested elements. Instead of attaching an event handler to each individual element, we can simply attach it to the parent. Consequently, when we click on a child element, the event will bubble up to the parent, allowing for a more efficient and streamlined event handling process.

[.bind]

Function.prototype.bind is a method in JavaScript used to create a new function with a specified this value and preloaded with any number of arguments. Importantly, invoking bind does not immediately execute the new function; instead, it returns the newly created function. 

[javascript]

JavaScript, a dynamically typed language, is mainly used for creating interactive websites. It also can be used in diverse areas such as backend and mobile development.


[prototype]

In JavaScript, prototypal inheritance works by allowing objects to inherit properties and behaviors from other objects through a prototype chain. Each object has a link to another object, its prototype. When accessing a property or method, JavaScript looks up the prototype chain until it finds the desired property or reaches the end. 
