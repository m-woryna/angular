# angular


ANGULAR

AngularJS extends HTML with new attributes. 
AngularJS is perfect for Single Page Applications (SPAs).
AngularJS is easy to learn.

AngularJS Example

<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<div ng-app="">
 
<p>Input something in the input box:</p>
<p>Name : <input type="text" ng-model="name" placeholder="Enter name here"></p>
<h1>Hello {{name}}</h1>

</div>

</body>
</html>

AngularJS Introduction

AngularJS is a JavaScript framework. It can be added to an HTML page with a <script> tag.
AngularJS extends HTML attributes with Directives, and binds data to HTML with Expressions.
AngularJS is a JavaScript Framework

AngularJS is a JavaScript framework written in JavaScript.
AngularJS is distributed as a JavaScript file, and can be added to a web page with a script tag:
--------

<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
---------
AngularJS Extends HTML

AngularJS extends HTML with ng-directives.
The ng-app directive defines an AngularJS application.
The ng-model directive binds the value of HTML controls (input, select, textarea) to application data.
The ng-bind directive binds application data to the HTML view.
AngularJS Example
----------
<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<div ng-app="">
 
<p>Input something in the input box:</p>
<p>Name: <input type="text" ng-model="name"></p>
<p ng-bind="name"></p>

</div>

</body>
</html>
------------

Example explained:

AngularJS starts automatically when the web page has loaded.
The ng-app directive tells AngularJS that the <div> element is the "owner" of an AngularJS application.
The ng-model directive binds the value of the input field to the application variable name.
The ng-bind directive binds the content of the <p> element to the application variable name. 

AngularJS Directives
As you have already seen, AngularJS directives are HTML attributes with an ng prefix.
The ng-init directive initializes AngularJS application variables.
-------
<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<div ng-app="" ng-init="firstName='John'">

<p>The name is <span ng-bind="firstName"></span></p>

</div>

</body>
</html>
-----------

Alternatively with valid HTML: 

<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<div data-ng-app="" data-ng-init="firstName='John'">

<p>The name is <span data-ng-bind="firstName"></span></p>

</div>

</body>
</html>
-----------
!!!
You can use data-ng-, instead of ng-, if you want to make your page HTML valid.
!!!
You will learn a lot more about directives later in this tutorial.

*************
AngularJS Expressions
**************
AngularJS expressions are written inside double braces: {{ expression }}.
AngularJS will "output" data exactly where the expression is written:
----------
<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<div ng-app="">
<p>My first expression: {{ 5 + 5 }}</p>
</div>

</body>
</html>
--------
AngularJS expressions bind AngularJS data to HTML the same way as the ng-bind directive.
-------
<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<div ng-app="">
 
<p>Input something in the input box:</p>
<p>Name: <input type="text" ng-model="name"></p>
<p>{{name}}</p>

</div>

</body>
</html>
--------
*********
AngularJS Applications
**********
AngularJS modules define AngularJS applications.
AngularJS controllers control AngularJS applications.
The ng-app directive defines the application, the ng-controller directive defines the controller.
----------
<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<p>Try to change the names.</p>

<div ng-app="myApp" ng-controller="myCtrl">

First Name: <input type="text" ng-model="firstName"><br>
Last Name: <input type="text" ng-model="lastName"><br>
<br>
Full Name: {{firstName + " " + lastName}}

</div>

<script>
var app = angular.module('myApp', []);
app.controller('myCtrl', function($scope) {
    $scope.firstName= "John";
    $scope.lastName= "Doe";
});
</script>

</body>
</html>
--------------
AngularJS modules define applications:
AngularJS Module
-----------
var app = angular.module('myApp', []); 
-------------
AngularJS controllers control applications:
AngularJS Controller
------------
app.controller('myCtrl', function($scope) {
  $scope.firstName= "John";
  $scope.lastName= "Doe";
}); 
------------
You will learn more about modules and controllers later in this tutorial.

****************
AngularJS Expressions
****************
AngularJS binds data to HTML using Expressions.
AngularJS Expressions

AngularJS expressions can be written inside double braces: {{ expression }}.
AngularJS expressions can also be written inside a directive: ng-bind="expression".
AngularJS will resolve the expression, and return the result exactly where the expression is written.
AngularJS expressions are much like JavaScript expressions: They can contain literals, operators, and variables.

Example {{ 5 + 5 }} or {{ firstName + " " + lastName }}
----------
<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<div ng-app>
<p>My first expression: {{ 5 + 5 }}</p>
</div>

</body>
</html>
----------
!!! If you remove the ng-app directive, HTML will display the expression as it is, without solving it: !!!

You can write expressions wherever you like, AngularJS will simply resolve the expression and return the result.

Example: Let AngularJS change the value of CSS properties.
Change the color of the input box below, by changing its value:
-----------
<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<p>Change the value of the input field:</p>

<div ng-app="" ng-init="myCol='lightblue'">

<input style="background-color:{{myCol}}" ng-model="myCol">

</div>

<p>AngularJS resolves the expression and returns the result.</p>

<p>The background color of the input box will be whatever you write in the input field.</p>

</body>
</html>
-----------------
AngularJS Numbers
===============

AngularJS numbers are like JavaScript numbers:
----------
<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<div ng-app="" ng-init="quantity=2;cost=5">
<p>Total in dollar: {{ quantity * cost }}</p>
</div>

</body>
</html>
---------
Same example using ng-bind:
---------
<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<div ng-app="" ng-init="quantity=2;cost=5">
<p>Total in dollar: <span ng-bind="quantity * cost"></span></p>
</div>

