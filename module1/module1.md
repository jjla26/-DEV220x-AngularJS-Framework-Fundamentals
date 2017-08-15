# Curso   Module 1: Getting Started with Angular   Resource Content: Getting Started with Angular   Video: What is Angular?

# Video: What is Angular?
 Bookmark this page
What is Angular?
 Hello and welcome back. We've just
introduced the course and kind of outlined
that this is the fundamentals of Angular
but i think we should spend a few
moments to really talk about what is
Angular. AngularJS is a JavaScript
application development framework and
what a framework does in general is
provides you a sort of top-level access
to some of the lower level functions in
JavaScript. So you don't necessarily have
to code as much JavaScript but what
Angular does a little bit better
than say a framework like JQuery or
anything like that is that it provides
kind of a different workflow and sort of
a different way of thinking about
JavaScript and this is especially useful
when you're constructing say single page
applications and a lot more complicated
and involved applications.
Ok so you mentioned JQuery there and
regular JavaScript so, hopefully a lot
of people are used to building
simple applications with that capability.
So why would I want to embrace Angular,
which is more complex than regular
JavaScript and jQuery, regardless of the
fact it does provide you a lot of
capabilities. So why would i choose to
build my application with Angular?
Angular is especially well-suited for
situations where you've got very
data-heavy applications. Applications
where the data is changing frequently
and large complex applications where you
would want to break it down into
multiple components. Ah so Angular gives
us an architectural pattern that we can
follow when constructing our apps. Exactly. As well as
giving us the utility to actually be
able to interact with data and so on. Yeah
and one of the, i mentioned before the
the difference in the workflow and
whereas in a primary basic
JavaScript application you're expected
to fetch data and then influence the
application with that data directly by
manipulating the DOM, what Angular does
is allows you to build reactive
components and essentially paths for your
data to follow to transform, basically
you're making these views able to
transform with the data and react to it
rather than having to influence it and
so instead of having kind of a command
control scenario over your over your
JavaScript, you're instead letting your
JavaScript and your HTML
kind of build itself upon the data
that you're presenting to it. So there's
obviously a lot that sits behind Angular
and we're not gonna be able to cover all
of that in this brief introduction so I
think we should instead set the scene
and head into one of the first
modules where we're going to be talking
about Angular modules, which is a unit of
encapsulation and dependency injection
in terms of how we can actually get
services and data start working together
Sounds good.

# Curso   Module 1: Getting Started with Angular   Resource Content: Getting Started with Angular   History of Angular

# History of Angular
 Bookmark this page
History of Angular

Angular is an open-source web framework for JavaScript applications. It's proven very popular, and was created in 2009 by two developers, Misko Hevery and Adam Abrons. The initial incarnation of Angular was GetAngular, which Hevery and Abrons designed to provide enterprise developers easy-to-build applications. Hevery was part of a Google team working on Google Feedback, and he grew increasingly frustrated with the immense amount of code, especially as testing and code modifications began. Hevery used GetAngular to rewrite Google Feedback, reducing the lines of code from 17,000 to 1,500. Clearly, that got Google's attention and development on GetAngular began in earnest. By the time, Abrons had stopped working on the original GetAngular project, Hevery and his manager, Brad Green, converted it into Angular, and Google built a team to create and support it. In 2012, Google released Angular version 1.0. To this day, Google continues to provide strong support and a cohesive community surrounding Angular.

Angular is so popular because it:

Provides improved application design architecture
Promotes code reusability
Offers plug and play components
Consists of easy-to-remove components
Employs two-way data binding
Allows better teamwork
Because of Angular's ease of use, developers of all experience levels can quickly understand its functionality and how to easily find specific code components. Angular contains the following core types of objects and components:

Modules
Controllers
Services
Directives.
These core components can be injected into each other using the Dependency Injection (DI) mechanism built into Angular. DI is a software design pattern that assigns dependencies to components instead of hard coding them within the component itself. You can divide your application into multiple types of components that Angular can inject into each other. You can create the components to be used in multiple applications without changing a single line of code, saving time and effort. Modularizing your application makes it easier to reuse, configure, and create easily testable components in your application.

Angular uses a feature called directives, allowing you to write HTML code, which then builds the HTML of your application instead of using templates to generate the user interface. The ng-model directive binds the value of HTML controls (input, select, and text area) to application data. Utilizing two-way data binding, the values in your view are tightly bound to the data source. When a user interacts and updates a value, your model is updated dynamically as well.

When a web page is loaded, the browser creates a Document Object Model (DOM) of the page. Using the DOM, JavaScript can access and change all the elements of an HTML document. This allows Angular to dynamically edit the HTML and provide updates to the HTML without requiring a page load.

