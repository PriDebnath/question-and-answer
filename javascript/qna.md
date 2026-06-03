# 70 JavaScript interview Questions and Answers
## Questions: 
1. What is JavaScript ? What is javaScript engine ?
2. What is client side and server side ?
3. What is scope in javaScript ?
4. What is the implicit type of a variable when defined without var, let or const ?
5. What is hoisting in javaScript ?
6. What is JSON ?
7. What is variable ? What is the difference between var, let and const ?
8. What is the difference between primitive and non-primitive data types ?
9. What is the difference between "null" and "undefined" ?
10. What is the use of "typeof" oporator ?
11. What is type coercion ?
12. Oporator is javaScript 
13. What is the difference between "==" and "===" ?
14. Explain Spread and Rest oporator 
15. What the use of indexOf method in an array ? 
16. What the difference between the find,  filter and slice method in an array ?
17. What the difference between the push and concat method in an array ? 
18. What the difference between the pop and shift method in an array ? 
19. What is the use of splice() method in an array ?
20. What is the difference between forEach() and map() method in array ?
21. What is array destructuring ?
22. What is array-like object in javaScript ?
23. How can we convert array-like objects to an array ?
24. What is the difference between for and while loop ?
25. What is the difference between break and continue statement ?
26. What is function expression ? 
27. Explain callback function and higher order function 
28. What is the difference between parameter and argument in function ?
29. What is first class function ?
30. Currying involves transforming a function into a series of functions, each handling one argument at a time 
31. What is "call", "apply" and "bind" in js ?
32. What is error handling ?
33. Types of error in javaScript ?
34. What the difference between deep and shallow copy in object ?
35. What is event delegation ?
36. What is event bubbling ? 
37. Explain Event loop:
38. Explain Closure
39. Explain array.reduce() 
40. What is block in JavaScript ?
41. What is a prototype in JavaScript?
42. How does the prototype chain work in JavaScript? 
43. Explain the difference between __proto__ and prototype. 
44. How do you add a method to an object's prototype? Provide a code example.
45. What is “this” keyword in JavaScript ?
46. What is arrow function ?
47. What is difference between synchronous and asynchronous ?
48. What is Promise in JavaScript ?
49. What is async and await ?
50. What is localStorage and sessionStorage ?
51. What is DOM in JavaScript ?
52. How to select elements in DOM ?
53. How to create and remove elements in DOM ?
54. What is event listener ?
55. What is debounce ?
56. What is throttle ?
57. What is execution context ?
58. What is call stack ?
59. What is strict mode ?
60. What is template literal ?
61. What is default parameter ?
62. What is optional chaining ?
63. What is nullish coalescing ?
64. What are JavaScript modules ?
65. What is fetch API ?
66. What is difference between cookies and localStorage ?
67. What is garbage collection ?.
68. What is immutability ?
69. What is Object.freeze() ?
70. What is Object.keys(), values(), entries() ?
71. 
---------------------------------------------------

## Questions and answers: 

1. What is JavaScript ? What is javaScript engine ?
JavaScript is a programming language used for converting static web pages to interactive and dynamic one.
JavaScript engine is a program present in we browser to run javaScript code .


3. What is client side and server side ?
client side is a device, application or software component that requests and consumes services or resources from a server.
Server side is a device, application or software component that provides services or resources to clients  .


4. What is scope in javaScript ?
Scopes determines where a variable or  function can be accessed in the code.
We have global scope, function scope and block scope .
   

5. What is the implicit type of a variable when defined without var, let or const ?
"var" is the implicit type that get added to those variables and they are accessible in global and block scope .


6. What is hoisting in javaScript ?
In javaScript, functions and variables declaration are moved to the top of their respective scopes during memory creation phase.
This is called hoisting . var, let and const are hoisted  . In case of function it hoists the whole function. 


8. What is JSON ?
JSON is a light weight data interchange format. It consists of key-value pairs.


9. What is variable ? What is the difference between var, let and const ?
Variables are used to store data.
Difference between them are - 
var: Function-scoped, and can be redeclared and reassigned.

let: Block-scoped, and can be reassigned but not redeclared.

const: Block-scoped, and immutable (cannot be reassigned), although properties of objects and elements of arrays can be modified.


