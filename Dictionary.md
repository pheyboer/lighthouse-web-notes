# Dictionary of Terms and Notes

### Odin Project
  - https://www.theodinproject.com/paths/foundations/courses/foundations#javascript-basics 

## Lecture Notes
  * Objects  https://github.com/andydlindsay/sep16-2024/tree/main/w01d03
  * Callbacks  https://github.com/FrancisBourgouin/lectures-web-ft-sep16-2024/tree/main/w1d4
    - https://vimeo.com/1015946338/633db77663
    - https://github.com/andydlindsay/flex-sep23-2024/tree/main/m01w02-2
  * TDD 
  * Asynchronus Control Flow https://github.com/andydlindsay/sep16-2024/tree/main/w02d02
  * Networking 
    - Part 1: https://vimeo.com/1012900013/6c1c4c8c17
    - Part 2: https://vimeo.com/1012899907/ee980ed2ae?share=copy 
  
## Test Topics
 - Test 1:
    - Count numbers in Array
    - Sum numbers of Array - can use ```.reduce```
    - Find the mean of an Array
    - Find the minimum Value of an Array
    - Find the maximum value of an Array
    - Find the range of an Array - can use ```.sort```
    - Find the meadian value of an Array
    - Find the Mode of an Array
    - Find the Standard Deviation of an Array
    - Review of test 1: will use ```.sort``` on test 2
  - Test 2:
    - All of test 1 topics
    - Functions as Objects
    - Comparisons (how to tell if two arrays are equal)
    - Callbacks
  - Test 3:
    - Test 1 and 2 topics


## Recipe
  - Clarify Question
  - Define Inputs
  - Define Outputs
  - Prcoessing and Logic
  - Break code down into small steps - incremental solutions
      - Write out pseudocode for each step


 ## VSCode Shortcuts
  https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf

 ## Git Shortcuts
  https://education.github.com/git-cheat-sheet-education.pdf

 ## Git Cloning and Commiting
  - Go to directory
  - ```git init``` to create new git repository
  - Make sure git is initalized (be careful for nested Git Repositories)
  - ```git clone <SSH URL>``` always use SSH
  - ```git status```
  - ```git add <file name>```
  - ```git commit -m "Commit Message"```
  - ```git push```
  - Double check branches and origin

  ### For Lighthouse Labs Testing
 - Git clone
  - Go to directory
  - Get token from Compass
  - ```npm run start-exam [exam token]```

 ## Markdown shortcuts
 https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet

 ## Javascript Cheatsheet
 https://htmlcheatsheet.com/js/

 ## Vim CheatSheet
 http://www.viemu.com/vi-vim-cheat-sheet.gif


  ## Variables
  - var - function scoped or globally scoped
  - let - block scoped (inside loop or conditionals)
  - const - block scoped

 ## Terms
   ## Scoping
  - Global - variable declared outside any function or block. Accessible anywhere
  - Function - variables declared within a function are scoped to that function. Accessible only within function
  - Block - variable confined to the block {} in which they are declared such as within 'it' or 'for'. Accessible within block

  - ## Pseudocode 
```js    
Loop from 100 to 200:
  Let num = the current step in the loop
  If num % 3 is equal to 0 and num % 4 is equal to 0:
    Print "LoopyLighthouse"
  Else if num % 3 is equal to 0:
    Print "Loopy"
  Else if num % 4 is equal to 0:
    Print "Lighthouse"
  Otherwise
    Print num
  End if
End loop
```

 # How we write a function
```js  
  function myFunction(a, b, c) {
    return a + b + c; }
```

 # Object Iteration
 - Properties rea Key-Value pairs associated with an Object
```js
const person = {
  name: 'Alice',
  age: 30,
  isStudent: false
};
Object Constructor:

javascript
Copy code
const person = new Object();
person.name = 'Alice';
person.age = 30;
person.isStudent = false;
```
 * ### For Loop C-Style
  - To iterate over the objects in an array
```js
  function printArrayElements(arr) {
  for (let i = 0; i < arr.length; i++) {
    console.log(arr[i]);
  }
}

// Example usage:
const exampleArray = [1, 2, 3, 4, 5];
printArrayElements(exampleArray); 
```


  * ## For...in
  - OBJECTS
  - Iterates over keys (property names)
  - Iterates through ARRAYS AND OBJECTS
  - Loop through keys of object (indexes)
  - Use when you need to access property keys