Since Angular is DOM-based, each component can be separated into separate files. Angular will then recompose these components into the DOM. You will find that there are less merge conflicts and, therefore, overall project progress becomes much easier to track.

Angular offers speed and flexibility, due to its component structure. Since it is modular, you can easily write and reuse the code, which is also testable. This means that Angular is an effective tool for building enterprise-wide applications across platforms.

In September 2014, Angular version 2.0 was announced at ng-Europe. This revision includes a complete rewrite of most core components of Angular in order to take advantage of the latest browser specifications. It is also written in Microsoft's TypeScript language, allowing for advanced language features and graceful degradation to older versions of ECMAScript. Angular version 2.0 was released to the public in September 2016.

This course will focus on Angular 1.5x due to the current market saturation of that version. Future versions of this course may feature Angular 2.x as adoption increases.

# Curso   Module 1: Getting Started with Angular   Resource Content: Getting Started with Angular   Why Angular?

# Why Angular?
 Bookmark this page
Why Angular?

When it comes to application development, you have many available choices. You may find yourself asking, "Do I use MVC (model-view-controller) or MVVM (model-view-viewmodel)? Server-side or client-side rendering?"

Even in JavaScript, there are numerous methods of developing applications available, from vanilla JavaScript (JavaScript with no framework) and jQuery to Knockout and React. So the question is:

Why use Angular?

Let's consider a common use case. You have an application with a database. You want to be able to send updates to the database, and search the database for content. If you use vanilla JavaScript or jQuery, you will have to bind events to send the data, bind the outputs to the DOM, and update the DOM every time the data changes.

Angular is essentially a whole new paradigm of JavaScript programming. In the past, DOM updates were performed manually, and data contracts were managed manually. Angular does all of that heavy lifting for you, checking and updating the DOM with each $digest cycle. The $digest cycle is the function to update the DOM that Angular calls whenever the data is updated. This function enables you to construct your application without considering the DOM. For more information, refer to the $digest() section within the documentation for $rootScope.Scope located at, https://docs.angularjs.org/api/ng/type/rootScope.Scope.

Think of Angular as HTML on steroids. With Angular, you can create your HTML with the data components built in. Once you hook the data components up to controllers and services, the DOM adjusts according to the data (without the need for cumbersome manual updates) as the user interacts with your application.

In addition, Angular code is constructed with modules that can be easily injected into each other, so that you can build independently functioning, reusable components.

It takes a bit to get used to the Angular way of thinking. If you are a traditional JavaScript programmer, you are used to the workflow of "Get data; change the DOM." Instead, consider what you want your views to look like, and build them that way, before hooking up the data. It's a bit different, but in time, many developers have found they prefer this way of working. The Angular workflow separates the data and the views, even though, in essence, Angular completely entwines them.

# Curso   Module 1: Getting Started with Angular   Resource Content: Getting Started with Angular   What is Angular?

# What is Angular?
 Bookmark this page
What is Angular?

As a developer, the first question you usually get asked by others (especially other programmers) if you mention Angular is "What is Angular anyway?"

What Angular does for JavaScript development is so dramatic, it has received iconic status among JavaScript developers that is shared only by a few other frameworks - namely, jQuery and React.

Angular is a JavaScript framework - a higher-level abstraction of JavaScript functions designed to make writing JavaScript simpler and easier. It's also its own development pattern, and can change the way you shape and build your applications. While Angular has many abstractions to lower level JavaScript methods, it does not have the sheer number of functions that jQuery does, so you will frequently see them side by side, jQuery within Angular. Instead of being a multipurpose collection of lower-level JavaScript functions, Angular provides a new way of organizing and running your JavaScript by allowing your HTML to be dynamic and react to data.

Comparing the workflow environments of vanilla JavaScript (JavaScript with no framework) or a jQuery environment to that of Angular could be described as the difference between carrying water with a bucket or building an irrigation system. Using vanilla JavaScript or jQuery, data and states are carried through from databases or user inputs to be represented by the view. The view is then modified directly with specific, action-based thinking.

Angular, by contrast, functions more like building channels by which your data can flow to the view, and the view reacts to the data that it is given instead of needing to be influenced by direct command-based lines of code. So thinking about the root components of Angular can be more easily related to plumbing.

Services are like the initial valves that lead to the water source. They exist primarily to feed data into the pipeline.

Controllers are like the pipes that control the water flow to and from the Services.

View Templates are like the faucets, they exist to consume the data and react accordingly.

# Curso   Module 1: Getting Started with Angular   Resource Content: Getting Started with Angular   Video: Modules and Dependency Injection

