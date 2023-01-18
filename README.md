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
          
3. Awesome JavaScript array methods [refrence here](https://jilles.me/awesome-javascript-array-methods/)
   -  #1 array.forEach(fn, index)
        - arr.forEach() takes a function as first argument and current index as second. It also creates a new scope whereas a for-loop doesn't.
        - a for loop you create 2 variables that are accessible outside of the for loop.

        ```
            users.forEach(function (user, i) {
                var fullName = user.firstName + ' ' + user.lastName;
                console.log('Hello ' + fullName);
            });
        ```
    - #2 array.map(fn)
    
       - It loops over the array (like forEach) but will create a new array with the items you return.
       
       ```
           var usersDb = users.map(function (user, index) {
              user.id = index + 1;
              return user;
          });
          console.table(usersDb);
       ```
    - #3 array.filter(fn)
      - Array.filter is like a bit like map. It also creates a new array but only containing the items where the function returns true.
      
        ```
          var guys = users.filter(function (user) {
              return user.gender === 'M';
          });
          console.table(guys);
        ```
     - #4 array.reduce(fn, startingValue)
       - The first argument is a function that takes 4 arguments, the last two are optional.
       - previousValue - the previous value in the next iteration, will be startingValue the first time.
       - currentValue - the current item in the array we're iterating over.
       - index - the index of the current item.
       - originalArray - the array we're executing .reduce on.
       
       ```
          var namesList = users.reduce(function (previous, current, index, originalArray) {
            var end = index + 1 === originalArray.length ? '.' : ', ';
            return previous + current.firstName + end;
        }, '');
          console.log(namesList); // Jilles, Justin, Miley.
       ```
     - #5 array.every(fn)
       - The last one is pretty uncommon but really handy. It's like kind of filter but returns a boolean rather than an array.
       
        ```
            function isMillionaire (person) {
                  return ['Justin Bieber', 'Miley Cyrus'].indexOf(person.firstName + ' ' + person.lastName);
              }

            if (users.every(isMillionaire)) {
                console.log('They are all rich!');
            } else {
                console.log('Someone in our group is not rich...');
            }
        ```
        
        ##### As a bonus there is also Array.some which is almost the same as every but returns true even if just one condition is true rather than all of them.
