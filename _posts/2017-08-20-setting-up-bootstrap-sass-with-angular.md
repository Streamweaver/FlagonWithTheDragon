---
layout: post
title: Setting Up Bootstrap Sass with Angular
categories: [tech]
tags: [coding, angular, bootstrap]
---
I had a tremendously difficult time getting bootstrap to work under sass and no single set of install directions worked for me so I wanted to capture the process I finally got to work here.  First, as of this writing, I couldn't get bootstrap 4 with sass to work after a very long time trying.  I kept getting popper.js errors and the nav just never worked so I backed out and went with bootstrap 4.  As of this writing bootstrap is at version 4.0.0.6-beta which may explain some of the problems.

### Dependencies

This assumes you have the following installed already.
* [node.js](https://nodejs.org/en/)
* [angular-cli](https://github.com/angular/angular-cli) globally via: `npm install -g @angular/cli`

### Start a new angular project

via angular-cli:
  ```shell
  > ng new <projectname> --style=scss
  > cd <projectname>
  ```
### Install bootstrap-sass and jquery

via npm from <projectdirectory>:
```shell
 > npm install bootstrap-sass jquery@latest --save
```
### Import Styles and Setup Variables.

Setup the file ~/src/app/_variables.scss and import it and the bootstrap styles into ~/src/app/styles.scss at the top:

```scss
  @import 'variables';
  @import '../node_modules/bootstrap-sass/assets/stylesheets/_bootstrap';
```

### Add Jquery and boostrap.js

In the file .angular-cli.json modify the "styles" array as follows:

```json
      "scripts": [
        "../node_modules/jquery/dist/jquery.min.js",
        "../node_modules/bootstrap-sass/assets/javascripts/bootstrap.min.js"
      ],
```

### Conclusion

I'm very new to Angular 4, and all this discovery came after just a day or so of doin tutorials so it's a fair thing to say that I'm sumbling around in the dark.  Not sure that can be helped though, even with as mush experience programming as I have, these 'automagic' build tools can be difficult to figure out and I think the tooling around Angular right now has a long way to go.  Further complicating things are the split between both angular information (still a lot of angular js stuff floating around) and Bootstrap 4 is still in beta.  

As I progress and get more use to the framework I'll try to loop around to a post in the future with whatever updated knowlege I pull together then.  I'm just putting this up now so I can note it for myself for future use and in case it's useful for anyone else.