# Video: Modules and Dependency Injection
 Bookmark this page
Modules and Dependency Injection
 
Hello this is Drake Boley again. I'm here
to help explain the basics of module
creation and dependency injection in
AngularJS and to start I've pulled up
this code editor. This is called codepen.
I don't know if any of you are familiar
with it but it is essentially a place
where you can enter HTML, CSS, JavaScript.
I already have
AngularJS loaded up as a dependency so
that we don't have to necessarily
included as a script tag, and so and we
can basically type into these boxes and
see the rendered view down here below so
that should make things a lot easier.
So what I'm going to start by doing is
I'm going to start by declaring the
module for our root Angular application,
which in this case I'm going to name
testApp, and we don't have any module
dependencies. If we were going to have
any other modules which this module
would depend upon they would go into
this array right here. So now I'm going
to go ahead and create my first
controller on this module. Because this
is essentially this uh, var app is now
the root module from which you can
define further components within your
Angular application. So now we're going
to do app.controller. So that this first
parameter here is essentially what
you're naming your controller and you,
you're going to use that later when
we bootstrap into our HTML, and a
function declaration. And we want to
include the scope of the controller
right here and we'll talk more about
scope in the next module but in, in
essence we'll just consider it, where
the variables live. So we're going to
declare just a basic variable in here.
And so now over here we're going to
bootstrap our application. So this HTML
in codepen already has the HTML tag, the
body tag, all of that, so we don't have to
worry about any of that. So we're going
to use the ng-app syntax and we're going
to reference this over here, this string
over here is what you would use to
bootstrap your application. So that
actually tells Angular to go ahead
and load your test app module onto this
particular <div>, and since we want to use
the data within this particular
controller, we're going to go ahead and
use the ng-controller syntax to bind
testController to this <div> as well. And
so once you've done that we can go ahead
and use curly braces to reference test
and when we do that, you will see the
output that, for the variable that we've
already defined over here. So that's the
basics of defining a module in Angular.
Now when we're talking about dependency
injection, essentially what we're going
to be doing is including something else
into that controller. So in this case
we're going to declare a constant and
it's going to be called testConstant
and
going to give it a string value of
constantValue. So then to inject this
constant into your controller all you
have to do is up here, where the function
is declared, you go ahead and include it
in what is required there. So then from
there, we could make a scope variable and
then we should be able to see, you can
see constantValue right here, has been
pulled in from this constant which we've
defined outside of this controller
and then pulled in through dependency
injection. There are much more advanced
uses for this but this is pretty much
the most basic way to demonstrate how
you can define different modules and
then pass them into different
controllers to get their values. And so
that's that's essentially it. We've, I've
taught you the basics of module
declaration, how to bootstrap your app,
and how to use dependency injection in it's
most basic form. Thank you.

# Curso   Module 1: Getting Started with Angular   Resource Content: Getting Started with Angular   Introduction to Angular Modules

# Introduction to Angular Modules
 Bookmark this page
Introduction to Angular Modules

In the most simple terms, an Angular module is nothing more than a container for various parts of your app. Since an Angular app does not have a single point of entry like some environments (such as a Main method in a C application), modules provide the means for defining how the application can be started. 

Note: Angular uses a Declarative Programming approach to define user interfaces and connect components.

In Angular, the word module refers to either an entire Angular application or independent components within that application, such as controllers, services, filters, and directives. The components of Angular modules provide specific functionality via self-contained sections of code. Through the process called Dependency Injection, modules can share variables between one another without having to reuse code.

Note: Dependency Injection will be discussed in greater detail in the next section.

Angular modules are organized by function rather than type. This modular concept helps you better understand the context of the different components, enables more direct access to the modules, and provides more streamlined testing of the modules.

Modules provide a number of benefits including:

They may be reused in multiple applications
They can be loaded in any order (or in parallel)
Unit testing need only load the relevant modules, keeping the tests fast

# Curso   Module 1: Getting Started with Angular   Resource Content: Getting Started with Angular   Creating Angular Modules

# Creating Angular Modules
 Bookmark this page
Creating Angular Modules

This is an example of defining a module in Angular.

var myApp = angular.module("myApp", []);
In this example, the module is assigned to the variable myApp on the left side of the assignment statement. The right side of the assignment is where the module is created, and in this example, is assigned the name "myApp". The empty array [] is where we can inject other modules as necessary. To bootstrap the module, you can use the HTML attribute ng-app='myApp' to bootstrap your app, or you can use the angular.bootstrap('myApp') syntax. You specify the variable name when you bootstrap a module.