```js  
const person = {
    name: 'Alice',
    age: 25,
    city: 'New York'
};

for (const key in person) {
    console.log(`${key}: ${person[key]}`);
}
```
```js
const dog = {
  faveToy: 'squeaky ball',
  breed: 'labrador',
  name: 'dioji',
};

for (const key in dog) {
  console.log('value', dog[key]);
}
```

 * ## For...of
  - ARRAYS
  - Iterates over values
  - Iterates through: arrays, strings, maps, sets. NOT OBJECTS
  - Use when you want to iterate over values of an ARRAY
    - if object is not iterable (plain object) ```TypeError```
  - Returns VALUES not keys
```js
const greeting = 'Hello';

for (const char of greeting) {
    console.log(char);
}
```
  - Output: 
```js
H
e
l
l
o
```

 * ### forEach
  - Execute provided function once for each element in the array
  - Can iterate over elements without needining to manage the loop counter
```js
array.forEach(callback(currentValue, index, array) {
    // Code to execute for each element
});
```

  - ```Infinity``` is highest number in JS
  - ```!``` Logical NOT operator
    - Inverts truthiness of a value


# Array Methods
  * ```.push()``` adds new element to end of array and returns new length of array
```js
let arr = [1, 2, 3];
arr.push(4); // arr is now [1, 2, 3, 4]
```
  * ```.pop()``` removes last element from array and returns that element
```js
let arr = [1, 2, 3];
let lastElement = arr.pop(); // lastElement is 3, arr is now [1, 2]
```
  * ```.shift()``` removes first element from array and returns that element
```js
let arr = [1, 2, 3];
let firstElement = arr.shift(); // firstElement is 1, arr is now [2, 3]
```
  * ```.unshift()``` adds element to begining of array and returns new length of array
```js
let arr = [2, 3];
arr.unshift(1); // arr is now [1, 2, 3]
```
  * ```.splice()``` remove or replace element and add new element in its place
```js
let arr = [1, 2, 3, 4];
arr.splice(1, 2, 'a', 'b'); // arr is now [1, 'a', 'b', 4]
```
  * ```.forEach``` executes provided function once for each element in array
```js
let arr = [1, 2, 3];
arr.forEach((num) => {
    console.log(num); // prints 1, 2, 3
});
```
  * ```.map()``` creates new array with results of calling a function on every element in the calling array
```js
let arr = [1, 2, 3];
let doubled = arr.map(num => num * 2); // doubled is [2, 4, 6]
```
  * ```.filter()``` creates new array with all elements that pass the test implemented by provided function
```js
let arr = [1, 2, 3, 4];
let evens = arr.filter(num => num % 2 === 0); // evens is [2, 4]
```
  * ```.reduce()``` reduce array to a single value. results in a single output value
    - Example: the sum of the elements of an array
    - Reduces an array to primitives
```js    
  let arr = [1, 2, 3];
  let sum = arr.reduce((acc, num) => acc + num, 0); // sum is 
```

  * ```.find()``` returns value of first element of array that satisfies test function
```js
let arr = [1, 2, 3];
let found = arr.find(num => num > 1); // found is 2
```
  * ```.included()``` check if array has a certain value. Returns true or false
```js
let arr = [1, 2, 3];
let hasTwo = arr.includes(2); // hasTwo is true
```
  * ```.sort()``` sorts elements of array. Returns sorted array
    - Very useful
    - modified original array and returns reference to same array
    - uses lexigraphical sorting
    - Sorts in asccending order
    - Can use this to find the Range
    - Single digits will sort correctly, big digits will not -lexigraphical sorting
    - deceding order use ```array.reverse```
    - Accepts function reference
      - Sorted based on relationship between each pair of elements a and b
      - <0, >0, or 0
    
```js
let arr = [3, 1, 2];
arr.sort(); // arr is now [1, 2, 3]

```
```js
    let numbers = [4, 2, 5, 1, 3];

// Sort in ascending order
numbers.sort((a, b) => a - b);
console.log(numbers); // Output: [1, 2, 3, 4, 5]

// Sort in descending order
numbers.sort((a, b) => b - a);
console.log(numbers); // Output: [5, 4, 3, 2, 1]
```

  * ```.join()``` joins element of array intro a string, separated by specified operator
