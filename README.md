## Table of Contents

1. **[HTML](#html)**
2. **[CSS](#css)**
3. **[JavaScript](#javascript)**
4. **[DOM](#dom)**
5. **[APIS](#apis)**
6. **[Libraries / Frameworks](#libraries)**
	- **[Angular.js](#angularjs)**
	- **[React.js](#reactjs)**
7. **[Security](#security)**
8. **[Performance](#performance-1)**
9. **[Testing](#testing)**
10. **[Scripting Problems](#scripting-problems)**
11. **[Tools](#tools)**
	- **[NPM / YARN](#npm)**
	- **[Webpack / Gulp / Grunt](#bundling)**
12. **[Network / Server](#network)**


---

## HTML

1. HTML5 form validation

> This is an example answer


> this also works with new line


---

## CSS


## JavaScript

Difference between Cookies, LocalStorage and Session storage
> ![image](https://i.imgur.com/fYnNXpA.png)

:mag: [https://www.youtube.com/watch?v=AwicscsvGLg](https://www.youtube.com/watch?v=AwicscsvGLg)

Difference between document.readyState() and window.onload()

**window.onload**
>The load event on the window object triggers when the whole page is loaded including styles, images and other resources.


**readyState**
>The document.readyState property gives us information  3 possible values:
*loading* – the document is loading.
*interactive* – the document was fully read.(like HTML content is loaded and other content is yet to load )
*complete* – the document was fully read and all resources (like images,scripts,stylesheets etc) are loaded .


---
Slice vs Splice
<table>
  <thead>
    <tr>
      <th>splice()</th>
      <th>slice()</th>
      </tr>
  </thead>
  <tbody>
    <tr>
      <td>splice  method returns the removed item(s) in an array </td>
      <td>method returns the selected element(s) in an array, as a new array object</td>
    </tr>
    <tr>
      <td>changes orignial array/Issues</td>
      <td>original array is untouched</td>
        </tr>
        <tr>
      <td>takes <strong>n</strong> number of arguments (start,deleteCount,items) start is manditory</td>
      <td>takes <strong>2</strong> arguments (begin,end) both are optional parameters</td>
    </tr>
     </tbody>
</table>

>**Example:splice()**
```javascript
var array=[1,2,3,4,5];
console.log(array.splice(2));
//  [3, 4, 5], returned removed item(s) as a new array object.

console.log(array);
//  [1, 2], original array altered.

var array2=[6,7,8,9,0];
console.log(array2.splice(2,1));
//  [8]

console.log(array2.splice(2,0));
//[] , as no item(s) removed.

console.log(array2);
// [6,7,9,0]

var array3=[11,12,13,14,15];
console.log(array3.splice(2,1,"Hello","World"));
// [13]

console.log(array3);
//  [11, 12, "Hello", "World", 14, 15]
```

>**Example:slice()**
```javascript
var array=[1,2,3,4,5]
console.log(array.slice(2));
//  [3, 4, 5], returned selected element(s).

console.log(array.slice(-2));
//  [4, 5], returned selected element(s).
console.log(array);
//  [1, 2, 3, 4, 5], original array remains intact.

var array2=[6,7,8,9,0];
console.log(array2.slice(2,4));
//  [8, 9]
```
>:mag:[reference](http://www.tothenew.com/blog/javascript-splice-vs-slice/)



---

what this keyword does in JavaScript?

- In most of the cases this is determined by how the function is called
- It may be different each time function is called
- Out side the function this referes to the global object
- It behaves differently in strict mode and normal mode
- In strict mode, if this was not defined by the execution context, it remains undefined
- Arrow functions does not provdide there own this binding
- When a function is used as a constructor (with the new keyword), its this is bound to the new object being constructed

 :point_right::mag_right:[reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this)


---

what is bind()?

  - The simplest use of bind() is to make a function that, no matter how it is called, it will be called with a particular *this* value
  - bind() method always creates new function.this keyword is set to the provided value  
   
 :point_right::mag_right:[reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_objects/Function/bind)

---
what is call() and apply()?

- call and apply  are similar to bind() where as in bind it will return a new function but in call and apply it calls a function with the given this value and argument
- The only difference between call and apply is call() accepts an argument list, while apply() accepts a single array of arguments.
 
:point_right::mag_right:[reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/call)

---

Ways of creating objects in JS

**Using ES6 class syntax:**
```javascript
class myObject  {
  constructor(name) {
    this.name = name;
  }
}
var e = new myObject("hello");
```
**Using the Object() constructor:**
```javascript
var a = new Object();
```
**Using Object.create() method:**
>This method creates a new object extending the prototype object passed as a parameter.
```javascript
var a = Object.create(null);
```
**Using the bracket's syntactig sugar:**
>This is equivalent to Object.create(null) method, using a null prototype as an argument.
```javascript
var b = {};
```

**Using the function constructor + prototype:**
```javascript
function myObj(){};
myObj.prototype.name = "hello";
var k = new myObj()
```
:mag:[reference](https://coderwall.com/p/p5cf5w/different-ways-of-creating-an-object-in-javascript)

---
 what is Async/Await?

- async/await makes our job easier when working with promises
- we define a async function by using *async* keyword
- when an async function is called it returns a Promise.If we dont return a promise  it will create a promise and return value is wrapped in a promise
- await keyword pauses and waits for the passed promise to get resolved

why async/await is better than prmoise?
  - it is clean to write
      - easy to handle errors
      - easy to debug(error stack in async await points to the function which contains error exactly)
      - further reference :point_right::mag:[reference](https://hackernoon.com/6-reasons-why-javascripts-async-await-blows-promises-away-tutorial-c7ec10518dd9)

:point_right:[performance difference between promise and async await](https://kyrylkov.com/2017/04/25/native-promises-async-functions-nodejs-8-performance/)

![image](https://i.imgur.com/LklaBEt.jpg)
>:point_right::mag:[reference](https://blog.sessionstack.com/how-javascript-works-event-loop-and-the-rise-of-async-programming-5-ways-to-better-coding-with-2f077c4438b5)


:point_right::mag:[Async/await polyfill](https://github.com/touskar/async-await-es7/blob/master/index.js)

---

 Difference between callback approach and promise API

| callback        | promise           |
| ------------- |:-------------:|
| callback is a function which is called on the completion of the given task.This prevents any blocking, and allows other code to be run in meantime     | A promise is an object that may produce a single value some time in the future: A promise may be in one of 3 possible states: fulfilled, rejected, or pending.|
|Callbacks are just the name of a convention for using JavaScript functions. There isn't a special thing called a 'callback' in the JavaScript language, it's just a convention. Instead of immediately returning some result like most functions, functions that use callbacks take some time to produce a result|promise provides us with more cleaner and robust way to handle async code.And also handles errors in an easy way.a promise is a returned object to which you attach callbacks, instead of passing callbacks into a function|

 >**Example:callback**
 ```javascript
 function greeting(name) {
  alert('Hello ' + name);
}

function processUserInput(callback) {
  var name = prompt('Please enter your name.');
  callback(name);
}

processUserInput(greeting);
 ```

 >**Example:promise**

 ```javascript

  function successCallback(result) {
  console.log("It succeeded with " + result);
}

function failureCallback(error) {
  console.log("It failed with " + error);
}

doSomething(successCallback, failureCallback);


let promise = doSomething();
promise.then(successCallback, failureCallback);
 ```
**why to use promise over callback examples**

>:rage:callback hell

```javascript
doSomething(function(result) {
  doSomethingElse(result, function(newResult) {
    doThirdThing(newResult, function(finalResult) {
      console.log('Got the final result: ' + finalResult);
    }, failureCallback);
  }, failureCallback);
}, failureCallback);
```
>:innocent: promise
```javascript
doSomething()
.then(result => doSomethingElse(result))
.then(newResult => doThirdThing(newResult))
.then(finalResult => {
  console.log(`Got the final result: ${finalResult}`);
})
.catch(failureCallback);
```

>:mag:[reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Using_promises)
>:point_right::mag:[reference for performance difference between callback and promise](https://kyrylkov.com/2017/04/25/native-promises-async-functions-nodejs-8-performance/)
---
## DOM


## APIS
1. What is Internationalization (i18n) and  Localization (L10n)?

> **Internationalization** (also known as i18n) is the process of creating or transforming products and services so that they can easily be adapted to specific local languages and cultures. In other words, internationalization is the process of adapting your software to support multiple cultures (currency format, date format, and so on)

> **Localization** (also known as L10n) is the process of adapting internationalized software for a specific region or language. In other words,localization is the process of adapting your software to support one or more culture.

2. Do JavaScript has native support for Internalization?
> `Solution`: Yes, the **Intl** object is the namespace for the ECMAScript Internationalization API, which provides language sensitive string comparison, number formatting, and date and time formatting.

>:point_right: :mag: [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl)


## Libraries / Frameworks

### Angular
1.	How to make one way binding in angular 1

> `Solution:` In One-Way data binding, view (UI part) not updates automatically when data model changed and we need to write custom code to make it updated every time.


**Example:**
```
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
	<head>
		<title>
			AngularJs Two Binding Example
		</title>
		<script src="http://ajax.googleapis.com/ajax/libs/angularjs/1.4.8/angular.min.js"></script>
		<script type="text/javascript">
			var app = angular.module('angularbindapp', []);
			app.controller('angularbindingCtrl', function ($scope) {
			$scope.name = 'Welcome to Tutlane.com';
			});
		</script>
	</head>
	<body ng-app="angularbindapp">
		<div ng-controller="angularbindingCtrl">
			<p>
				Message:   {{ name }}
			</p>
		</div>
	</body>
</html>
```

---
2.	Difference between services and factory in angular

> `Solution: ` - A service is a constructor(Object.create()) function whereas a factory is not, a factory function is really just a function that gets called, which is why we have to return an object explicitly. Services allow us to use ES6. Angular services are application singletons, this means that there is only one instance of a given service per injector.

**Example:**
```
app.service('myService', function() {

  // service is just a constructor function
  // that will be called with 'new'

  this.sayHello = function(name) {
     return "Hi " + name + "!";
  };
});

app.factory('myFactory', function() {

  // factory returns an object
  // you can run some code before

  return {
    sayHello : function(name) {
      return "Hi " + name + "!";
    }
  }
});
```

---
3.	How do you share data between controllers without using rootscope in angular 1.x?
> `Solution:` Services, Factories or app level constants

---
4.	difference between component and directive, angular lifecycle, dirty checking and Digest cycle(Angularjs 1.x)

---
5.	What is $resource, $sce and $http (angular 1.x)

---

## Security


---

## Performance


---

## Testing

## Scripting Problems


---

## Tools




## Network / Server and Browser

1. what happens when you type in a URL in browser ?
> `Solution: `

I. browser checks cache; if requested object is in cache or is fresh, if cached skip to `step IX`

II. browser asks OS for server's IP address

III. OS makes a DNS lookup and replies the IP address to the browser

IV. browser opens a TCP connection to server (this step is much more complex with HTTPS)

V. browser sends the HTTP request through TCP connection

VI. browser receives HTTP response and may close the TCP connection, or reuse it for another request

VII. browser checks if the response is a redirect or a conditional response (3xx result status codes), authorization request (401), error (4xx and 5xx), etc.; these are handled differently from normal responses (2xx)

VIII. if cacheable, response is stored in cache

IX. browser decodes response (e.g. if it's gzipped)

X. browser determines what to do with response (e.g. is it a HTML page, is it an image, is it a sound clip?)

XI. browser renders response, or offers a download dialog for unrecognized types

More simplified diagram:
![image](https://i.imgur.com/sAgeGNR.png)

---
2. How browser rendering works?
> `Solution: `
![image](https://imgur.com/8trAk0z.png)

> **DOM Tree** - The browser starts by constructing the DOM tree (a tree of nodes corresponding to HTML elements).

> **CSSOM Tree** - Next the browser constructs the CSSOM tree (a tree of nodes corresponding to CSS selectors).

> **Render Tree** - The browser then traverses the DOM tree and matches each element with the appropriate style from the CSSOM tree. The result is the render tree. Elements that you can't see (i.e. the document head and elements with the "display" property set to "none") are not added to the render tree.

> **Painting** - Finally, the browser  uses the render tree to "paint" or "rasterize" the pixels currently within your viewport so that you can see them on your screen.

> **Repainting** - If dynamic changes occur (e.g. scrolling, adding/changing element properties with JavaScript, etc.) the browser must repaint the affected regions.

---



Useful Links
•	 http://davidshariff.com/blog/preparing-for-a-front-end-web-development-interview-in-2017/
•	https://frontendmasters.com/books/front-end-handbook/2017/practice/making-fd.html