Note: "Bootstrap" is just a fancy way of saying "configure and start."

To add controllers or other components to the module, reference the variable that you had defined for the module (var myApp in this instance), and then add additional method calls, like so:

var myApp = angular.module("myApp", []);
myApp.controller("myController", [function() {}]);
Sometimes in applications, you will see a different following syntax:

var myApp = angular.module("myApp", [])
.controller("myController", [function() {}]);
This syntax is also valid and is often more succinct as you are defining the module rather than chaining that together with the definition of the controller.

You will have probably noticed that the controller we have defined here doesn't do anything yet, but it is enough for us to use to get started.

# Curso   Module 1: Getting Started with Angular   Resource Content: Getting Started with Angular   Bootstrapping Your Angular Modules

# Bootstrapping Your Angular Modules

Bootstrapping your module starts Angular and initializes the module, binding it to a section of the HTML that you wish to transform into a dynamic view. "Binding" tells Angular that this piece of HTML will be controlled by Angular, which will allow it to transform the HTML as the data changes, thereby creating a "Dynamic View" instead of the "Static View" of plain HTML.

Your Angular app can affect as much or as little HTML as you prefer. For example, if you are defining a Single Page App, you will want to bootstrap your module on the <html> element, so that Angular can control the entirety of the page.

```[html]
<!DOCTYPE html>
<html ng-app="myApp">

<head>
    <title>My Page</title>
</head>

<body ng-controller="myController">
</body>

</html>
```
If you want Angular to only control some of your page, for example, if you are implementing Angular in a website that was built mostly out of jQuery, then you would do something like this:
```[html]
<!DOCTYPE html>
<html>

<head>
    <title>My Page</title>
</head>


<body>

<div>

There's some content here not controlled by Angular.
</div>

<div ng-app='myApp'>
This is the content that is controlled by the Angular module 'myApp'.
<div ng-controller='myController'>
This is the content controlled by the controller myController.
</div>

</div>

</body>
</html>
```
You could also use multiple Angular modules on the same page, enabling you to create two separate applications to control different pieces of the page, like so:
```[html]
<!DOCTYPE html>
<html>

<head>
    <title>My Page</title>
</head>


<body>

<div ng-app='myOtherApp'>
This is the content controlled by the Angular module 'myOtherApp'.
</div>

<div ng-app='myApp'>
This is the content that is controlled by the Angular module 'myApp'.
<div ng-controller='myController'>
This is the content controlled by the controller myController.
</div>

</div>

</body>
</html>
```
Note: You'll notice the Angular bootstrap property begins with ng-. This is a standard preface for Angular object references and probably has something to do with the way it sounds (or, as some suspect, the fact that it makes up the second two letters of the word Angular). If you use Visual Studio or Visual Studio Code, you can use Intellisense to find Angular objects by typing ng- and letting Visual Studio provide you with options for what Angular objects are available.

For more information , you can see: 
Visual Studio: https://aka.ms/edx-dev220x-vs01 
Download Visual Studio Code: https://aka.ms/edx-dev220x-vscode

# Curso   Module 1: Getting Started with Angular   Resource Content: Getting Started with Angular   Introduction to Dependency Injection

# Introduction to Dependency Injection
 Bookmark this page
Introduction to Dependency Injection

Dependency Injection (DI) is a software design pattern that manages how components in a system obtain their dependencies. In Angular, Dependency Injection is responsible for:

Creating components
Maintaining a component's state
Providing components to other components, as required
In Angular, DI allows us to share variables and functions between self-contained modules without having to reuse code, and maintains the state of each component.

DI employs the injector, the service object(s) to be used, the client object that is depending on the services it uses, and the interfaces.

Note: The Angular injector is used for retrieving services as well as creating the necessary objects for us. See: Angular Injector.

The injector introduces the services to the client. Often, it also constructs the client. An injector may connect together a very complex object graph by treating an object like a client, and later, as a service for another client. The injector may actually be many objects working together, but may not be the client.

Note: Services are discussed in our training course Advanced Framework Fundamentals with Angular. You can read more information on services in the documentation. Read More.

When Angular compiles the HTML, it processes the ng-controller directive, which, in turn, asks the injector to create an instance of the controller and its dependencies. The application code simply declares the dependencies it needs without having to deal with the injector. Angular invokes certain functions, such as service factories and controllers, via the injector. You annotate these functions so that the injector knows what services to inject into the function.

These functions are injectable with dependencies, just like the factory functions. The factory methods are registered with the modules. Components such as services, directives, filters, and animations are defined by an injectable factory method or constructor function. These components can be injected with service and value components as dependencies.

