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
2. what is Doctype?
---
3. About data-tags in html5
---
4. What is the value passed in viewport tag (MetaTags)

## CSS

1.	Difference between rem and em

---
2.	FLEX

---
3.	Vertically and horizontally align an item using only css? (ans:- transform: translate(-50%, -50%)

---
4.	Box model and Box sizing

---
5.	Difference Between ID and Class

---
6.	CSS specificity rules

---
7.	What is the difference between Inline CSS and On Page CSS?

---
8.	block vs inline-block vs inline

---
9.	What are the different selectors in CSS?

---
10.	What is the purpose of the z-index and how is it used

---



## JavaScript

1. What is javascript typecasting? What is use strict in javascript?

---
2.	Difference between ' == ' and '==='.

---
3.	Difference between undefined and not defined

---
4. What is commonjs?

---
#### 5. Difference between callback approach and promise API
 
 >Promises and Callbacks are not fundamentally different promises are advisable when user wants to perform series of tasks

> callback is a function which is called on the completion of the given task.This prevents any blocking, and allows other code to be run in meantime 
 
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
 > promise provides us with more cleaner and robust way to handle async code.And also handles errors in an easy way.
>a promise is a returned object to which you attach callbacks, instead of passing callbacks into a function
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

>:rage:callback

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

---
6.	Difference between bind ,call, apply function.

---
7.	What is Event Bubbling/ Delegation

---
8.	Singleton design pattern in javascript

---
9.	What is prototype and inheritance in JS

---
10.	Difference between event.stopPropogation and event.preventDefault

---
11. Service workers related questions

---
12.	Web workers related questions

---
13.	What is web services.?


---
14.	Clone an object


---
15.	Define object and Create an object and instantiate it.


---
#### 16.	Ways of creating objects in JS

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
17.	Async/Await related questions


---
18.	What is closure, Hoisting, Broadcast,Emit and On


---
#### 19.	Difference between document.ready and window.load

**window.onload**
>The load event on the window object triggers when the whole page is loaded including styles, images and other resources.

**readyState**
>The document.readyState property gives us information about it. There are 3 possible values:
*loading* – the document is loading.
*interactive* – the document was fully read.
*complete* – the document was fully read and all resources (like images) are loaded too.



---
20.	HTML5 localstorage and session storage


---
21.	Race condition in javascript


---
#### 22.	Slice vs Splice
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
>:mag:[Reference](http://www.tothenew.com/blog/javascript-splice-vs-slice/)



---
23. about using ES6 sets over arrays

---
#### 24.	Write an emitter class? 
>:mag:[Solution](https://www.glassdoor.co.in/Interview/Write-an-emitter-class-emitter-new-Emitter-1-Support-subscribing-to-events-sub-emitter-subscribe-eve-QTN_1793084.htm)

  ---
25.	Multiple API requests

---
26.	Functional programming. what is composition

## DOM

1. How would you ensure clicking on this picture would go to a  specific link?

---
2.	How can we create routing without any framework with pure Javascript

---

## API

1. Indexed DB

---
2. PWA

---
3. browser Caching related question

---
4. Implement promise without using promise API

---
5. Write a polyfill for a promise

## Libraries / Frameworks

### Angular
1.	How to make one way binding in angular 1

---
2.	Difference between services and factory in angular

---
3.	How do you share data between controllers without using rootscope in angular 1.x? - service and app level constants

---
4.	difference between component and directive, angular lifecycle, dirty checking and Digest cycle(Angularjs 1.x)

---
5.	What is $resource, $sce and $http (angular 1.x)

---

## Security

1. Reflow / Repaint / Browser optimizations

---

## Performance

1. how do you increase the performance of application?

---
2. Chrome Developer tools

---

## Testing

## Scripting Problems

1.	How will you write a program to find-out if given string is Palindrome

---
2.	Sort the elements of the list using mergesort

---
3.	Find the maximum number in an array

---
4.	sum(2)(3)(5)(3) for n times

---
5.	Implement DFS algorithm over json data, to add function over a specific node.

---
6.	When to use array and when to use linked-list.

---
7.	Write an array flatten function.

---

## Tools

1. Use of build tools, webpack and how useful they are

---
2. How to bundle js files (best way)



## Network / Server

1. What kind HTTPS requests methods
---
2. HTTP status codes
---
3. explain CORS

---
4. polyfils and it's workings

---
5. How browsers work?

---
6. What happens once you enter url into browser?

---







Useful Links
•	 http://davidshariff.com/blog/preparing-for-a-front-end-web-development-interview-in-2017/
•	https://frontendmasters.com/books/front-end-handbook/2017/practice/making-fd.html

