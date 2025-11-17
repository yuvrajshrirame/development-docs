# JavaScript

## Execution context in JS

![image.png](image.png)

- Execution context is an environment/container in which JS code is executed.
- The container is consist of two phases: memory creation phase and code execution phase which are also called as —
    - memory → variable environment
    - code → thread of execution
- Memory consists of data in key-value pairs whereas code is consists of lines that are executed at the time of execution

> JS is a synchronous and single threaded language
> 
- Single threaded → can execute a single thread at a time
- Synchronous → can only execute one command at a time and in a certain order

> Everything in JS happens inside an execution context
> 

## How JS code is executed?

![image.png](image%201.png)

> In phase 1 (i.e. memory creation phase) :
> 

![image.png](image%202.png)

> In phase 2 (i.e. execution phase) :
> 

Note: For functions, separate execution context is created. 

![image.png](image%203.png)

After return statement, the execution will return to its last position/line of code.

The value for square2 function will be set to 4 and the whole execution context for function will be deleted.

In line number 7, function is being invoked with new value, so new execution context will be created once again.

## Call Stack

Call stack maintains the order of execution of execution contexts.

Call stack is also known as —

- Execution context stack
- Program stack
- Control stack
- Runtime stack
- Machine stack

![image.png](image%204.png)

## Hoisting in JS

Detailed Video : [https://youtu.be/Fnlnw8uY6jo](https://youtu.be/Fnlnw8uY6jo)

**Hoisting** is a JavaScript behavior where variable, function, and class **declarations** are “moved” to the top of their scope (such as a function or global space) before the code actually runs. This allows you, in some cases, to reference variables or functions even before they’re explicitly declared in code below.

### Variable Hoisting

- **With `var`**: The declaration is hoisted, but the initialization is not. If you use a **`var`** variable before its line of declaration, its value will be **`undefined`** until the code reaches the initialization.

### Function Hoisting

- **Function declarations** (**`function foo() {}`**) are fully hoisted, including the function body. This means you can call the function before it’s declared in your code.

## Functions in JS (❤️ of JS)

### Standard Functions

```jsx
function add(a, b) {
  return a + b;
}
```

### Arrow Functions

```jsx
const add = (a, b) => {a + b}
```

## Shortest JS Program

- Shortest JS program is an empty program. Even if nothing is there, it still performs multiple operations behind the scenes.
- When a JS program is run, a global execution context is created, a global object (window object) is created and a this object is created (this object points to window object)
- At global level, this equals to window object
    
    ```jsx
    // at global level only
    window === this
    true
    ```
    
- Anything not inside function is in global scope
- Whenever we add variables or functions in global scope, they are directly added to window object, whereas the variable inside functions are not added.
    - Very IMP ⬇️
        
        ```jsx
        let x = 10; // x is added to window object
        function abc(){ // abc is added to window object
        	let y = 20; // y is not added to window object
        }
        console.log(window.a); // prints 10
        console.log(a); // prints 10
        console.log(this.a); // prints 10 (coz at global level, this = window)
        // IMP: anything which does not mention window as prefix is assumed as a global scope.
        ```