DI allows a client the flexibility of being configurable. Only the client's behavior is fixed. The client may act on anything that supports the intrinsic interface the client expects. The client only needs to know about the intrinsic interfaces of the services since these define how the client may use the services. This separates the responsibilities of use and construction. The interfaces are the dependency types that the client expects.

You use DI when defining components or when specifying functions to run at configuration and run time for a module by calling the config and run methods. The run method accepts a function, which can be injected with service, value, and constant components as dependencies. Note that you cannot inject providers into run blocks. The config method accepts a function, which can be injected with provider and constant components as dependencies. Note that you cannot inject service or value components into configuration.

# Curso   Module 1: Getting Started with Angular   Resource Content: Getting Started with Angular   Using Dependency Injection

# Using Dependency Injection
 Bookmark this page
Using Dependency Injection

One of the most commonly used dependencies in Angular is $scope. Controllers need access to the $scope object in order to bind values to the view (this will be explained further in the Controllers section of the course). In order to have the $scope available, all we need is the following code in place:

myApp.controller("myController", [
    "$scope",
    function($scope) {
        // do stuff here      
    }
]);
The controller initialization is similar to the one we've already seen, with a few additions:

On the second line, we have "$scope". This line specifies that we are adding a reference to the $scope object.
On the next line after that, we have the $scope object as a parameter. This defines $scope as a variable name in our controller.

# Curso   Module 1: Getting Started with Angular   Module Labs: Overview and Required Configuration   Labs Overview

# Labs Overview
 Añadido a marcadores
Labs Overview

This module of the course includes a series of three tutorial style labs and one self-assessment lab. Some lab configuration is required.

The tutorial labs are designed to help you set up Angular and start using Angular modules and dependency injection. These labs will lead you step-by-step through the process of bootstrapping Angular, creating modules, and implementing dependency injection.

The final lab in this module is a self-assessment lab. In this lab, you will apply what you've learned during the tutorial labs to create a new HTML page and separate JavaScript files for the app and controller. The self-assessment lab gives you the opportunity to reinforce what you learned without providing the prescriptive step-by-step instructions that are provided in the tutorial labs.

Tutorial Labs 

Bootstrapping Angular

There are multiple ways to instantiate Angular so that it works with your HTML to produce a dynamic view. The method that you choose will depend on whether you are building out a whole Single Page App (SPA), or just a component for an existing website. In this lab you will set up your HTML for Angular, declare your app, and bootstrap Angular.

Declaring Modules

In Angular, the word module refers to either an entire Angular application or independent components within that application, such as controllers, services, filters, and directives. In this lab, you will declare a Controller and bind the Controller to your HTML.

Implementing Dependency Injection

Dependency Injection is one of the best features in Angular. In this lab, you will learn how to declare constants and inject dependencies into your controllers. Services, Factories, and Resources can also be injected, and in labs that come up in later modules you will learn about them as well.

# Curso   Module 1: Getting Started with Angular   Module Labs: Overview and Required Configuration   Configuration: To Install Visual Studio Code

# Configuration: To Install Visual Studio Code
 Bookmark this page
To Install Visual Studio Code

In order to develop your Angular, let's set up Visual Studio Code.

Visual Studio Code is lightweight and is compatible with most available hardware and platform versions.

Mac OS X

Download Visual Studio Code for Mac OS X.
Double-click on the downloaded archive to expand the contents.
Drag Visual Studio Code.app to the Applications folder, making it available in the Launchpad.
Add Visual Studio Code to your Dock by right-clicking on the icon, and choosing Options, Keep in Dock.
Linux

Download Visual Studio Code for your distribution, .deb for Debian-based distributions such as Ubuntu or .rpm for Red Hat-based distributions, such as Fedora or CentOS.
Install the package through a graphical user interface package manager by double-clicking on the package file, or through the command line:

bash # For .deb sudo dpkg -i .deb

# For .rpm (Fedora 21 and below) sudo yum install .rpm

# For .rpm (Fedora 22 and above) sudo dnf install .rpm

Visual Studio Code should now be available to run through the launcher or the command line by running code.
Tip: Run code in any folder to start editing files in that folder.

Windows

Download Visual Studio Code for Windows.
To launch the setup process, double-click VSCodeSetup.exe.

By default, Visual Studio Code is installed in the "C:\Program Files (x86)\Microsoft VS Code" folder location (for a 64-bit machine). The setup process should only take about a minute.

Note: .NET Framework 4.5 is required for Visual Studio Code. If you are using Windows 7, please ensure .NET Framework 4.5 is installed.

For more detailed instructions and tips, visit the full Microsoft Visual Studio Code Installation Instruction guide here.

