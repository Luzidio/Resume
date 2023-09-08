Page 1
# Javascript Concepts
## You Should Know

_____________________
Page 2
Hey Devs
Javascript is everywhere. Millions of webpages are built on JS.

Let's discuss some of the **basic concept** of Javascript which are **important to learn** for any **Javascript developer**.

Page 3
## Scope
Scope determines the accessibility of variables, objects and functions.
 - In JavaScript, a variable has **3 types of scape**:
  a. Block Scope
  b. Function Scope
  c. Global Scope

Page 4
## Hoisting
**Hoisting in Javascript** is a behavior in which a function or variable can be **user before declaretion**.
 - In terms of variables and constant keywords var is hoisted, and **let and const does not allow hoisting**.
  
   (ex1)[

    // Exemplo com var
console.log(x); //saida: indefinida
var x = 5;

// Exemplo com Let
console.log(y); //lança um erro
let y =10;

// Exemplo com const
console.log(z); //Trows an error
const z =15;

  ]

Page 5
## Closures
Closure means that an **inner function always has acess** to the variable of **its outer function**, even after outer function has returned.
(ex2)[

  function outerFunction(){
  var outerVariable = "I'm from the outer function";
  function innerFunction(){
    console.log(outerVariable);
  }
  return innerFunction;
}

var myClosure= outerFunction();
// Even though outerFunction has finished executing,
// innerFunction still has acess to outerVariable
myClosure(); //Output: "I'm from the outer function"

]

Page 6
## Callbacks
A callback function can be defined as a **function passed into another funcion** as parameter.
(ex3)[

  function greet(name, callback) {
  console.log("Hi" , name)
  callback()
}
//Callback function
function callMe(){
  console.log("I'm callback function")
}
//passive function as an argument

// output
// Hi Room
// I'm callback function

]

Page 7
## Promises
Promises is a good way to **handle asynchronous operations**.
- It's used to **find out** if the asynchronous operation is successfully **completed or not**.
- A promise may have one of **three states**:
  a. Pending
  b. Fulfilled
  c. Rejected

  Page 8
  ## Async & Await
  **Stop** and **wait** until **something is resolved**.
  - We use the **async keyword** with a function to represent that the function is an **asynchronous function**.
  - The async function returner a promise
  (ex4)[

    const showPost = async() => {
    const res = await fetch("http://xyz.com/roomPost")
    return res.posts;
    }
    console.log(showPost());

  ]

  Page 9
  Follow Page