```js
let arr = ['Hello', 'World'];
let str = arr.join(' '); // str is "Hello World"
```
  * ```.reverse()``` reverses elements of array
```js
let arr = [1, 2, 3];
arr.reverse(); // arr is now [3, 2, 1]
```



*  ### Function for Sum of 2 numbers with assertion test
```js
// FUNCTION IMPLEMENTATION
const sum = function (a, b) {
  return a + b;
};

// TEST CODE
console.assert(sum(1, 2) === 3);
console.assert(sum(1, 20) === 3); // bad / incorrect assertion, and we see it fail!
```

* 
* ParseINT - turns string to number
* ParseFloat - for decimals

* Console.assert
  - Static method write an error message to the console if assertion is false. If true nothing happens

* Split
  - ```.split(/\s+/)``` divides string into an array, where each element corresponds to a part of the string that was separated by whitespace.
  - Example:
```js
  
    const trimmedName = "John Doe Smith";
const nameParts = trimmedName.split(/\s+/);
console.log(nameParts); // ["John", "Doe", "Smith"]

```


  # Callbacks
  - A function we pass to another function as arguments
```js  
function greet(name, callback) {
    console.log(`Hello, ${name}!`);
    callback();
}

function sayGoodbye() {
    console.log("Goodbye!");
}

// Passing sayGoodbye as a callback to greet
greet("Alice", sayGoodbye);
```

* Slice process arguments
* Arrays

## Data types
  - Primitive: String, number, boolean, undefined, null, symbol, (bigInt)
  - 7 Fundamental types of Javascript: 6 above plus Objects
  - Reference: Objects, Arrays, Functions
  - Data Types are Primitives OR objects
  - Dot syntax works on nested objects
  - function that doesnt have a return: it will be undefined
  - Primitive types dont have properties
  - Primitive types have corresponding Objects
  


## Objects
  - Key/value pairs
  - The key in an object is always a string
  - In arrays, use index to access a value
  - Use key to access value
  - Array is type of object
  - Object is like a table with 2 columns
  - Object is a bundle of information known as ```state```
  - When property's value is a function, it is called a method
  - Behaviour: what the method does
  - ```this``` refers to the object that the method was called on

```js
  const myObj = {
  firstName: 'Lorem',
  lastName: 'Ipsum'
};

// we have two options for accessing values
// dot syntax
console.log(myObj.firstName); // Lorem

// square bracket syntax
console.log(myObj['lastName']); // Ipsum
```
- Functions inside Objects
  - Objects are key/value pairs. Functions are values. You can store functions inside of an object
  - Reference other properties in an object by using 'this'
  - ```this``` works within context of object
  - ```this``` DOES NOT work with arrow functions
    - reference to the oject where ```this``` is used
```js
const myObj = {
  firstName: 'Lorem',
  sayHello: function () {
    console.log('hello');
  }
};

myObj.sayHello(); // hello
console.log(myObj); // { firstName: 'Lorem', sayHello: [Function: sayHello] }
```  
  - Reference other properties in an object by using 'this'
```js
const myObj = {
  firstName: 'Lorem',
  lastName: 'Ipsum',
  sayFullName: function () {
    console.log(`My full name is ${this.firstName} ${this.lastName}`);
  }
};

myObj.sayFullName(); // My full name is Lorem Ipsum
```
 - Object iteration with ```for...in```
    - Iterate through object's keys. CANT use ```for...of```
```js
const obj = { a: 1, b: 2, c: 3 };

for (const key in obj) {
  // we can use the key to access the value
  const value = obj[key];
}
```

