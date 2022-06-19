# Build tools: What's it called?
At some point in your web development career, you have inspected one of your favourite websites with the developer tools of your browser. Then when you scroll down you see the script tags where the source files are called with names like `65e027f.js`. And you are wondering: 'why would you ever call your javascript file this?'. Well you don't... It is done by a module bundler or another build tool that automates complex tasks you don't want to do by yourself.

## Gulp
Gulp is one of the most popular and most used build tools out there. Gulp is a task runner that automates tasks that repeat a lot and you don't want to do yourself. Especially for complex and slow tasks Gulp is an excellent solution. 
Being a Node.js app, you can simply define your tasks by writing javascript, so you don't have to adapt to a new syntax. 

### Ease of use
In Gulp you can create pipelines which is a list of tasks that you want to run within the same operation. Each task therefore is its own asynchronous function. You can simply chain these tasks or group them with Gulps `series()` and `parallel()` functions respectively. You build operation would look something like this then: 

<table>
<tr>
<td>

```javascript
const { parallel } = require('gulp');

function javascript(cb) {
  // Run your tasks
  cb();
}

function css(cb) {
  // Run your tasks
  cb();
}

exports.build = parallel(javascript, css);
```
</td>
<td>

``` javascript
const { series } = require('gulp');

function javascript(cb) {
  // Run your tasks
  cb();
}

function css(cb) {
  // Run your tasks
  cb();
}

exports.build = series(javascript, css);
```
</td>
</tr>
</table>

#### Files
When working with files in Gulp, there are probably some tasks that you want to run on the file after each other. Using the `src()` and `dest()` methods, you can call a file, run some tasks and then output the processed file to another destination. In between you can execute any process you want by chaining the `.pipe()` method. For example when compiling your JavaScript: 

``` javascript
const { src, dest } = require('gulp');
const babel = require('gulp-babel');

exports.default = function() {
  // The asterix is a wildcard which means every file with '.js' extension
  return src('src/*.js')
    .pipe(babel())
    .pipe(dest('output/'));
}
```

### Optimisation
I have used Gulp as task runner to optimise the performance of my web-application. Using Gulp I was able to make image-files smaller and compile my JavaScript to code that can run on any browser. Gulp allows for external libraries, called plugins, to enter the process and access, modify and compile files so you can automate everything that you want. 

#### Javascript
Using Babel, you can compile your ES6 JavaScript to ES5 so it works on every browser, but included with the new JavaScript functionalities. It will output a completely working JavaScript in both ES6 and ES5 syntax.

#### Assets
With a plugin like `image-min` you can minify your images on the website without losing too much quality that it will be visible. You can optimise an entire directory of images at once. These assets can be drastically reduced in size, which means that you don't have to download so many data anymore. 


### Bundling & building

#### Javascript
When writing a lot of JavaScript, a module approach may come in handy. But when deploying and serving all your JavaScript, more files means more downloads, bandwidth and data. Then bundling all your files into one and minifying it reduces the amount of data that needs to be downloaded. Additionally you can also choose the way it will be bundled; in the commonJs way or using modules. Build tools like Webpack, Rollup.js and Parcel can bundle your Javascript to one file. That file can be named whatever you want, but by default, it will generate a name. That is why you have probably seen those weird script names mentioned in the beginning of this article. 

#### CSS
CSS, just like JavaScript, can be structured in different files. And just like JavaScript, it can save data when bundling and minifying those files. Then you also have pre-processors like Sass, which give you extra functionalities to CSS which vanilla CSS doesn't have. Then you need to process the files to vanilla CSS.

## Other popular build tools
So Gulp is pretty incredible and can be used for a lot of automation of tasks but before you do this you want to get yourself familiar with what build tools are; What do they do? And which ones are out there? Every build tool aims to give the developer a better experience, but not always do you need a build tool to get you your better developer experience. You have to know what you need for your project in order to select build tools that will actually help you work more efficient or make things easier. Therefore, first understanding your project and how all the technical aspects work under the hood is a great advantage when exploring this world.

A list of other kinds of build tools: 
- Package managers (like npm or yarn)
- Transpilers/compilers (Babel, TypeScript, Dart)
- Bundlers (Webpack, Parcel, Rollup.js)
- Minifiers (Uglify, minify)

## Sources
* [FreeCodeCamp.org](https://www.freecodecamp.org/news/making-sense-of-front-end-build-tools-3a1b3a87043b/)
* [DeveloperExperience.io](https://developerexperience.io/practices/javascript-front-end-build-tools)
