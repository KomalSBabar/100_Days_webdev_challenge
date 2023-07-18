
#Moderns Incomplete Guide to Navigating the JavaScript Landscape
-> The core language sometimes referred to as vanilla Javascript or Vanilla JavaScript
-> The browser specification of the Javascript language is ECMAScript
-> when people say then use ES6,ES2015,ES2017, ES 2020 etc.. refers to the use of features defined in ECMAScript, but no necessarily supported by modern browsers
Using ECMAScript usually means also using Babel.js to make it work in current browser implementations.
-> TypeScript is mostly used in modern javascript it has .ts file extension 
->The moderb web runs on javascript frameworks React , Vue , Angular (Javascript Frameworks allowing us to write Javascript - based front - end applications )
->with javascript framework comes build tools such as (npm,WebPack,Gulp) build tools and infrastructure to automate the process of optimizing human - readable Javascript for the best browser performance
->Javascript is used for frontend and backend aswell from some past years 
-> Node.js - Javascript server runtime used to run JavaScript everywhere;used to run npm, Webpack, Babel, and more .
-> javascript is core underline language.


#Tools for working with javascript
-> modern browser - ideally all browser for testing
-> Code editr - Visual studio code 
-> Live server environment - extension to VScode or similar(Ritwick Dey)
-> The browser console  - available in most browser

#Formatting and Linting
->download extension in VSCode -> (ESLint and Prettier code)  
          - this make a code a look pretier to human eye 
          - it helps automatically clean up your formatting
          - it looks clean when working with code.
         - ESLint helps automattically detect coding errors and can do basic cleanup automatically
         - Both require Node.js

-> Downloaded Node.js 
        
#Javascript language basics

#Javascript as an external file

#Modern Javascript loading

->  Default Behaviour
    Browser stops rendering when javascript is encountered. Javascript is executed before rendering continues.Often referred to as content blocking.

    <script src="JS/script.js"></script>

     -Html parsing                           Html parsing
                   JS download
                               JS execution

->  Using Async Keyword
     async keyword changes this behaviour significantly
     it tells browser when your downloading js file keep parsing the html file then execute the js file then continue with parsing of html file.
     this dramatically shorten the time it takes the browser to execute everything and it doesnt create this huge render blocking issue.
     this is good for some purpose such as  use when we need the js parse as quickly as possible any really dont care about rendor blocking.
     Browser downloads Javascript in parallel while HTML renders. When Javascript is fully loaded, rendering stops while Javascript is executed.

    <script src="JS/script.js" async></script>

    -Html parsing              Html parsing
      Js download
                  Js execution

->  Using defer Keyword
    in some circumsentence we need to make sure the browser only executes the JS , after the document is complete for that we have defer keyword
    Browser downloads JS in parallel with HTML renders, then defers execution of Javascript until HTML rendering is complete.

      -Html parsingHtml parsingHtml parsingHtml parsing          
                  Js download
                                                        Js execution


->async/defer should be standard way of loading javascript today.
   Only use render blocking when you have a specific reason.Loading Javascript in the footer is now an anti-pattern.
   Foe here on forward Javascript should always loaded in the head and then use async or defer when that Javascript is executed on the document


#Javascript modules
-> a file gets really large file and lot of code in one page so  it requires lot of scrolkling so for this problem we have solutionas Javascript Modules. 
   Javascript modules allow us to break pieces out of a JS file and place them in a separate file and import them back into the original file again.
   we have use import and export in JS 

   file 1 
   we defined the constant backup and exported 

   file 2
   we import the backpack from file1 amd used here 

   if we work with react or any framework this is the practise and used 

   ->and you have to loaded the both js file in main page 


#Objects : A practical introduction

-> Javascript is prototype based Object Oriented programming language. that means as its core , when we work with Javascript we are working with objects that are based on the prototypes.
-> an Object in JS is preety much the same as object in real life, expect it's written in code  instead of created as physical object.
-> methods - property-changing features inside objects.


#Objects : code version

-> A Javascript object is a collection of data and functionallity stored as propertys and methods that describes the object and what it can do.
-> const backpack; //variable holds data.
   const backpack = {}; //Curly brackets define data as an object. //this curly bracket says this is a javascript object and currently the JS object is empty. So i need to populate my object with some data. this is done using some properties.

   const backpack = {
        name: "Everyday Backpack", // each properties is defined using key- value pairs separated by colon (,).
   };
                             
-> Properties can nest sub - objects with their own properties.
-> "this" keyword refers to the current object.
-> use camelCase property names to avoid issues.


#Acessing objects

console.log("The backpack object" , backpack);

#Acessing objects properties
*using dot (.) notation
console.log("Strap  length :", backpack.strapLength);
console.log("Strap  length left :", backpack.strapLength.left);

*using brackets [] notation 
using bracket notation it gives us more control and allow us to do advance things.

var query = "pocketNum";
console.log("The pocketNum value :", backpack[query]);





QUIZ
Q1. When does the browser execute Javascript?
Ans : When the script is encounterd if the script is set to "async", when the script is fully loaded. If the script is set to "defer", when the entire HTML page is rendered.
Q2. What happens when you defer Javascript?
Ans: The browser loads the Javascript asynchronously when it is encountered , then waits until all HTML is rendered before executing the script.

Q3. Javascript modules are heavily used in frameworks like React and Vue. What is the advantage of using modules?
Ans : Modules enable modularization of code where individual functions, components, data objects, and other parts can be separated into individual files.

#Practice 1 
 1) Give each object an identifiable name.
 2) Create properties to describe the objects and set their values
 3) Find an object that has another object inside of it to create a nested object.
 4) Test your objects in the browser console by accessing the entire object and its specific properties.

 


 #Object Methods

 #Practice 2 build new method
 1) Create new methods in this objecr to change each property 
  key reminds: - pas value to a function inside the parenthesis.
               - Refer  to the current object as "this"
               - Assign any value to any property


#Classes: Object blueprints 
