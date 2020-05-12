
## Callbacks

* More complexly put: In JavaScript, functions are objects. Because of this, functions can take functions as arguments, and can be returned by other functions. Functions that do this are called higher-order functions. Any function that is passed as an argument is called a callback function.

#### Why do we need Callbacks?
For one very important reason — JavaScript is an event driven language. This means that instead of waiting for a response before moving on, JavaScript will keep executing while listening for other event

- Callbacks are a way to make sure certain code doesn’t execute until other code has already finished execution.

```
function doHomework(subject, callback) {
  alert(`Starting my ${subject} homework.`);
  callback();
}
function alertFinished(){
  alert('Finished my homework');
}
doHomework('math', alertFinished);
```
We’ve passed the alertFinished function definition as an argument during our doHomework() function call!

output : starting followed by finished. 

The main difference between callbacks and promises is that with callbacks you tell the executing function what to do when the asynchronous task completes, whereas with promises the executing function returns a special object to you (the promise) and then you tell the promise what to do when the asynchronous task completes.

### References :

1. https://codeburst.io/javascript-what-the-heck-is-a-callback-aba4da2deced
2. https://stackoverflow.com/questions/38425751/returning-chrome-storage-api-value-without-function
3. https://itnext.io/javascript-promises-vs-rxjs-observables-de5309583ca2

