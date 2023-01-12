# Javascript_Questions

## Table of Contents


* [Basic Questions](#basic-questions)


1. How to write Hello World in JavaScript?
  [example code here](https://www.programiz.com/javascript/examples/hello-world#:~:text=The%20second%20line-,console.,prints%20the%20'Hello%2C%20World!')
2. What is a variable?

    [example code here](https://codepen.io/juneJune_95/pen/yWyWJZ)

    [example code here2](https://www.tutorialsteacher.com/javascript/javascript-variable)
    

3. JavaScript Program To Work With Constants [refrence here](https://www.programiz.com/javascript/examples/constants), [example code here](https://codepen.io/juneJune_95/pen/vYjpYrQ?editors=1111)

   The "const" keyword in JavaScript is used to create a constant variable, which means the variable cannot be reassigned a new value.
   
   ##Example: Work With Constants
   ```
     const a = 5;
      a = 44; // throws an error
   ```
    - Constants are block-scoped. Hence the variable defined inside a block represents a different value than the one outside. For example,
      ```
          {
              const a = 50;
              console.log(a); // 50
          }
          console.log(a); // 5
      ```
     - The arr array value is changed and a new element is added. In array, the values can be changed. However, the array reference cannot be changed. For example,
     
         ```
          const arr = ['work', 'exercise', 'eat'];
           arr[3] = 'hello';
         ```
      - Also, the constant should be initialized. You cannot just declare a constant. For example,
          ```
              const x;
              // SyntaxError: const declared variable 'x' must have an initializer.
          ```
