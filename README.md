# Website Performance Optimization Project

Welcome to my Udacity FEND project, where we apply best practices to achieve a PageSpeed score of 90+ and optimal scrolling / resizing on pizza.html

### Use

To see access the website, just use this link here: https://learnathoner.github.io/Optimization_Project/

### Process / Tools Used

The optimizations were made using:
  * **Npm**
  * **Gulp**
  * **Google's Web Starter Kit** - A simple template with options for liveReloading, transpiling ES6, a built in server, and optimizations.
    * Url: https://developers.google.com/web/tools/starter-kit/
  * **Inliner** - Minifies, strips whitespace, and compiles JS/CSS/HTML into a single file to reduce requests
    * Url: https://github.com/remy/inliner


### Optimizations Made

* **HTML** - To achieve a PageSpeed score in the 90's, the following changes were made to the html:
  * Font request was changed to an @font-face and added to CSS
  * Split CSS by Media type
  * JS requests changed to async
  * Image optimization
  * Minifying and inlining
* **JS**
  * **function changePizzaSizes** - Removed layout calculations from loop, instead calculating size once and applying to every element.
  * **function updatePositions**
    * Removed style calculation from updatePositions
    * Added movement calculation to separate loop, since there are only 5 options and it was being calculated for every pizza container
  * **document.addEventListener('DOMContentLoaded')** - Lowered background ".mover" count from 200 to 24 to match visible amount.
  * Changed querySelectorAll's to getElementsByClassName
