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
