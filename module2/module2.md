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

# Curso   Module 2: Using Controllers   Resource Content: Controllers   Scope Overview

### Scope Overview

The $scope object is used to make the model available to the view. It is also referred to as the view model.

Essentially, if you want a variable to be able to be used or influenced by the view, you assign it as a subproperty to the Scope.

As discussed prior, the scope is defined and controlled by Controllers.

# Curso   Module 2: Using Controllers   Resource Content: Controllers   Scope Properties

### Scope Properties
 Bookmark this page
Scope Properties

To define Scope variables, simply assign them as subproperties of the $scope object.
```[javascript]
var app = angular.module("app", [])
.controller("myController", [
    "$scope",
    function ($scope) {
        $scope.name = "Fred Flintstone";
    }
]);
```

Scope properties can be any standard JavaScript object.
```[javascript]
$scope.person = {
     firstName: "Fred",
     lastName: "Flintstone"
};
```

# Curso   Module 2: Using Controllers   Resource Content: Controllers   Scope Methods

## Scope Methods
 Bookmark this page
Scope Methods

To create a function that your view can use (such as something bound to a click event), assign a function as a subproperty of the Scope object, like so:

```[javascript]

var app = angular.module("app", [])
.controller("myController", [
    "$scope",
    function ($scope) {
        $scope.title = "Home";
        
        $scope.renameTitle = function (newValue) {
            $scope.title = newValue;
        };
    }
]);
```

Or alernatively:

```[javascript]
var app = angular.module("app", [])
.controller("myController", [
    "$scope",
    function ($scope) {
        $scope.title = "Home";
        
        function renameTitle(newValue){
            $scope.title = newValue;
        }
        
        $scope.renameTitle = renameTitle;
    }
]);
```
Anonymous functions cannot be bound to the $scope.

# Curso   Module 2: Using Controllers   Resource Content: Controllers   Implementing Scope

### Implementing Scope

 Bookmark this page
Implementing Scope

Here is a full example of how Scope is used. As you can see here, title is bound to the $scope object, and a function called renameTitle.
```[javascript]
var app = angular.module("app", [])
.controller("myController", [
    "$scope",
    function ($scope) {
        $scope.title = "Home";
        
        $scope.renameTitle = function (newValue) {
            $scope.title = newValue;
        };
    }
]);
```
So this markup:
```[html]
<div ng-controller='myController'>
<h1>{{title}}</h1>
<a href='#' ng-click='renameTitle("Away")'>Click This to Change</a>
</div>
```

Would render to look like:
```[html]
<div ng-controller='myController'>
<h1>Home</h1>
<a href='#' ng-click='renameTitle("Away")'>Click This to Change</a>
</div>
```
And upon clicking on the link with renameTitle bound to the ng-click, the event would turn into:
```[html]
<div ng-controller='myController'>
<h1>Away</h1>
<a href='#' ng-click='renameTitle("Away")'>Click This to Change</a>
</div>
```

# Curso   Module 2: Using Controllers   Module Labs: Overview and Required Configuration   Labs Overview

### Labs Overview
 Bookmark this page
Labs Overview

This module of the course includes a series of three tutorial style labs and one self-assessment. Some lab configuration is required.

The tutorial labs are designed to teach you more about how to define and implement controllers . These labs will lead you step-by-step through setting up your controller, binding to controller scope, and implementing two-way binding.

The final lab in this module is a self-assessment lab. In this lab, you will apply what you've learned about controllers and properties during the tutorial labs to enhance an existing app. The self-assessment lab gives you the opportunity to reinforce what you learned without providing the prescriptive step-by-step instructions that are provided in the tutorial labs.

Tutorial Labs

Throughout the duration of this course, we will be building an application together to help demonstrate the concepts of programming in Angular. We're going to use something fairly simple that resembles an application that would be used in the real world - a pizza restaurant menu application.

Setting Up Your Controller

In this lab, you will set up your app with separately defined scripts instead of script tags within your HTML, define your app module, create a controller to house the logic for your menu, and bind your controller to the view using the $scope object.

