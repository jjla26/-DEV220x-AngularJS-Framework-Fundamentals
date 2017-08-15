# Curso   Module 2: Using Controllers   Resource Content: Controllers   MVVM Overview

### MVVM Overview
 Bookmark this page
MVVM Overview

Angular is an implementation of the MVVM (Model-View-ViewModel) design pattern.

Model-View-ViewModel Diagram
MVVM is different from MVC, most notably because it allows for two-way data binding between the model and the view. For example, an input field could be modified by a user, which will cause the data in the model to change, or a change within the model can cause the input data to reflect different data instead.

MVVM consists of these three components:

Model

The model is the source of data, or the data itself, usually encapsulated in Services, Factories, or Constants in Angular. It is best to keep all the business logic in the model in MVVM.

View

The view is what the user sees and interacts with, in this case, the dynamic view presented by Angular on the web page. In Angular, instead of manipulating the DOM of the view itself as with jQuery, the views are constructed in such a way that any changes to the view model will cause the view to mutate accordingly.

View Model

The view model binds the data from the model to the view and vice versa. In Angular, it is encapsulated by the $scope variable, which is decorated by a function called a Controller. It's best to keep the view model as thin as possible, placing most of the logic to services and factories. Think of the view model as a series of streets, some can be one-way or two-way, depending on the desired functionality. Since data can be manipulated both by the user and the model, the view model allows for both interactions to work with the same variable.

Further reading

More information on the MVVM pattern can be found on Wikipedia. MVVM - Wikipedia

# Curso   Module 2: Using Controllers   Resource Content: Controllers   Controllers Overview

### Controllers Overview
 Bookmark this page
Controllers Overview

Controllers are a JavaScript Constructor Function. As their name implies, their primary purpose is to control; in this case, control the view model contained within the Angular Scope.

Controllers are used to:

Set the initial state of Scope variables, which are then made available for the View to consume and interact with
Add behavior to the Scope by two-way binding variables and declaring Scope functions
Set up communications to and from the view and Model objects such as Services, brought in through Dependency Injection
Angular invokes the controller with a $scope object. Any objects (or primitives) assigned to the scope become model properties. The role of controllers in Angular is to expose data to our view via $scope, and to add functions to $scope that contain business logic that enhances view behavior.

For example, you may have a variable that determines whether a DOM element, (say a button), is visible to the user. You declare that variable JavaScript (in the controller code) using the scope object as $scope.showLDBtn = true. Because you've declared it this way in the controller, the view (the HTML) that is associated with that controller can simply reference the variable: <button ng-show="showLDBtn == true">Load Data</button>. The ng-show property checks the value of showLDBtn and sets the visibility of the button accordingly. As the value of showLDBtn changes in JavaScript--say in response to some event--the button will be shown or hidden simply by changing the showLDBtn property to true or false.

Typically, when you create an application, you need to set up the initial state for the $scope. You do this by attaching properties to the $scope object. The properties contain the view model (the model that will be presented by the view). All the $scope properties will be available to the template at the point in the Document Object Model (DOM) where the controller is registered. You can associate controllers with scope objects implicitly via the ng-controller directive or $route service.

A controller should contain only the business logic needed for a single view; presentation logic should remain within views and directives. Note that the most efficient way to use controllers is by encapsulating work that doesn't belong to controllers into services, and then using these services in controllers via dependency injection (DI).

Do not use controllers to manipulate the DOM, format input, or filter output. Using databinding and other built-in Angular methods such as filters, form controls, and directives will help you maintain the testability and ease of use of your controllers. These methods will also keep the concern of your presentation layer at the view level. Likewise, avoid using Controllers to share code or state across controllers, or to manage the life-cycle of other components. This behavior should be kept at the Model level in services or factories.

Note: You can learn more about controllers here.

# Curso   Module 2: Using Controllers   Resource Content: Controllers   Creating a Controller

### Creating a Controller
 Bookmark this page
Creating a Controller

Controllers are created by registering with an existing Angular Module.
```[javascript]
var app = angular.module("app", [])
.controller("myController", [
    "$scope",
    function ($scope) {
        // do work here
    }
]);
```
Notice in our example that our controller is named myController, and that name will correspond to the ng-controller attribute in our HTML.

The // do work here line in the code above is where we will place our code to create and interact with our view model.

# Curso   Module 2: Using Controllers   Resource Content: Controllers   Implementing a Controller

### Implementing a Controller
 Bookmark this page
Implementing a Controller

As we have seen before, controllers are placed on the page with the ng-controller attribute. Here is an example using the myController we created.
```[html]
<body ng-controller="myController">
    ...
</body>
```
The controller does not have to be placed on the <body> tag; it can be used in any HTML tag. This allows finer grained control of your application and makes using multiple controllers easier.

Nesting controllers within each other results in separate scopes being created for each controller. Their scopes can be shared between each other by means of the scope.parent property. This can be useful for isolating logic within certain components of the page, but still maintaining a larger scope of more global function.
```[html]
<body ng-controller="pageController">
    <div ng-controller='myChildController'>
        <div ng-controller='evenDeeperController'>
        </div>
    </div>
</body>
```
In order to prevent variable collision between controllers and make referencing different scopes easier, use the controller as syntax. It will assign the scope for that controller to a separate variable that the view can reference.
```[html]
<body ng-controller="SettingsController1 as settings">
{{settings.sampleScopeVariable}}
</body>
```