8. What is the difference between primitive and non-primitive data types ?
Primitive data types can store single value. They are immutable meaning once their value is assigned it can not be changed . If we update a primitive variable's value it will take new space in memory and the new value will get assign to it . They are number, string, undefined, null etc .
Non-primitive data-types are totally opposite of primitive, they are complex, mutable and their value can be changed maintaining same memory location .
Example:
```
let num =  2
let nums = [1,2]
console.log(num) // 2 
console.log(nums) // [1, 2, 3]
// Changing values
nums.push(3)
num = 7
```


9. What is the difference between "null" and "undefined" ?
A variable automatically gets "undefined" if we do not assign any value to it on the other hand we can initialise a variable with a value of "null" meaning the variable has a nothing as value . "undefined" can be used in case where we know we will get the correct value for the variable soon . "null" can be used where we  know we are not going to get a value for the variable any soon .


10. What is the use of "typeof" oporator ?
  To determine the type a variable we use "typeof" oporator . It can be used to know the datatype of something coming from external sources .   

11. What is type coercion ?
  Type coercion is an automatic way of changing datatypes of a variable depending on circumstances or condition . For example if we try to use addition oporator ( + ) on a string and a number variable, javaScript will treat the number as a string datatype then it will add that as string ( 5 + "5" = "55" ) or ( 5 === 5 = true )


12. Oporator in javaScript 
  There are three oporators  based on number of operand it has. 
Unary oporator "="  ( let a = 2) , binary oporator "+" ( let c = a + b ) and ternary operator ( let result = condition ? "yes" : "no" )


13. What is the difference between "==" and "===" ?
"==" called loose equality check . For example ( 1 == "1"  is true ) and ( 1 == true is true ) in loose equality check javaScript do type coercion  behind the scene before the comparison .   
"===" called strict equality check  For example ( 1 === "1"  is false ) and ( 1 === true is false ) in strictly equality check javaScript don't do type coercion  so value and data type need to be matched to get the correct output .



14. Explain Spread and Rest oporator 
  Spread oporator is used to spread an iterable like array, string or object into an individual element . 
