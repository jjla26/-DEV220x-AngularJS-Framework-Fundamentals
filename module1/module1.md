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