Binding to Controller Scope

In this lab, you will declare $scope variables within the controller and bind them to your view, declare a $scope function and use it with an event handler, and declare a $scope watch.

Using Two-Way Binding with ng-model

In this lab, you will create communication between your controller and your view by implementing two-way binding between the view and the $scope by using ng-model, thereby creating a dynamic input field that updates data as you type it in.

# Curso   Module 2: Using Controllers   Module Labs: Overview and Required Configuration   Configuration: To Set Up the Lab Environment

### Configuration: To Set Up the Lab Environment
 Bookmark this page
Configuration: To Set Up the Lab Environment

You will be using Visual Studio Code to complete the labs in this module. You are welcome use a different editor to modify your code files, but the lab instructions in this course will describe the steps that you need to perform using Visual Studio Code unless otherwise noted.

Create a local folder on your development computer that you can use for your code project. Name the folder "Mod2Lab".

Note: You can use File Explorer or another tool of your choice to create the project folder.

Save the following zip to file the Mod2Lab project folder that you created above. 

Mod2_Lab_BeginningProject.zip (for Windows OS)

Tip: To open a Save As file dialog, right-click the link above, and then click Save target as or Save Link as.

Use File Explorer to open the Mod2Lab folder that you created above.

To extract the contents of the Mod2_Lab_BeginningProject.zip file, right-click Mod2_Lab_BeginningProject.zip, and then click Extract All.

Expand the Mod2_Lab_BeginningProject folder that was created when the files were extracted, and then move the contents of this folder (the extracted files and folders) into root of the Mod2Lab folder.

Note: The Mod2_Lab_BeginningProject folder that was created when the files were extracted should now be empty.

Delete the Mod2_Lab_BeginningProject.zip file, or move it to another folder location outside of Mod2Lab project folder.
Verify that the Mod2_Lab_BeginningProject folder is now empty, and then delete the Mod2_Lab_BeginningProject folder.


# Curso   Module 2: Using Controllers   Tutorial Lab: Setting Up Your Controller   To Set Up Your HTML

### To Set Up Your HTML
 Bookmark this page
To Set Up Your HTML

In this lab we will expand on your ability to use Controllers to bind data to your View, by showing you how to do things like binding functions to the scope and utilizing scope watches. In order to do this, we will be building a small interactive pizza menu.

To start us off, let's get our files ready for our new controller.

Note that we are using separate files now for our controllers and views. This is the preferred way to organize an application, rather than putting all of your HTML and JavaScript in one big file.

Use Visual Studio Code to open the Mod2Lab folder that you created as part of the lab configuration process.

In Visual Studio Code, in the Explorer pane, to create a folder that you will use for your JavaScript files, click New Folder, type app and then press Enter.

To create a new JavaScript file in the "app" folder, right-click app, click New File, type app.js and then press Enter.

Also in the "app" folder, create a second file named menuController.js.

Open index.html.

Just before the closing </body> tag, to add script references for the JavaScript files, enter the following code:

<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.5.5/angular.min.js"></script>
<script src="./app/app.js"></script>
<script src="./app/menuController.js"></script>
Now we can define our app and controller.

# Curso   Module 2: Using Controllers   Tutorial Lab: Binding to Controller Scope   To Declare Scope Variables and Bind the Variables to Your View

# To Declare Scope Variables and Bind the Variables to Your View
 Bookmark this page
To Declare Scope Variables and Bind the Variables to Your View

In this lab we are going to use the $scope object to communicate with our view. The $scope variable allows you to tell your HTML that there is a value in your controller that needs to be displayed in the HTML. Not only that, Angular will keep up on $scope variables and update them as they change. This is the fundamental difference between Angular and standard JavaScript programming, as you are setting up code for your view to keep up with the logic and maintain the values itself, rather than having to change the view yourself as values change.

Now that we have our controller in place and wired up to our page, let's set the title based on a scope property.

If it isn't already open, use Visual Studio Code to open your Mod2Lab folder.

In Visual Studio Code, open your menuController.js file.

Inside the main function($scope) method, to create a property named "title", enter the following code:

