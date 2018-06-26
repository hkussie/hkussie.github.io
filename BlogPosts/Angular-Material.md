## Creating a sleek, professional looking  UI using Angular Material  
---

This tutorial explains how to apply the fundamental directives provided by Angular Material to create an Instagram inspired UI layout. Angular Material is a particularly helpful framework for generating beautiful UIs for a number of reasons, among them being the minimal amount of effort needed to create comprehensive UI components that work across desktop, web and mobile devices.

** Required for this tutorial: ** A package manager of some sort. I used bower for this particular tutorial, however, npm and other package managers are perfectly fine for developing with Angular Material. With that being said, the following commands will install all of the Angular Material directives needed for this tutorial:

```
bower install angular
bower install angular-material
bower install angular-messages
bower install angular-aria
bower install angular-animate
```
---
Once you have run these git commands, you should then include your newly acquired dependencies in the head tag within your index.html page:

```html
<head>
  <meta charset="utf-8">
  <title>Generic Application</title>
  <link rel="stylesheet" href="bower_components/angular-material/angular-material.min.css">
  <link rel="stylesheet" href="Styles/style.css">
  <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
  <script src="bower_components/angular/angular.min.js"></script>
  <script src="bower_components/angular-animate/angular-animate.js"></script>
  <script src="bower_components/angular-aria/angular-aria.min.js"></script>
  <script src="bower_components/angular-material/angular-material.min.js"></script>
  <script src="Modules/module-1.js"></script>
</head>

```
---
Now that our dependencies have been embedded into our html page, we can begin to build our layout. The first step in creating our project, is to initialize Angular and Angular Material within our project. Inside my Modules folder, I have created a file called module-1.js which is where we will initialize Angular, and inject Angular Material into our project. Our file should look something like this:

```js
  'use strict';

  angular.module('myApp', ['ngMaterial'])

    .controller('headerCtrl', ['$scope',
    function($scope) {
        $scope.header = "PictureBoard Application";
    }]);

```
---
Lets now take a look at some of the directives necessary for creating our layout. The first directive that we'll make use of will be Toolbar. The Toolbar directive, (md-toolbar), is usually inserted above the content area, and can be thought of as a place holder for the header within our page. When put into our page, it should look something like this:

```html

<md-toolbar>
  <h1 class="header" ng-controller="myCtrl">{{header}}</h1>
</md-toolbar>  

```
---
Now that we have our header in place, lets create the structure of our layout. The directives that we'll be making use of throughout the layout of our page include: the content directive, the tabs directive, and the card directives. All of our content will fall within the directive content, which manifests itself as the md-content tag. The content directive is a container element most useful for scrollable content. Angular Material does this by setting the CSS overflow property to auto so that content can properly scroll.

The next directive that we'll be working with is the tab directive. The tab directive will serve as a method for generating headers within our user profiles. Within our newly created tab, we will make use of the card directives to create the components for our user profiles. Within the md-card tag, we will utilize the md-card-header, md-card-title, md-button, and md-card-avatar directives to create the specific components of the user profile. Using these directives will give us a profile picture, caption, like button, and comment button. Your code should look like the following:

```html
 <md-card>
    <md-card-header>
        <md-card-avatar>
            <img class="md-user-avatar" src="Images/UserPic(1).png">
          </md-card-avatar>
          <md-card-header-text>          <span class="md-title">Lorem ipsum</span>
          <span class="md-subhead">Dolor sit amet</span>
        </md-card-header-text>
    </md-card-header>
</md-card>      
```
This piece of code will give us a generic user profile, and can be repeated as many times as you'd like. The end product should look something [like the following](https://hkussie.github.io/AngularMaterial-UI-Application/)! 
