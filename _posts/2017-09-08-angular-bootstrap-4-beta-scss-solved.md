---
layout: post
title: "Angular Bootstrap 4 beta SCSS Solved"
date: "2017-09-08 00:12:34 -0400"
categories: [tech]
tags: [coding, angular]
---

I've had some problems getting the bootstrap 4 beta scss npm package to work with Angular 4 (angular/cli actuall) and found the solution to the issue today.  I missed a detail in the bootstrap documentation to use the jquery-slim verion and had been using jquery-min instead.  The webpack error thrown wasn't particularly helpful and gave me back something about undefined value.  Well, forget all that and if you get an error, hop over and check to make sure you're importing the jquery.slim.js file before banging your head against a wall.

So to have a complete set of instructions for using Bootstrap 4 Beta in an Angular 4 project.

Install dependencies via npm:
```bash
npm install --save bootstrap@4.0.0-beta jquery@latest popper.js@latest
```

*Note that in this version tether is no longer required, you can uninstall it if upgrading.*

In `styles.scss` import bootstrap and a local _variables.scss file (wherever you put it):

```css
@import '../node_modules/bootstrap/scss/bootstrap';
@import 'sass/variables';
```

Register the javascript files in `.angular-cli.json`
```json
...
      "scripts": [
        "../node_modules/jquery/dist/jquery.slim.js",
        "../node_modules/popper.js/dist/umd/popper.js",
        "../node_modules/bootstrap/dist/js/bootstrap.js"
        ]
...
```
*Again, not the jquery.slim.js import*

That's it, it should now work.