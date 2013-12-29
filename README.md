# Bind Event Handler
Bind Event Handler is a little snippet that checks what type of event attaching function is supported in the browser and then returns that function so that bindEventHandler() works as an event handler attachment function.

## Purpose of snippet
This snippet is especially useful when you don't use jQuery or any other library for attaching event handlers and you are creating user interface widgets with vanilla JavaScript. Testing the support for attaching event handlers each time you would want to register an event handler would have some negative impact on performance. With this snippet the support is being checked only once and the results are being cached.

## Usage
The usage of the snippet is fairly easy. It is being used just like any other event handler attaching function. It accepts three parameters:

* the DOM element,
* the name of the event that will trigger the handler,
* handler function

__Example:__
```javascript
var element = document.getElementById('test-element');

bindEventHandler(element, 'click', function() {alert('It works!')});
```