* ## Object Oriented Programming
  - Programming paradigm where we use objects to encapsulate data and behaviour
    - these are properties of the object
    - we do this to reduce duplicated code and to break up code into sensibly divided -
    - OOP by itsself does not require the use of classes
  - A class is a blueprint from which instances of objects can be created
  - Classes have data in the form of calue properties and behaviour in the form of methods
  - classes can inherit behaviour from other classes using the ```extends``` keyword
  - Subclasses can override methods that are inherited in their superclass
  - Javascript gives us ```get``` and ```set``` keywords to define methods that are data getters and setters 
  - OOP software development paradigm
  - popular way to solve code organization, re-use and modularity
  - Javascript is not strictly OO in the way that Java or Ruby are
  - Functional programming is an alternative paradigm
  - classes are most popular way to perform OO
    - Javascripts object system is based on ```prototypes``` not classes
    - Classes added in ES6
  - In OOP classes are templates that we use to create instances of objects
    - A class describes what the object is going to be and we can create new objects using the class
  - To declare a new class use the ```class``` keyword
    - To create a new object from a class use the ```new``` keyword
  - ```constructor``` special kind of method for setting default values for any new objects properties
  - Class pattern allows us to DRY up code by defining the default state and behaviours in one place
  - Classes promote code modularity
    - define a blueprint once and create multiple instances from it
    - each instance inherits properties and methods from the class
      - reduces redundancy
    - Instead of deining multiple object literals with same methods and properties, a class is defined once, and instances created from the class will all share the same method implementation but can maintain different states.
    - The encapsulation of related data and behaviours within a class structure promotes modularity and makes code cleaner and easier to maintain ***
    - OO bundles together state and logic into an object that can be represented into a single variable 
  - Getters: method that retrieves a property value
```js
  const person = {
    firstName: 'John',
    lastName: 'Doe',
    get fullName() {
        return `${this.firstName} ${this.lastName}`;
    }
};

console.log(person.fullName); // Output: "John Doe"

```
  - Setters: allows you to set a property value
```js
const person = {
    firstName: 'John',
    lastName: 'Doe',
    set fullName(name) {
        const parts = name.split(' ');
        this.firstName = parts[0];
        this.lastName = parts[1];
    }
};

person.fullName = 'Jane Smith';
console.log(person.firstName); // Output: "Jane"
console.log(person.lastName);  // Output: "Smith"
```
- Full example:
```js
class Person {
    constructor(firstName, lastName) {
        this.firstName = firstName;
        this.lastName = lastName;
    }

    get fullName() {
        return `${this.firstName} ${this.lastName}`;
    }

    set fullName(name) {
        const parts = name.split(' ');
        this.firstName = parts[0];
        this.lastName = parts[1];
    }
}

const person = new Person('John', 'Doe');
console.log(person.fullName); // Output: "John Doe"
person.fullName = 'Jane Smith';
console.log(person.firstName); // Output: "Jane"
```
  - public vs private setters
  - add information about super keyword
  - Dependency Injection: passing an object the things  it needs rather than having the object access them itself. makes code more modular and testable
  - Single Responsibility Principle - change in one part wont affect other unrelated parts of our app

* ## Inheritance
  - Duplication problem
    - Two classes that share the same behaviour and state information
  - Inheritance: build a new class based on an existing class
    - Remove duplicatoin by moving shared code from two classes into another class
  - ```extends``` superclass vs subclass






* ## Data Structures
* ## Dot Syntax


* ## Function
    Implement a function with example

* ## Arrow Functions
  - Concise way to write functions
  - Annymous by nature
```js
 const add = (a, b) => {
    return a + b;
};
```
```js
const add = (a, b) => a + b; // Implicit return

```
```js
const square = x => x * x; // No parentheses needed for single parameter
```
  - No binding of ```this```
    - Arrow functions dont have their own binding of ```this```
    - Useful for callbacks
```js
function Counter() {
    this.count = 0;

    // Using a regular function would bind 'this' to the function itself
    setInterval(function() {
        this.count++; // 'this' is not the Counter instance
        console.log(this.count);
    }, 1000);
}

const counter = new Counter(); // NaN is printed

// Using an arrow function preserves 'this'
function Counter() {
    this.count = 0;

    setInterval(() => {
        this.count++; // 'this' refers to the Counter instance
        console.log(this.count);
    }, 1000);
}

const counter = new Counter(); // 1, 2, 3, ...

```
  - Use Cases:
    - Callbacks: commonly used in array methods ```.map()```, ```.filter()```, and ```.reduce()```
    - ```.reduce``` callback function on each element of the array, in order, passing return value from calculation on previous element
  - Arrow functions do not have their own ```arguments``` object
  - Not suitable for methods
  - Cannot be used as constructor function

* ## Template Literals
  - Enclosed with backticks ```(`)```
  - Can have multi-line strings
  - String interpolation - dynamic strings
  - Tagged templates

* # Recursion
  - Technique where a function calls itself in order to solve a problem
  - Key components:
    - Base Case: Condition that stops recursion. Without this, function calls itself indefinitely leading to stack overflow
    - Recursive Case: The function calls itsself with modified arguments that bring it closer to the base case 
```js
function factorial(n) {
  // Base case: factorial of 0 is 1
  if (n === 0) {
    return 1;
  }
  // Recursive case: n! = n * (n - 1)!
  return n * factorial(n - 1);
}