</body>
</html>
-----------
!!!!! Using ng-init is not very common. You will learn a better way to initialize data in the chapter about controllers.

AngularJS Strings
====================
AngularJS strings are like JavaScript strings:
----------
<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<div ng-app="" ng-init="firstName='John';lastName='Doe'">

<p>The full name is: {{ firstName + " " + lastName }}</p>

</div>

</body>
</html>
-----------
Same example using ng-bind:
------------
<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<div ng-app="" ng-init="firstName='John';lastName='Doe'">

<p>The full name is: <span ng-bind="firstName + ' ' + lastName"></span></p>

</div>

</body>
</html>
----------

AngularJS Objects
===================
AngularJS objects are like JavaScript objects:
-------------
<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<div ng-app="" ng-init="person={firstName:'John',lastName:'Doe'}">

<p>The name is {{ person.lastName }}</p>
<p>The imie is {{ person.firstName }}</p>
</div>

</body>
</html>
---------------------

AngularJS Arrays
=================
AngularJS arrays are like JavaScript arrays:
Example
----------
<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<div ng-app="" ng-init="points=[1,15,19,2,40]">

<p>The third result is {{ points[2] }}</p>

</div>

</body>
</html>
----------------------

Same example using ng-bind:
-------------------------
<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<div ng-app="" ng-init="points=[1,15,19,2,40]">

<p>The third result is <span ng-bind="points[2]"></span></p>

</div>

</body>
</html>
---------------------

AngularJS Expressions vs. JavaScript Expressions
++++++++++++++++++++++++++++++++++++++++++++++++++++++
Like JavaScript expressions, AngularJS expressions can contain literals, operators, and variables.
Unlike JavaScript expressions, AngularJS expressions can be written inside HTML.
AngularJS expressions do not support conditionals, loops, and exceptions, while JavaScript expressions do.
AngularJS expressions support filters, while JavaScript expressions do not.
Learn about JavaScript in our JavaScript Tutorial.

****************************
AngularJS Modules
***************************
An AngularJS module defines an application.
The module is a container for the different parts of an application.
The module is a container for the application controllers.
Controllers always belong to a module.

Creating a Module
=========================
A module is created by using the AngularJS function angular.module
-------------

<div ng-app="myApp">...</div>

<script>

var app = angular.module("myApp", []);

</script>
-------------
The "myApp" parameter refers to an HTML element in which the application will run.
Now you can add controllers, directives, filters, and more, to your AngularJS application.
---------------
Adding a Controller
Add a controller to your application, and refer to the controller with the ng-controller directive:
---------------
<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<div ng-app="myApp" ng-controller="myCtrl">
{{ firstName + " " + lastName }}
</div>

<script>
var app = angular.module("myApp", []);
app.controller("myCtrl", function($scope) {
    $scope.firstName = "John";
    $scope.lastName = "Doe";
});
</script>

</body>
</html>
------------------
You will learn more about controllers later in this tutorial.

Adding a Directive
AngularJS has a set of built-in directives which you can use to add functionality to your application.
For a full reference, visit our AngularJS directive reference.
In addition you can use the module to add your own directives to your applications:
--------------------
<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<div ng-app="myApp" w3-test-directive></div>

<script>
var app = angular.module("myApp", []);
app.directive("w3TestDirective", function() {
    return {
        template : "I was made in a directive constructor ok ok!"
    };
});
</script>

</body>
</html>
---------------------------

You will learn more about directives later in this tutorial.

Modules and Controllers in Files
---------------------------------
It is common in AngularJS applications to put the module and the controllers in JavaScript files.
In this example, "myApp.js" contains an application module definition, while "myCtrl.js" contains the controller:
--------------
<!DOCTYPE html>
<html>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>
<body>

<div ng-app="myApp" ng-controller="myCtrl">
{{ firstName + " " + lastName }}
</div>

<script src="myApp.js"></script>
<script src="myCtrl.js"></script>

</body>
</html>
--------------

myApp.js
var app = angular.module("myApp", []);
!!!!!!!!!
The [] parameter in the module definition can be used to define dependent modules.
Without the [] parameter, you are not creating a new module, but retrieving an existing one.
!!!!!!!!!!!

myCtrl.js
app.controller("myCtrl", function($scope) {
  $scope.firstName = "John";
  $scope.lastName= "Doe";
});

Functions can Pollute the Global Namespace
------------------------------------------
Global functions should be avoided in JavaScript. They can easily be overwritten or destroyed by other scripts.
AngularJS modules reduces this problem, by keeping all functions local to the module.

When to Load the Library
------------------------
While it is common in HTML applications to place scripts at the end of the <body> element, it is recommended that you load the
AngularJS library either in the <head> or at the start of the <body>.
This is because calls to angular.module can only be compiled after the library has been loaded.
example:
--------
<!DOCTYPE html>
<html>
<body>
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.6.9/angular.min.js"></script>

<div ng-app="myApp" ng-controller="myCtrl">
{{ firstName + " " + lastName }}
</div>

<script>
var app = angular.module("myApp", []);
app.controller("myCtrl", function($scope) {
    $scope.firstName = "John";
    $scope.lastName = "Doe";
});
</script>

<p>It is recommended that you load the AngularJS library either in the HEAD or at the start of the BODY.</p>

</body>
</html>
--------







----------- https://www.w3schools.com/angular/angular_expressions.asp

