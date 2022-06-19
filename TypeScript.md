# Typescript: what’s not to love?

## What is TypeScript?
Typescript is becoming more and more popular. Developers are getting used to it and have begun to love it so much that it is much praised over the world. But why? Are they right or is it just some hype? 
TypeScript is open-source but the compiler is mainly developed by Microsoft, the company behind windows and also VSCode, the most popular code editor.
TypeScript is a superset of JavaScript, which means that it adds functionality and a more extensive way of writing javascript, though regular javascript is also valid within the TypeScript language. It compiles down to regular JavaScript, so when you build your web application, it can run in any environment that supports javascript. This makes it a really reliable and solid extension to write your code. 

Now since they turn basically into the same code with the same result, you might be asking yourself: ‘Why would I use TypeScript over regular JavaScript?’.

## TypeScript goals
TypeScript has 11 design goals to define which way to go. They all aim towards helping the developer write reliable and safe code easily and they achieve this in a few ways.

- Static typing en type inference
- IDE support
- Modern JavaScript features
- Gradually adaptable

## Static typing & type inference
So JavaScript is dynamically typed, this means that a variable can have any type until it is instantiated. In some cases with more complex code, you assume that you get a certain type of variable while it actually being something else. These type errors can be easily avoided by defining your variable type. 

In TypeScript you can type your variables in the following way: ` let dog : string = ‘Bello’ `. This way, whenever the variable dog is called or mutated, is has to be or become a variable of type ‘string’ or it will throw an error. In the same way you can type functions and object structures to only return or contain certain types of variables. To make things easier TypeScript also has type inference which automatically types your variables when declared. That is why they say TypeScript is ‘optionally’ typed, because you don’t have to define a type, it can do it automatically. 
While it seems like you have to do a lot of extra typing with every variable you have, in the longrun, this will make your app be less prone to errors en more reliable for release. 

## Integrated IDE support
So a lot of extra work and a lot of errors have happened so far because of the typing. How is this helping me write more reliable code? Well, TypeScript integrates really well with code editors, so it can read your variables and their types and makes them available for your code editor. In VSCode for example, while coding and using a variable or referring to it, you immediately get a popup with suggestions, properties and/or errors that will happen if you run the code like you wrote it. 

<img src="https://i.postimg.cc/66Mx0R6F/code.png" alt="Object typed with TypeScript" width="400px" />

![Properties popup when referring to object in VSCode using TypeScript](https://i.postimg.cc/1XrtCztJ/Screenshot-2022-06-17-at-13-12-58.png)

Direct feedback is a great way of helping you write that more reliable code without having to compile the code first and see which error you get. Instead you can write your code, see which errors will occur and when finally running your code, you should have a clean running app.

## Adaptation
As said, TypeScript is a superset of JavaScript, so regular JavaScript is also valid in TypeScript. If you want tot learn TypeScript, you can do so by slowly starting to use it in projects. Start off small by typing your variables en work your way up to complex objects and classes. To convert a JavaScript file to TypeScript, you can simply change the `.js` extension to `.ts` and you have a working TypeScript file. In the future TypeScript will help you write reliable code, but for now, it is just another tech that complicates your life as a developer.

## Sources
* [StackOverflow](https://stackoverflow.com/questions/12694530/what-is-typescript-and-why-would-i-use-it-in-place-of-javascript)
* [TypeScriptlang.org](https://www.typescriptlang.org/)