console.log(factorial(5)); // Output: 120
```
  - Tail Recursion:
    - Recursive call is the last operation in the function
    - Javascript does not have built in tail call optimization

* ## Command Line Arguments
  - Accessible via the ```process``` object: ```process.argv```
  - Allow you to pass information to your Node.js scripts
  - ```.slice``` to take out parts of the array into a new object array
  - Example:
 ```js 
  const args = process.argv.slice(2); //slice out first 2 command line arguments
const sum = function(numbers) { //create function called sum
  let total = 0;
  for (let i = 0; i < numbers.length; i++) { //loop through array
    total += Number(numbers[i]); // turn string to number
  }
  return total;
};
console.log("Sum: ", sum(args));
```
- Example 2, Tail: use slice to return everything exept first item (head) of array
```js
const tail = function(array) {
  return array.slice(1);
};
```


* ## Linting
 -  Eslint - analyze code for potential errors and enforces standard code
 - Debuggin procedures
 - How to decipher an error message

* ## Higher Order Functions
  - Functions that can take other functions as arguments or return functions as their output
  - Accepting functions as arguments
  - Can return another function

* ## Annonymous Functions
  - Functions that are defined without a name. Used as arguments to other functions, for callbacks
  or when defining functions that will not be reused
  - Useful when function only needed once or for specific context
  - Cannot be called again unless they are assigned to a variable or passed as an argument


# TDD Test Driven Development

* ## Modules
  - Node's way of organizing code into individual files
  - Allows you to resuse functionality accoss different parts of project
  - Dont need to copy paste code
    - Define code once in a module then import whenever needed
    - Reduces redundancy, makes codebase easier to maintain, and minimizes risks of error
  - every js file in node is implicitly a module
  - module.exports tells node what to export from a file. Defaults to {}
  - can use ```require``` with relative paths (doesn't need js extension)
  - ```const sayHelloTo = require('./myModule');```
* Node.js
  - Package manager: npm
    - Packages are self contained code libraries we can install and use in projects

* Unit Testing
  - Tells us if code is working
  - It's just: ```npm test```
  - Writing code that tests other code

```js
// Example of a simple function
function largestNumber(array) {
  return array.reduce((previousValue, currentValue) => {  
    return Math.max(previousValue, currentValue);
  });
}

```
```js
// Example of a test for that function
const array = [1,2,3,4,5];
const largest = largestNumber(array);
assert.equal(largest, 5);

```
-  ### Mocha and Chai 
    - Packages to write automated tests
    - To install ```npm install mocha chai --save-dev``` saves as dev dependecies
    - replace ```test``` with 'mocha' in JSON
    - to run ```npm run test```

-  Mocha
    - Testing framework. Looks in ```test``` folder for files to run
    - ```module.exports``` and ```require```
    - Use ```.gitignore``` to ignore sensitive files
    - In JS file add
    - In test file use require
```js      
      const assert = require('chai').assert;
      const app = require('../app');
```
    
  - describe/it statement in test file
      describe('App', function() {
        it('app should return hello', function () {
          assert.equal(app(), 'hello');
        });
      });
    

  - Chai
    - Assertion library
    - describe desired output of code
    - ```should``` ```it``` and ```assert```
    - 



  - BDD: Behavior Driven Development 
    - Write test to check behaviour of code
   - Mocha Instructions
      - Initialize a project as a num package
      - ```npm init -y``` 
      - not in test folder
       - Add test framework eg. 'mocha' to scripts
       - update scripts
       


* # Asynchronus Control Flow
  - ## Callbacks
    - Functions passed as arguments to be executed once an operation completes
    - Code modularity

const forEach = (array, action) => {
  for (const element of array) {
    action(element)
  }
}

const logThatElement = (element) => console.log(element);

const logThatElementButFancy = (element) => console.log("🔥🔥" + element)

const someArray = [1, 2, 3, 4, 5]

forEach(someArray, logThatElement)




```js    
function fetchData(callback) {
    setTimeout(() => {
        callback("Data received");
    }, 1000);
}

fetchData((data) => {
    console.log(data);
});

