---
layout: post
title: Frontend Tools
categories: [JavaScript, Tools]
---

Summarize my knowledge about the most popular JavaScript package managers, bundlers, and task runners.

## 1) Module Bundlers

*webpack* and *browserify* as popular ones, work like task runners but with more flexibilities, bundle everything together.
Work for larger project, might be more overhead if application is small.

Brief history of the Dependency Graph
```html
<script src="jquery.min.js"></script>  
<script src="jquery.some.plugin.js"></script>  
<script src="main.js"></script>
```
Bundle everything
```js
// build-script.js
var scripts = [  
    'jquery.min.js',
    'jquery.some.plugin.js',
    'main.js'
].concat().uglify().writeTo('bundle.js');

// Everything our app needs!
<script src="bundle.js"></script>  
```

### webpack

![webpack-flow]({{ site.baseurl }} /images/JavaScript-Foundation/webpack-flow.png)

* Module bundler
* Recursively builds a dependency graph and includes every module into 1 bundles
* Four Core Concepts: entry, output, loaders, and plugins.
* Dead asset elimination.
* Easier code splitting.
* Control how assets are proccessed.
* Stable production deploys
* Works well with React
* More [here](https://webpack.js.org/concepts/) and [here](http://blog.andrewray.me/webpack-when-to-use-and-why/)

### browserify
* Allows node.js style modules in browser
* Export and require
* More [here](http://blakeembrey.com/articles/2013/09/introduction-to-browserify/)

## 2) Task Runners

*gulp* and *grunt*, creating tasks and run them whenever you want, for example you install a plugin to minify your CSS and then run it each time to do minifying.

Common tasks:
* Used for automation on time-consuming and repetitive tasks
  * Minifying, concatenating, and cleaning up CSS and JS
  * Cache busting
  * Running unit testing
  * Linting code for errors
  * Compressing images
  * Sending updates to a production server
  * Updating databases
  * Compiling LESS files
  * Optimization
  * etc.
* Check for new files or changes to files in certain directories
* Uses Node.js and js files to build tasks


Major differences is how they accomplish them

### gulp

```js
gulp.task('jpgs', function() {
    return gulp.src('src/images/*.jpg')
    .pipe(imagemin({ progressive: true }))
    .pipe(gulp.dest('optimized_images'));
});
```
* Designed to use a **Series of plugins** that each do a task.
* Uses JavaScript, easier to write, CODE
* Shorter
* Faster speed, uses streams and handles tasks in memory, handles several tasks at the same time.
* More [here](http://gulpjs.com/)
* 2,774++ Plugins [here](http://gulpjs.com/plugins/)
* 26,802++ Stars [Github](https://github.com/gulpjs/gulp)

### grunt

```js
imagemin: {
    jpgs: {
        options: {
        progressive: true
        },
        files: [{
            expand: true,
            cwd: 'src/img',
            src: ['*.jpg'],
            dest: 'images/'
        }]
    }
}
```

* Accomplish multiple tasks at the same time.
* Uses CONFIGURATION files similar to [JSON](http://www.json.org/)
* Longer. Have to **declare source and destination files** for every task.
* Normally only handle one task at a time
* More [here](https://gruntjs.com/)
* 6013++ Plugins [here](https://gruntjs.com/plugins)
* 11,491++ Stars [Github](https://github.com/gruntjs/grunt)

![grunt-vs-gulp-speed]({{ site.baseurl }} /images/JavaScript-Foundation/grunt-vs-gulp-speed.gif)
