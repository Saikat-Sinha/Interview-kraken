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

