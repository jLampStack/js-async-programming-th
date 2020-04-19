# View Project

## https://jlampstack.github.io/js-async-programming-th/

# Readme

https://github.com/jLampStack/js-async-programming-th/blob/master/README.md

# Resources

https://teamtreehouse.com/library/asynchronous-programming-with-javascript

## setTimeout()
https://www.w3schools.com/jsref/met_win_settimeout.asp



# Asynchronous Programming

## INTRO

* JavaScript is synchronous and single threaded. If you're executing a block of code then no other JavaScript on that page will be executed until the block is complete. This is known as blocking behaviour.

* **Real Life Example** is a person who multi-tasks (Asynchronous) opposed to doing one thing at a time (Synchronous).

  * **Asynchronous Example:** If your on the phone you can also make coffee and toast at the same time. You would put coffee in the pot, walk to the toaster, and pop in the toast while waiting for the coffee to brew.

  * **Synchronous Example:** Is the opposite of Asyncrhonous and performs operations one thing at a time. Imaging how long it woudl take if we didn't start breakfast until after getting off the phone, or if we didn't pop in the toast until the coffee was completely brewed. This would take a really long time. 

* **JavaScript Example:** Imagine an AJAX request is made to the server, the page stops loading and doesn't continue to load the rest of the page until the request is complete. This can potentially take a long time and make the program feel stuck. You would lose web traffic because the website isn't optimized.

* Asynchronous should be used if your program needs to run a task that takes time so that other parts of the program can carry on and do what they need to do.


## 3 FUNCTIONS THAT AVOID BLOCKING BEHAVOIUR
  * setTimeout

  * callbacks
  * promises
  * async/await

## setTimeout()

EXAMPLE:
```
<script>
    console.log('ONE...');

      setTimeout(() => {
        console.log('TWO...');
      }, 5000);

    console.log('THREE...');
  </script>
```

* setTImeout() freezes the anonymous function for 5 seconds allowing the rest of the program to run

* After 5 seconds it runs again

* The console will long in the following order: ONE... THREE... TWO... 

* Without setTimeout() the program would load: ONE... TWO... THREE...

  * TWO would freeze the rest of the program from performing actions until it's complete 

* setTimeout() is considered  Asynchronous in that it breaks the synchronous flow, but it's not actually going to execute concurrently/on a separate thread. There are better ways of doing this.



The callback queue is a holding area for callbacks that are waiting to be put on the call stack and eventually executed.

Any time the call stack is empty, the event loop pushes the first task from the callback queue onto the call stack and runs it.

JavaScript is a synchronous, single-threaded language.

The call stack is a mechanism the JavaScript engine uses to able to keep track of the order of function calls and where it is in a program at any given moment.

An API mashup is a site or app that is created using two data sources.