# Curso   Module 1: Getting Started with Angular   Module Labs: Overview and Required Configuration   Configuration: To Set Up the Lab Environment

# Configuration: To Set Up the Lab Environment
 Bookmark this page
Configuration: To Set Up the Lab Environment

You will be using Visual Studio Code to complete the labs in this module. You are welcome to use a different editor to modify your code files, but the lab instructions in this course will describe the steps that you need to perform using Visual Studio Code unless otherwise noted.

There are just a couple of steps required to set up the lab environment for this module.

Create a local folder on your development computer that you can use for your code project. Name the folder "Mod1Lab".

Note: You can use File Explorer or another tool of your choice to create the project folder.

Save the following code file to the project folder that you created above.

Note: You will need to rename the file to match the file name shown below.

helloworld.html
Tip: To open a Save As file dialog, right-click the links above, and then click Save target as or Save Link as.

# Curso   Module 1: Getting Started with Angular   Tutorial Lab: Bootstrapping Angular   To Set Up Your HTML for Angular and Declare Your App

## To Set Up Your HTML for Angular and Declare Your App
 Bookmark this page
To Set Up Your HTML for Angular and Declare Your App

In Angular, the word module refers to either an entire Angular application or independent components within that application. In the most simple terms, an Angular module is nothing more than a container for various parts of your app. In the following steps you will create an app module.

Open Visual Studio Code.

In Visual Studio Code, open the Mod1Lab folder that your created as part of the lab configuration process.

Open helloworld.html, and then locate the <body> section of your file.

Before the closing </body> tag, to add a reference to the Angular JavaScript library, enter the following code:

<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.5.5/angular.min.js"></script>

Directly below the code line that you just entered, to create a <script></script> tag that you will use to declare your Angular app, enter the following code:

<script></script>

Note: Remember that the term "module" and "app" in Angular are interchangeable. Angular modules are self-contained applications designed to either be standalone or components of other apps. You will be building up your Angular app and adding additional modules as you work your way through the labs in this course.

Between the <script></script> tags that you just created, to declare your Angular app, enter the following code:

var helloWorldApp = angular.module('helloWorldApp', []);

Note: In the code line above, the empty array represented by [], is where you would define any other Angular modules that your app may depend on (for example, ng-animate, ng-touch).

# Curso   Module 1: Getting Started with Angular   Tutorial Lab: Bootstrapping Angular   To Bootstrap Angular

## To Bootstrap Angular
 Bookmark this page
To Bootstrap Angular

The term "Bootstrap" is just a fancy way of saying "configure and start." In the previous section of this lab, you defined your helloWorldApp module. In the following steps you will bootstrap your app module by using the HTML attribute ng-app.

Note: The 'ng-app' is an example of a custom attribute. Angular is taking advantage of the fact that the developer can add arbitrary attributes to HTML elements. In fact, the HTML 5 specification does define custom attributes that start with 'data-'  - see here for more details on those. Of course, based upon the specification, the Angular attributes starting with 'ng-' are actually invalid HTML. In order to support them, the Angular reads (or pre-processes) your HTML page and uses the 'ng-' attributes to guide it as it makes changes to the HTML, resulting in the output of valid HTML that displays data, respond to actions, etc.

In Visual Studio Code, near the top of your helloworld.html file, locate the opening <html> tag.

To bootstrap Angular by using the ng-app attribute, update the <html> tag to appear as follows:

<html ng-app="helloWorldApp">
Generally, if you are creating a Single Page App, you would apply the ng-app attribute on the <html> tag to bootstrap your application for the entire page. If you are working with multiple angular apps in the same page, or if you want to isolate the Angular application to only a portion of the page, you can use ng-app on a lower level element, such as a <div> tag.

Locate the <body> section of your file, and then locate the <div> that contains the container class .

Below the code line that defines an <h1> header, to display content on your page by using an Angular expression, enter the following code:

<h2>{{'Hello from AngularJS'}}</h2>
The {{}} in this HTML are used to indicate an Angular expression. You can use an Angular expression like this to reference values that are defined in the Scope function of the module (more on that later). In this case, the expression is simply telling Angular to print the hard coded string "Hello from AngularJS".

Use File Explorer to open your Mod1Lab folder.

Open your helloworld.html file in your browser. Your page should look similar to the following:

AngularFundamentals - Hello from AngularJS
Note: Notice that the {{}} structure is not being displayed. This is because Angular has evaluated the contents of the mustaches (in this case your hard coded "hello" message) and has rendered the view using the evaluated value as intended.

At this point your helloworld.html file should look similar to the following:

HTML code
Note: If you need help please review Creating Angular Modules and Bootstrapping Your Angular Modules. in the Reference Content section of this module.

# Curso   Module 1: Getting Started with Angular   Tutorial Lab: Declaring Modules   To Declare a Controller

## To Declare a Controller
 Bookmark this page
To Declare a Controller

To add controllers or other components to an existing module, you reference the variable that you defined for the module. In the steps below you will add a controller to your helloWorldApp module. 

If it isn't already open, use Visual Studio Code to open your Mod1Lab folder.

Open your helloworld.html file, and then, in the <body></body> section, locate the <script></script> tag that is used to define your app module.

Below the code line used to define your helloWorldApp module, to create a new controller module named firstController, enter the following code:

helloWorldApp.controller('firstController', []);
Note: There are two things that you should notice about this code:

First, notice that we used the app name, helloWorldApp, at the front of our controller definition. This tells Angular to define your controller as part of the helloWorldApp module.

Second, notice the array brackets [] at the end of the controller definition. The array brackets are used to hold the contents of the controller, which you will start defining in the next step. The array can also be used for injecting additional dependencies into the controller, which you will learn more about later in this module.

To specify that your controller has a dependency on a $scope object, update the code for your controller as follows:

    helloWorldApp.controller('firstController', [
            '$scope',
            function($scope){
            }
        ]);
The '$scope' variable refers to the layer that binds the data from the controller into your view. For this reason, $scope is used by almost every controller.

The last spot in the dependency definition is where you put a function with inputs matching every dependency you injected prior to it function($scope). This will be where you actually put the logic for your controller.

Inside of the $scope function that you just added to your controller, to create a property of the $scope variable that can be used to display content on your Web page, update your $scope function as follows:

    function($scope){
        $scope.appName = 'An App Name';
    }
You create properties of the $scope variable to bind to your view. You can include other variables and program logic within your controller that you define normally, but they will not be accessible by the view if they are not defined within $scope.

The code for your controller should now look like the following:

helloWorldApp.controller('firstController', [
    '$scope',
    function($scope){
        $scope.appName = 'An App Name';
    }
]);

# Curso   Module 1: Getting Started with Angular   Tutorial Lab: Declaring Modules   To Bind the Controller to Your HTML

## To Bind the Controller to Your HTML
 Bookmark this page
To Bind the Controller to Your HTML

When Angular compiles the HTML, it processes the ng-controller directive, which in turn asks the injector to create an instance of the controller and its dependencies. In the following steps you will use ng-controller to bind your controller to your HTML.

In your helloworld.html file, locate the opening <body> tag.

To bind your controller to the <body> section of your Web page by using the ng-controller attribute, update your <body> tag as follows:

    <body ng-controller="firstController">
Applying the ng-controller attribute to an HTML tag tells Angular that the controller will work on that particular section of the view. Just like the ng-app declaration, ng-controller can be used on lower level elements as well. In this case, we have defined it on the <body> tag so the entire HTML body will be controlled by this controller. You will learn more about Controllers in a later module.

Locate the <h2> tag that you created previously. This is where you are displaying the text content "Hello from AngularJS"

Below the line containing the "hello" message, to reference the value of the scope variable you set in firstController, enter the following code:

    <pre>{{appName}}</pre>
At this point your helloworld.html file should look like this:

alt text
Browse to your page and you should see the following.

alt text
If you need help please review the Module Creation document.

# Curso   Module 1: Getting Started with Angular   Tutorial Lab: Implementing Dependency Injection   To Declare a Constant

## To Declare a Constant
 Añadido a marcadores
To Declare a Constant

In the previous lab, you used ng-controller to bind your controller and its dependencies to your HTML. Your application code declared a dependency on $scope and Angular used an injector to take care of the rest. Angular will also invoke certain functions, such as services and factories, via the injector. In order to properly demonstrate the concept of Dependency Injection, we are going to create our own dependency, and then inject that into our controller. You will learn more about Dependency Injection in the following units. We will start things off by using the simplest thing you can inject into a controller, the Constant.

A constant is used to hold static values. It is most useful in an application with multiple controllers, if you want to only define a property in one place. It can then be injected into any controller.

In your helloworld.html file, locate the <script></script> tag that is used to define your app module.
    <script></script>
    
        var helloWorldApp = angular.module('helloWorldApp', []);

Below the code line defining helloWorldApp, to create a new constant for your app named myConfig, enter the following code:

   helloWorldApp.constant('myConfig', {applicationName:'My Angular JS App'});
A constant can either be a single value such as a string, or an object. It can't be a function, and shouldn't have any logic of its own, since it's a very isolated component. In this case we have chosen to use an object with a single property.

