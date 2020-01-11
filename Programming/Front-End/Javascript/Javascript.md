JavaScript


# Table of Contents

1. [String Interpolation](#string-interpolation)
2. [Template Literals](#template-literals)
3. [Conditional Statements](#conditional-statements)
4. [Function Declarations](#function-declarations)
5. [Scope](#scope)
6. [Arrays](#arrays)
7. [Loops](#loops)

---



## <u>String Interpolation</u> 

```javascript
const myPet = 'armadillo';
console.log(`I own a pet ${myPet}.`);
// Output: I own a pet armadillo.
```

---



## <u>Template Literals</u>

```javascript
// STRING CONCATENATION
console.log('Hi, I\'m ' + p.name + '! Call me "' + p.nn + '".');
```

```javascript
// TEMPLATE LITERALS
console.log(`Hi, I'm ${p.name}! Call me "${p.nn}".`);
```

---



## <u>Conditional Statements</u>



#### 	If keyword

```javascript
let sale = false;
if (sale) {
  console.log("Time to buy!");
}
// Prints "Time to buy!"
```



#### 	If...Else Statements

```javascript
if (false) {
  console.log('The code in this block will not run.');
} else {
  console.log('But the code in this block will!');
}
// Prints "But the code in this block will!" 
```



#### 	Comparison Operators

```javascript
let hungerLevel = 10;
if (hungerLevel > 7) {
  console.log('Time to eat!');
} else {
  console.log('We can eat later!');
}
```



#### Logical Operators

- **&& (and operator) **

  When using the && operator, both conditions must evaluate to true for the entire condition to evaluate to true and execute. Otherwise, if either condition is false, the && condition will evaluate to false and the else block will execute. 

```javascript
if (stopLight === 'green' && pedestrians === 0) {
  console.log('Go!');
} else {
  console.log('Stop');
}
```




- **- || (or) operator**

   When using the || operator, only one of the conditions must evaluate to true for the overall statement to evaluate to true. In the code example above, if either day === 'Saturday' or day === 'Sunday' evaluates to true the if‘s condition will evaluate to true and its code block will execute. If the first condition in an || statement evaluates to true, the second condition won’t even be checked. Only if day === 'Saturday' evaluates to false will day === 'Sunday' be evaluated. The code in the else statement above will execute only if both comparisons evaluate to false.    

```javascript
    if (day === 'Saturday' || day === 'Sunday') {
  console.log('Enjoy the weekend!');
} else {
  console.log('Do some work.');
}
```




   - **! (not) operator**

     Essentially, the ! operator will either take a true value and pass back false, or it will take a false value and pass back true.

```javascript
let excited = true;
console.log(!excited); // Prints false

let sleepy = false;
console.log(!sleepy); // Prints true
```



- **Ternary Operator **

  ​	We can use a *ternary operator* to simplify an `if...else` statement. 

```javascript
let isNightTime = true;

if (isNightTime) {
  console.log('Turn on the lights!');
} else {
  console.log('Turn off the lights!');
}
```

- We can use a *ternary operator* to perform the same functionality:  

```javascript
isNightTime ? console.log('Turn on the lights!') : console.log('Turn off the lights!');
```



- **Else If Statements**

  ​	We can add more conditions to our `if...else` with an `else if` statement. The `else if` statement allows for more than two possible outcomes. You can add as many `else if` statements as you’d like, to make more complex conditionals! 

  ```javascript
  let stopLight = 'yellow';
  
  if (stopLight === 'red') {
    console.log('Stop!');
  } else if (stopLight === 'yellow') {
    console.log('Slow down.');
  } else if (stopLight === 'green') {
    console.log('Go!');
  } else {
    console.log('Caution, unknown!');
  }
  ```



- **The switch keyword**

  ​	 `else if` statements are a great tool if we need to check multiple conditions. In programming,  we often find ourselves needing to check multiple values and handling  each of them differently. 

  ```javascript
  let groceryItem = 'papaya';
  
  switch (groceryItem) {
    case 'tomato':
      console.log('Tomatoes are $0.49');
      break;
    case 'lime':
      console.log('Limes are $1.49');
      break;
    case 'papaya':
      console.log('Papayas are $1.29');
      break;
    default:
      console.log('Invalid item');
      break;
  }
  
  // Prints 'Papayas are $1.29'
  ```



#### Summary

- An `if` statement checks a condition and will execute a task if that condition evaluates to `true`.

- `if...else` statements make binary decisions and execute different code blocks based on a provided condition.

- We can add more conditions using `else if` statements.

- Comparison operators, including `<`, `>`, `<=`, `>=`, `===`, and `!==` can compare two values.

- The logical and operator, `&&`, or “and”, checks if both provided expressions are truthy.

- The logical operator `||`, or “or”, checks if either provided expression is truthy.

- The bang operator, `!`, switches the truthiness and falseness of a value.

- The ternary operator is shorthand to simplify concise `if...else` statements. 

- A `switch` statement can be used to simplify the process of writing multiple `else if` statements. The `break` keyword stops the remaining `case`s from being checked and executed in a `switch` statement.

  ---

  

## <u>Function Declarations</u>

​	A *function* is a reusable block of code that groups together a sequence of statements to perform a specific task. 

```javascript
function sayThanks(name) {
  console.log('Thank you for your purchase '+ name + '! We appreciate your business.');
}
sayThanks('Cole'); // op Thank you .... Cole ...
```



- **Default Parameters**

```javascript
function greeting (name = 'stranger') {
  console.log(`Hello, ${name}!`)
}

greeting('Nick') // Output: Hello, Nick!
greeting() // Output: Hello, stranger!
```



- **Arrow Functions**

```javascript
const rectangleArea = (width, height) => {
  let area = width * height;
  return area;
};
```

---



## <u>Scope</u>

​	Scope defines where variables can be accessed or referenced. While some  variables can be accessed from anywhere within a program, other  variables may only be available in a specific context. 



**Block** - A block is the code found inside a set of curly braces `{}`.



#### Global Scope

​	In *global scope*, variables are declared outside of blocks. These variables are called *global variables*.

```javascript
const color = 'blue'

const returnSkyColor = () => {
  return color; // blue 
};

console.log(returnSkyColor()); // blue
```



#### Block Scope

​	When a variable is defined inside a block, it is only accessible to the code within the curly braces `{}`.

```javascript
const logSkyColor = () => {
  let color = 'blue'; 
  console.log(color); // blue 
};

logSkyColor(); // blue 
console.log(color); // ReferenceError
```



**Scope Pollution** - *Scope pollution* is when we have too many  global variables that exist in the global namespace, or when we reuse  variables across different scopes.

```javascript
let num = 50;

const logNum = () => {
  num = 100; // Take note of this line of code
  console.log(num);
};

logNum(); // Prints 100
console.log(num); // Prints 100
```

---



## <u>Arrays</u>

​	Arrays are JavaScript’s way of making lists. Arrays can store any data types (including strings, numbers, and booleans).

**Summary** -

- Arrays are lists that store data in JavaScript. 

- Arrays are created with brackets `[]`.

- Each item inside of an array is at a numbered position, or index, starting at `0`. 

- We can access one item in an array using its index, with syntax like: `myArray[0]`.

- We can also change an item in an array using its index, with syntax like `myArray[0] = 'new string'`; 

- Arrays have a `length` property, which allows you to see how many items are in an array.

- Arrays have their own methods, including `.push()` and `.pop()`, which add and remove items from an array, respectively.

- Arrays have many methods that perform different tasks, such as `.slice()` and `.shift()`, you can find documentation at the [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) website. 

- Some built-in methods are  mutating, meaning the method will change the array, while others are not mutating. You can always check the documentation.  

- Variables that contain arrays can be declared with `let` or `const`. Even when declared with `const`, arrays are still mutable. However, a variable declared with `const` cannot be reassigned. 

- Arrays mutated inside of a function will keep that change even outside the function. 

- Arrays can be nested inside other arrays. 

- To access elements in nested arrays chain indices using bracket notation. 

  

```javascript
const flowers = ['peony', 'daffodil', 'marigold'];

function addFlower(arr) {
  arr.push('lily');
}

addFlower(flowers);

console.log(flowers); // Output: ['peony', 'daffodil', 'marigold', 'lily']
```

---



## <u>Loops</u>

​	A *loop* is a programming tool that repeats a set of instructions until a specified condition, called a *stopping condition* is reached.



#### The For Loop

​	A `for` loop contains three expressions separated by `;` inside the parentheses: 

```javascript
for (let counter = 0; counter < 4; counter++) {
  console.log(counter);
}
```



**Looping through Arrays**	

```javascript
const animals = ['Grizzly Bear', 'Sloth', 'Sea Lion'];
for (let i = 0; i < animals.length; i++){
  console.log(animals[i]);
} /*
Grizzly Bear
Sloth
Sea Lion */
```



#### Nested Loops

When we have a loop running inside another loop, we call that a *nested loop*.

```javascript
const myArray = [6, 19, 20];
const yourArray = [19, 81, 2];
for (let i = 0; i < myArray.length; i++) {
  for (let j = 0; j < yourArray.length; j++) {
    if (myArray[i] === yourArray[j]) {
      console.log('Both loops have the number: ' + yourArray[j])
    }
  }
};
```