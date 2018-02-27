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
>:mag:[Reference](http://www.tothenew.com/blog/javascript-splice-vs-slice/)



---


## DOM


## APIS


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




## Network / Server


---







Useful Links
•	 http://davidshariff.com/blog/preparing-for-a-front-end-web-development-interview-in-2017/
•	https://frontendmasters.com/books/front-end-handbook/2017/practice/making-fd.html

