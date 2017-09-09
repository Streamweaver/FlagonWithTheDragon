---
layout: post
title: "Angular-CLI and Bootstrap 4 SCSS Retake"
date: "2017-08-25 00:12:34 -0400"
categories: [tech]
tags: [angular, bootstrap]
---
Setting up Bootstrap 4 to work with Angular-CLI turned out to be WAY easier than what I had been trying to do in my [previous post]({{ site.baseurl }}{% post_url 2017-08-20-setting-up-bootstrap-sass-with-angular %}).  The info I had been finding was way off track and I think (like me) they were confused between the static and scss portions of bootstrap 4.

First, go ahead and setup your angular-cli project with the style option `--style=scss` or just convert your poject by setting the appropriate line in `.angular-cli.json` (google it hippies).

From porject folder npm install bootstrap 4.  Command below reflects version at time of writing but check the bootstrap 4 site for current command. 
  ```
  npm install bootstrap@4.0.0-alpha.6 jquery@latest tether --save
  ```

Create your own file for variables wherever you like and import it into the root styles.scss file.  I created mine in `scss/_variables.scss` 

Import your variables file and the bootstrap scss file into `src/styles.scss` like so:
```scss
// My own variables file.
@import 'scss/variables';

// Load the main bootstrap file
@import '../node_modules/bootstrap/scss/bootstrap';
```

If you want to test it, set a variable in your local file with something like `$body-bg: red;` and reload the page and you'll know if it's working.

You'll want to import the javascript files as usual in angular-cli.  For that just open `.angular-cli.json` and add them to the scripts property like so:
```json
      "scripts": [
        "../node_modules/jquery/dist/jquery.min.js",
        "../node_modules/tether/dist/js/tether.min.js",
        "../node_modules/bootstrap/dist/js/bootstrap.min.js"
      ],
```

That is pretty much it!  Bootstrap does the importing for you of all the sub-components.  Likely there is more but this is MUCH more clean that the method I previously posted about so I wanted to update.