Spread an array ( console.log(...[1, 2, 3]) //output: 1 2 3) merging array with spread oporator ( [ ...arr, ...arr2] )
  Rest operator can be used to collect all remaining items from a iterable or object.
 Example:
```
 function func( a, b , ...restParams){
    console.log( restParams )
   // Output: [3, 4]
 }
func( 1, 2, 3, 4)
```

15. What the use of indexOf method in an array ? 
We use to get the index of a specific element in an can .
Example
```
let arr = [ 1, 2 ]
console.log( arr.indexOf(1) )
// Output: 0
```

16. What the difference between the find,  filter and slice method in an array ?
   Array.find() method get the first element in an array which fulfilling the condition whereas Array.filter() method returns all elements which fulfilling the condition .
Array.slice() method get a subset of an array by taking start and end index .


17. What the difference between the push and concat method in an array ? 
 Both are used to add new item to an existing array .
 Array.push(item) method adds the new items to the actual array whereas Array.concat([item1, item2]) creates a new array and attach those new items to the newly created array .


18. What the difference between the pop and shift method in an array ? 
 Both are used to remove item from an existing array .
Array.shift() remove item from the beginning of an array and Array.pop() remove item from last .


19. What is the use of splice() method in an array ?
Array.splice() method can be used to add, remove or replace to an array . 
 arr = arr.splice(startIndex, deleteCount, ...itemsToAdd)
```
let arr = [ "a", "b", "c"]
arr.splice(1,9, "x", "y")
// Output: ["a", "x", "y", "b", "c" ]
```

20. What is the difference between forEach() and map() method in array ?
  Both are used to iterate over an array but after iterating over an array map() method returns a new array with the changes whereas forEach() method doesn't.


21. What is array destructuring ?
  Using destructuring we can access an individual element of an array . 
let [ firstFruit, secondFruit ] = [ "orange", "apple" ] 
firstFruit // output: "orange"


22. What is array-like object in javaScript ?
  Array-like objects are objects that have indexed elements and a length property but may not have all methods of an array. Like strings, arguments in function , html elements 
string example
```
let s = "pri"
s.length // output: 3
argument in function
function func( ){
  arguments[0] // output : a
}
func("a", "b")
```

24. How can we convert array-like objects to an array ?
```
let arrayLikeObj = { 0: "a", 1: "b", 2: "c" }
let usingArrayFrom = Array.from(arrayLikeObj)
let usingSpread = [ ...arrayLikeObj ]
```

26. What is the difference between for and while loop ?
Both are used to iterate over something .
for loop allow us to iterate over something for a specific number of time whereas while loop runs until a condition is met .


27. What is the difference between break and continue statement ?
We can stop executing any loop with break statement .
 Continue statement can be used where we want to skip the current iteration in the loop and move on to next iteration .


28. What is function expression ? 
  When we assign a function to a variable and use the variable name to invoke that,  it  calls function expression .


29. Explain callback function and higher order function 
  When a function get passed to a function as an argument it called callback function on the other hand the function that is receiving the callback function called higher order function 


30. What is the difference between parameter and argument in function ?
  Parameters are placeholders defined in function decoration . Here :  "a" and "b"
function sum(a,b){}
  Arguments are actually value passed into the function while invoking it . Here "1" and "2"
sum(1, 2)


31. What is first class function ?
  When we have the ability to use a function as a variable in a programming language it is said to have first class function . First class means having the ability to assign it to a variable , passed as argument or return from a function .


32. What is Function Currying ?
 Currying involves transforming a function into a series of functions, each handling one argument at a time 
Example :
```
  function curryAdd(a) {
    return (b) => {
      return a + b
    }
  }
  
  let added2 = curryAdd(2)
  let add2more = added2(2)
  let add3more = added2(3)
  console.log(add2more)
  console.log(add3more)
```

31. What is "call", "apply" and "bind" in js ?
In JavaScript, call, apply, and bind are methods used to set the context of "this" keyword for a function and control its invocation.
```
 let person1 = { name: "Pritam" }
 let greetPerson = function(greetText){
   console.log(greetText + ' ' + this.name)
 }
 greetPerson.call(person1,"Hi") // call
 greetPerson.apply(person1, ["Hi"]) // apply
 let greetPerson1 = greetPerson.bind(person1, "Hi") // bind
 greetPerson1()
```

32. What is error handling ?
Normally if javaScript finds any error it stop executing further codes .
But  we can define a try-catch block and put the code in try block which can cause error .
In this way javaScript try executing the code 
and goes to catch block if it finds an error .
Then execute further codes 


34. Types of error in javaScript ?
  1. Syntex error: when we miss to write correct syntex .
  2. Reference error: when it fail to find an variable in current scope .
  3. Type error: it can be shown when we use a method on different type .
  4. Renge error: when we try to access a specific indexed element which is not present .


34. What the difference between deep and shallow copy in object ?
  We can make a swallow copy of an object using spread oporator
```
let obj = { name: "Pritam" }
let swallowObj = { ...obj }

let obj3 = { j: { k: 6 } }
    let obj4 = { ...obj3 }
    obj3.j.k = 7
    obj4.j.k = 8
    console.log(obj3) // 8 : changing copied object will also make changes in parent object
```

  We can make a deep copy with JSON.parse() and JSON.stringify() 
```
let obj2 = { name: "Pritam" }
let deepObj = JSON.parse(JSON.stringify(obj2))
```

35. What is event delegation ?
Rather than adding event listener on each element we attach just one event listener to those element's  parent and respond to the event on parent and its childs . 


36. What is event bubbling ? 
If you have two elements a parent and its child and they have their own click event listener . In this case, clicking the child will trigger the event that was set to it and then its parent's click event will also run . This way event will go from child element to parent element ( upward to DOM tree ) this default behaviour is called event bubbling .

We can do the opposite ( going downward to DOM tree ) by passing third argument to true of event listener . 
It is called capturing . 
```
let clickParent = function(event) {
    console.log('Parent div clicked');
   //event.stopPropagation()
  }

  let clickChild = function() {
    console.log('child div clicked');
  // event.stopPropagation()
  }
  
  parent.addEventListener('click', clickParent,true);
  child.addEventListener('click', clickChild,true);
```

37. Explain Event loop:
An Event Loop in JavaScript is a core mechanism that allows JavaScript to perform asynchronous tasks without blocking the main thread. When javaScript finishes running all synchronous tasks and the call stack is empty . Event loop places tasks from callback queue to call stack for execution . This loop continues until the  callback queue is empty .

38. Explain Closure
Function, along with their lexical environment, forms a closure. And when a function is returned the whole closure is returned, this allows functions to retain access to variables from their outer lexical environment even after that scope has finished executing.


39. Explain array.reduce() 
The reduce() method runs a callback function on each array element to produce (reduce it to) a single value.The reduce() method works from left-to-right. The reduce() method does not change the original array.


40. What is block in JavaScript ?
We use block to combine multiple statement to a single statement . It can be created with curly braces .


41. What is a prototype in JavaScript?
A prototype is an object from which other objects inherit properties and methods. Every JavaScript object has a prototype, and the prototype object itself may have its own prototype, forming a chain called the prototype chain.


42. How does the prototype chain work in JavaScript? 
The prototype chain is used for property and method lookup. When you access a property or method on an object, JavaScript first looks at the object itself. If it doesn't find it there, it looks at the object's prototype, then the prototype's prototype, and so on, until it either finds the property/method or reaches the end of the chain (null).


43. Explain the difference between __proto__ and prototype. 
__proto__ is a property of an object that points to the prototype that the object was created from. prototype is a property of a constructor function that is used to set the __proto__ of new instances created by that constructor.


44. How do you add a method to an object's prototype? Provide a code example.
```
function Person(name) {
  this.name = name;
}

Person.prototype.sayHello = function() {
  console.log(`Hello, my name is ${this.name}`);
};

const alice = new Person('Alice');
alice.sayHello(); // 'Hello, my name is Alice'
```


45. What is “this” keyword in JavaScript ?
this refers to the object that is currently executing the function.
- In global → window (browser)
- In object → that object
- In arrow function → inherits from parent


46. What is arrow function ?
Arrow function is a shorter way to write functions.
- No function keyword
- No own this

Example:
```
const add = (a, b) => a + b;
```


47. What is difference between synchronous and asynchronous ?
- Synchronous → runs line by line (blocking)
- Asynchronous → runs in background (non-blocking)

Example:
```
setTimeout(() => console.log("Hi"), 1000);
```

48. What is Promise in JavaScript ?
Promise is used to handle async operations.
It has 3 states:
- Pending
- Resolved
- Rejected

Example:
```
fetch(url).then().catch();
```

49. What is async and await ?
Used to handle promises in cleaner way.

async makes function return promise
await waits for result

Example:
```
async function getData() {
  let res = await fetch(url);
}
```


50. What is localStorage and sessionStorage ?
Both store data in browser.
- localStorage → permanent (until manually cleared)
- sessionStorage → cleared when tab closes

Example:
```
localStorage.setItem("name", "Pritam");
```
51. What is DOM in JavaScript ?

DOM (Document Object Model) represents HTML as a tree structure so JavaScript can access and modify elements.

52. How to select elements in DOM ?
```
getElementById()
querySelector()
querySelectorAll()
```
53. How to create and remove elements in DOM ?
```
let div = document.createElement("div");
document.body.appendChild(div);
div.remove();
```
54. What is event listener ?
It listens for events like click, scroll, etc.
```
btn.addEventListener("click", fn);
```
55. What is debounce ?
Debounce delays function execution until user stops action.
Used in search input.

56. What is throttle ?
Throttle limits function execution to once in a time interval.
Used in scroll events.

57. What is execution context ?
Environment where JS code runs.
Global
Function

58. What is call stack ?
Stack that keeps track of function execution (LIFO).

59. What is strict mode ?
"use strict";
Prevents bad practices and errors.

60. What is template literal ?
String using backticks ` `
```
let name = `Hi ${user}`;
```
61. What is default parameter ?
```
function add(a = 0, b = 0) {}
```
62. What is optional chaining ?
Safely access nested object
```
user?.address?.city
```
63. What is nullish coalescing ?
Returns right value if left is null or undefined
```
let x = a ?? "default";
```

64. What are JavaScript modules ?
Used to split code into files
export
import

65. What is fetch API ?
Used to make HTTP requests
```
fetch(url).then(res => res.json());
```

67. What is difference between cookies and localStorage ?
Cookies → small, sent to server 
localStorage → large, only browser 

68. What is garbage collection ?
Automatic memory cleanup by JavaScript engine.

69. What is immutability ?
Data cannot be changed directly.
We create new copy instead.

70. What is Object.freeze() ?
Prevents object modification.
Object.freeze(obj);

71. What is Object.keys(), values(), entries() ?
keys() → returns keys
values() → returns values
entries() → returns key-value pairs