```



- # Promises


   - Objects that represent the eventual completion (or failure) of an asynchronus operation
   - Common use is when we want to run network requests to fetch data from APIs
    - Use ```.then .catch .finally```


```js
const boilWater = () => {
  return new Promise((resolve, reject) => {
    if (Math.random() > 0.5) {
      return resolve();
    }
    return reject("Oven Broke");
  });
};

// boilWater()
//   .then(() => console.log("water is boiling!"))
//   .catch(() => console.log("The oven broke"));

const putThePastaInWater = () => {
  return new Promise ((resolve, reject) => {
    if (Math.random() > 0.5) {
      return resolve();
    }
    return reject("Pasta fell on floor");
  });
};

boilWater()
  .then(() => putThePastaInWater())
  .then(() => console.log("Pasta boiling was success"))
  .catch((error) => console.log(error));
```


```js
const fetchData = () => {
    return new Promise((resolve) => {
        setTimeout(() => {
            resolve("Data received");
        }, 1000);
    });
};

fetchData().then((data) => {
    console.log(data);
});
```
  - Async/ Await
    - Syntax that allows you to write asynchronus code that looks synchronus, easier to read and maintain
```js
const fetchData = () => {
    return new Promise((resolve) => {
        setTimeout(() => {
            resolve("Data received");
        }, 1000);
    });
};

const getData = async () => {
    const data = await fetchData();
    console.log(data);
};

getData();
```
  - ## Error Handling
   -  handling errors in asynchronus code done with ```.catch()``` for promises or try/catch blocks with async/await
```js
const fetchData = () => {
    return new Promise((_, reject) => {
        setTimeout(() => {
            reject("Error fetching data");
        }, 1000);
    });
};

const getData = async () => {
    try {
        const data = await fetchData();
        console.log(data);
    } catch (error) {
        console.error(error);
    }
};

getData()
```


## Async control flow libraries
- Libraries like ```async.js``` can provide additional control flow patterns like series, parallel, and waterfall for managing complex asynchronus workflows

## Transposition:
  - Rearrange arrays
  - Eg: transform rows into columns in a matrix
  - 2D array (matrix) transposition would be converting rows to columns
    - Rows become columns. Columns become rows
  - Example: Transpose 2D matrix
    - Initalize empty array
    - Loop over each column
    - Loop over each row
    - Transpose: 
      - Initalize empty array for each column in original matrix
      - Fill array with elements from original matrix 

## Networking and TCP
- Two or more computers communicate with each other
- Transmission Control Protocol
- MAC address: name
  - 48 bits, 6 bytes long
- IP address: telephone number

## HTTP
- URL: Uniform Resource Locator
  - URL has: 
  - Protocol
  - Domain (or Host)
  - Port
  - Resource Path
  - Query Parameters
  - Anchor
- 9 HTTP request methods, but we only need to consider 4
  - ```get```: used to get data from the server
  - ```post```: used to create new data
  - ```put```: used for editing existing data on the server
  - ```delete```: used to delete existing data
- Status Codes:
  - 200: Everything went great
  - 201: Request succeeded and new resource has been created as result
  - 404: Resource not found
  - 500: The server had an error
  - 451: Resource not available due to legal reasons
- HTTP is request-response protocol where client makes requests and server sends responses
- HTTP is a text based protocol
- HTTP requests must contain verb/method(```get```) and the Path ```/about```
- HTTP requests arent always to recieve data but sometimes to save data, done via a ```post``` instead of a ```get```
- requests and responses both contrain key-value based headers
- URL: Server uses path to determine which resource to access. Parameters add additional information about what the client is interested in
- UDP: User Datagram Protocol
  - Smaller header size (8 bytes) which results in smaller packet sizes
  - Connectionless ie. there is no need to establish or maintain a connection
  - No error recovery (any corrupted packets are discarded)
  - Packets can arrive in any order
  - Useful for streaming/low latency applications
  - Example: Twitch
- TCP: Transmission Control Protocol
  - Larger header size (20 bytes)
  - Requires a connection (3-way handshake)
  - Corrupted packets are reported to the server and are re-sent
  - Packets arrive in order
  - Useful when guaranteed communication is needed
  - reliable, safe. will resend if packages are missing
- HTTP:
- Needle:
















* Object Manipulation
* SQL
* Algorithms
* APIs
* Refactoring
* test topics