Save your file.

That's it! You've created your first component ready for injection into your controller.

In the next unit, you will inject this value into your controller and use it in your app. 

# Curso   Module 1: Getting Started with Angular   Tutorial Lab: Implementing Dependency Injection   To Inject a Dependency

## To Inject a Dependency
 Bookmark this page
To Inject a Dependency

At this point, we have created our own dependency - now it's time to use it. In order to do so, we need to tell the controller that this particular dependency is needed for the logic within the controller to function. By adding it to the list of dependencies, Angular will make it available to the controller automatically when the controller is invoked. This is what Dependency Injection is all about. 

Note: For additional information on Dependency Injection, please see this Wikipedia Page. For a deep dive of Angular Dependency Injection, please see the Angular Documentation.

If it isn't already open, use Visual Studio Code to open your Mod1Lab folder.

Open your helloworld.html file, and then, in the <body> section, locate the code used to create your controller.

Inside the array brackets [], before the function declaration, to declare a dependency on 'myConfig', update your controller as follows:

helloWorldApp.controller('firstController', [
    '$scope', 'myConfig',
    function($scope, myConfig){
        $scope.appName = 'An App Name';
    }
]);
Just like when we declared $scope as a dependency into this controller, we have told Angular to load the myConfig constant that we created in the previous lab. 

Note: Notice that the dependency myConfig has been included twice; once as a string literal and a second time as an object parameter. The string literal is included for minification purposes, and tells the minifier that the 'myConfig' object is being injected, but it can rename the myConfig variable to a shorter name.
Change your $scope.appName variable to utilize the injected value.

helloWorldApp.controller('firstController', [
    '$scope', 'myConfig',
    function($scope, myConfig){
        $scope.appName = myConfig.applicationName;
    }
]);
We have now replaced the $scope value we previously defined in our view with the value we defined in our injected constant. In this case, applicationName is the property of the constant we have created. If the constant were a single value instead of an object, you would simply use $scope.appName = myConfig
Your completed helloworld.html file should look similar to the following:

Part 3 helloworld.html
Save your file, then Use File Explorer to open your Mod1Lab folder.

Open your helloworld.html file in a browser. Your page should now look like the following:

Part 3 Screenshot
Congratulations! You have created and injected your own dependency into your app. You can use Dependency Injection to make single components for multiple controllers to use, while keeping your code clean and consistent.

If you need help please review the Introduction to Dependency Injection document.

# Curso   Module 1: Getting Started with Angular   Self-Assessment Lab: Angular Fundamentals   Lab Overview

## Lab Overview
 Bookmark this page
Lab Overview

In the previous labs, we walked you through building your first Angular application. For this self-assessment lab, you will build your own basic Angular JS application to display the current date on the screen.

When you are finished, your completed lab assignment should look similar to the following screenshot:

completed self-assessment lab

# Curso   Module 1: Getting Started with Angular   Self-Assessment Lab: Angular Fundamentals   Lab Requirements

## Lab Requirements
 Bookmark this page
Lab Requirements

These are the requirements to complete the self-assessment lab. Use these requirements to guide the construction of your application. If you get stuck, refer back to the lab or course material to help you along. We have written the requirements as a user story. 

Note: User stories are used in the Scrum software development methodology. Scrum is an iterative approach to software development. Read more about Scrum and User Stories.

Task: Construct a basic Angular application to display the current date on the screen.

User Story:

As a user, I want a web page that will display the local date and time so that I can always be on time.

Acceptance Criteria:

Have an HTML file for the view (i.e. index.html)
Load the Angular library in a script tag
Declare an Angular module
Declare an Angular Controller
Use ng-controller to bind the Controller to the View
Use an Angular Expression to bind the date value to the View
Use the JavaScript Date Object to generate the date.
Use Dependency Injection to get the date value from the constant.
Note: In this module, you placed all your JavaScript in your HTML file between <script> tags. In future modules, you'll be creating external JavaScript files and injecting those. The principles are exactly the same but the JavaScript just lives in external files. If you would like to use external files for this Self-Assesment, feel free to give it a try. Instead of putting the JavaScript in your HTML, simply create an external file with a .js extension and copy and paste the JavaScript (everything between the <script> tags) into that file and use dependency injection to include it in your controller.

TIPS:

Be sure to put your declarations in order (Angular, then App declaration, then constant, then controller. This will ensure you have no errors.
Since this is a fairly simple application, it would make things easier to keep everything in the same file. For more involved applications using external JavaScript files organized into sub-folders is useful.
Remember - When you are done your application should look something like this:
completed self-assessment lab assignment