$scope.model = {title: 'Our Menu'};
Open the index.html file.

Inside the <h2> tag, to display the title variable that you just defined inside your controller rather than static text, replace the contents of the <h2> tag with {{model.title}}.

Note: It is best practice to always bind to an object off of the scope, in this case, "model". This provides a clean separation and avoids binding issues in a more complex application.

Putting a $scope variable's name inside an Angular expression {{ }} binds it to the view, and sets up a watcher to keep up on the value.

Performance Tip: If you know a variable isn't going to change in the view, and you just want to bind its initial value, you can use the '::' characters in your expression (e.g. {{::model.title}}) to perform a one-time binding. This tells Angular to go ahead and set the value the first time, but not to set a watcher to keep up on it. This can be a useful performance boost for larger applications.

On the File menu, to save your work, click Save All.
Use your browser to open your index.html file. Verify that the title property from the scope is now displayed on the page.

# Curso   Module 2: Using Controllers   Tutorial Lab: Binding to Controller Scope   To Declare a Scope Function

### To Declare a Scope Function
 Bookmark this page
To Declare a Scope Function

In addition to creating values for your views to reference, the $scope object can also hold functions for your view to interact with using Angular's event handlers such as ng-click, ng-mouseover, etc. This has several advantages, such as not having to manage event handlers separately or deal with the lifecycle of unbinding them when elements are removed from the DOM.

In Visual Studio Code, open your menuController.js file.

Within the main function($scope) method, to create a function that will be used to change the menu item that a customer is ordering, enter the following code:

$scope.changeMainDish = function (item) {
    $scope.model.mainDish = item;
}
This function is setting a property on the scope with the parameter value. Now you need to display that value on your page.

Open the index.html file.

Below the <h2> tag that displays the title variable, to display a selectable list of menu items on your page, enter the following code:

    <div>
        <label><input type="radio" name="category" /> Cheese Pizza</label>
    </div>
    <div>
        <label><input type="radio" name="category" /> Pepperoni Pizza</label>
    </div>
    <div>
        <label><input type="radio" name="category" /> Margherita Pizza</label>
    </div>
    <div>
        <label><input type="radio" name="category" > BBQ Chicken Pizza</label>
    </div>
    <div>
        <label><input type="radio" name="category" /> Combo Pizza</label>
    </div>

    
Then, let's add the ng-click attribute to each of these elements to set up a click handler for each of these events to run changeMainDish when they are clicked on:

    <div>
        <label><input type="radio" name="category" ng-click="changeMainDish('Cheese Pizza')"/> Cheese Pizza</label>
    </div>
    <div>
        <label><input type="radio" name="category" ng-click="changeMainDish('Pepperoni Pizza')"/> Pepperoni Pizza</label>
    </div>
    <div>
        <label><input type="radio" name="category" ng-click="changeMainDish('Margherita  Pizza')"/> Margherita Pizza</label>
    </div>
    <div>
        <label><input type="radio" name="category" ng-click="changeMainDish('BBQ Chicken Pizza')"/> BBQ Chicken Pizza</label>
    </div>
    <div>
        <label><input type="radio" name="category" ng-click="changeMainDish('Combo Pizza')"/> Combo Pizza</label>
    </div>

    
Finally, let's add this code underneath the list to display which item you have selected out of the list, by binding it to the $scope variable that is being set in the changeMainDish function.



    <div>
        <h3>Selected Item</h3>
        <pre>{{model.mainDish}}</pre>
    </div>
Save your work, and then use your browser to open your page.

In the browser view of your page, select a radio button for one of the menu items. You should see that the name of the selected menu item is displayed below the text "Selected Item".

Your page should appear similar to the screenshot below.

Tutorial Lab Completed Screenshot
Let's relate what you are seeing in the browser to the code that your entered above. When a menu item is selected, a click event is fired that passes the name of the corresponding menu item to the changeMainDish function. The changeMainDish function updates the value of mainDish, which is then displayed in the <pre> tag under the text "Selected Item".

If you need help, please review the Implementing Scope document.

#