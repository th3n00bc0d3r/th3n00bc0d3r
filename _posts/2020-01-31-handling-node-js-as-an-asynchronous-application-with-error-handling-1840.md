---
title: Handling Node.JS as an Asynchronous Application with Error Handling
date: '2020-01-31T10:40:55.897Z'
excerpt: >-
  This article is about implementing asynchronous calls in JavaScript and
  Node.JS.   In this article, y...
thumb_img_path: >-
  https://res.cloudinary.com/practicaldev/image/fetch/s--CptQWf0l--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://res.cloudinary.com/practicaldev/image/fetch/s--XtNOroCk--/c_imagga_scale%2Cf_auto%2Cfl_progressive%2Ch_420%2Cq_auto%2Cw_1000/https://dev-to-uploads.s3.amazonaws.com/i/yhdhnd613nc6yik5a5ew.jpg
comments_count: 0
positive_reactions_count: 6
tags: []
canonical_url: >-
  https://dev.to/th3n00bc0d3r/handling-node-js-as-an-asynchronous-application-with-error-handling-1840
layout: post
---
**This article is about implementing asynchronous calls in JavaScript and Node.JS.** 

In this article, you will learn how to implement the following coding practices

- differentiate between a Synchronous and Asynchronous Call
- execute functions in Concurrency
- execute Promises in an Asynchronous Call
- wait for a function to execute before continuing
- prevent a Node.JS Application from Breaking
- handle errors of consecutive running functions

Asynchronous calls are the knife and butter for a JavaScript developer. JavaScript, as a language, is a single-threaded engine which means that one thing can happen at one time. This is called single threading. This does bring in simplicity but holds one back from performing time-consuming operations. The time for an operation in a web application is termed as its operation cost, and for Javascript developers, pushing an application to be performative, means that we reduce this operation cost to as low as possible. This process of reducing the cost is called optimization of an application. Therefore, to run such concurrency in a Javascript code, we use asynchronous calls.

## **What is a synchronous call?**

A synchronous call the code that is being executed i.e the program itself, will wait for each line to run before moving on wards to the end of the program. It can be further illustrated by stating that each operation will complete before starting the next operation. The time needed to execute the operation is known as the latency or lag the user perceives. The order of the code matters in synchronous calls. Most of the code that you have written in Javascript is running as synchronous. 

*Sample Code of a Synchronous Call* 

{% raw %}```
const printToConsole = (msg) => {
  console.log(msg);
}

const myFunctionOne = () => {
  printToConsole('Hello From Soshace, I am Number One');
}

const myFunctionTwo = () => {
  printToConsole('Hello From Soshace, I am Number Two');
}

const displayMessages = () => {
  myFunctionOne();
  myFunctionTwo();
  printToConsole('Dude, I am from the Third');
}

displayMessages();
```{% endraw %}

*Output of the Code*

![](https://i.ibb.co/thmBk8n/Screenshot-2019-11-15-at-8-44-00-AM.png)

To better understand the output of the code, Javascript creates an environment which calls the main() function. The main() function is the single-core thread of Javascript itself. This environment is like a stack on top of which the displayMessage() function is added.

The displayMessage() function holds a set of functions. The first one that is executed is myFunctionOne() therefore it is added on the top of the execution stack. myFunctionTwo() functions follows and the last one to get executed is printToConsole() function. At this point, no function is executed — only queued, until no function is left in the program.

![](https://i.ibb.co/VLqCT28/call-stack-1.jpg)

Once there are no functions left, the queue starts emptying up one by one starting from the bottom which, in this case, first executes the main() thread and then the displayMessages() function. The first output in the console will be of myFunctionOne(), which is “Hello from Soshace, I am Number One”, then the second console output will be from myFunctionTwo(), which is “Hello from Soshace, I am Number Two”. After the last function, which is printToConsole() is out, it will finally output to the console “Dude, I am from the Third”. This environment created by Javascript is known as an Execution Context and the queuing process is known as the Call Stack.

![](https://i.ibb.co/wMcpzrt/call-stack-2.jpg)

### **What is an Execution Context?**

JavaScript creates an environment where it examines the code and performs basic execution tests for any possible errors and then executes the code. This is done as a global context so, if a new function gets executed, it will repeat the process. This environment is called the execution context.

### **What is a Call Stack?**

JavaScript creates a stack, where it keeps a record of the functions that are being run as code. This stack is a Last-In-First-Out (LIFO). When JavaScript runs the code, it adds the function into this stack and starts carrying it out. Any function further more down the line is pushed to it and carried out in order.

The diagram illustrates the creation of the execution context, which is the main(), and as it starts pouring in the function until it runs out of function to run.

**The Asynchronous Call**

In the following code, we are creating a delay function. The delay function promises us a value after it is executed in the console. A promise with respect to the delay function is an object that will return us a value somewhere in the future. Next we have written an async function that will execute the promises and at the end should print us a message.

{% raw %}```
const myDelay = (ms) => {
    return new Promise((resolve) => {
        setTimeout(() => {
            console.log('Delayed');
            resolve();
        }, ms);        
    })
}

const myFunction = async () => {
    myDelay(2000);
    myDelay(2000);
    console.log('End of the Line');
}

myFunction();
```{% endraw %}

*Output*

![](https://i.ibb.co/BPsJ8LZ/Screenshot-2019-11-15-at-9-48-33-AM.png)

As you can see, the code was executed in concurrency where it did not wait for the delay function to execute and moved to the end of the code to complete its call stack. This can be troublesome in use cases, where you want to wait for a value from a network call before proceeding on with the code. To fix such an issue we use the ‘await’ keyword in javascript.

{% raw %}```
const myDelay = (ms) => {
    return new Promise((resolve) => {
        setTimeout(() => {
            console.log('Delayed');
            resolve();
        }, ms);        
    })
}

const myFunction = async () => {
    <strong>await</strong> myDelay(2000);
    <strong>await</strong> myDelay(2000);
    console.log('End of the Line');
}

myFunction();
```{% endraw %}

*Output*

![](https://i.ibb.co/k49WZKf/Screenshot-2019-11-15-at-9-54-56-AM.png)

Now, our JavaScript will wait for the function to complete and keep its promise before rushing into completing the script. This is highly effective in doing network calls and waiting for data to form from the network. Once you receive the data then you can process the data received from the network call and proceed with your application. It also ensures that nothing is missed or skipped during the execution of the code.

**Handling Errors**

We are now creating a function that will help us simulate an error.

{% raw %}```
const simulateError = async () => {
    throw new Error('Failure!')
}

simulateError();
```{% endraw %}

*Output*

![](https://i.ibb.co/JBzL5pw/Screenshot-2019-11-15-at-10-03-35-AM.png)

This has literally broken our application, now, if this was a production-level application, one would lose all contact to the backend API and lose the server from serving people currently using the application which nobody wants.

{% raw %}```
const simulateError = async () => {
    throw new Error('Failure!')
}

simulateError()
.catch(
  (error) => {
  	console.log(error)
});
```{% endraw %}

The catch clause will ensure that our application is not broken from serving our clients. Let’s look at the output.

![](https://i.ibb.co/6g1m9PR/Screenshot-2019-11-15-at-10-10-58-AM.png)

As you can see, it has warned us of the same danger but has kept our application alive. This is helpful when working with production level apps that should not break out of the process and require manual restarting.

**Error Handling in a Chain of Promise Events**

A typical case would be of running multiple await statements and having a couple of them produce an error. The code can become really messy to handle it but there is a better way of doing it with a much cleaner code organization.

{% raw %}```
const simulateError = async () => {
    throw new Error('Failure!')
}
const produceMultipleErrors = async _ => {
  const one = await simulateError()
  const two = await simulateError()
  const three = await simulateError()
}
 
produceMultipleErrors()
    .catch(
        (error) => {
            console.log(error)
        });
```{% endraw %}

The above code will allow us to compile errors into a single stack and produce it as all the calls are asynchronously executed. This is a great error handling technique that comes in handy when writing bigger applications. Error handling is an important part of any application which a lot of developers overlook.

Recently, I did come up with various situations when building up my own social media, but this allowed me to solve the hiccups in my code in a much cleaner and more precise way. I think the use of asynchronous functions in your code helps you in making your application mode dynamic and robust, therefore promising that your application would eventually survive the hardened road bumps of the development stage into the production stage.

*[This post is also available on DEV.](https://dev.to/th3n00bc0d3r/handling-node-js-as-an-asynchronous-application-with-error-handling-1840)*


<script>
const parent = document.getElementsByTagName('head')[0];
const script = document.createElement('script');
script.type = 'text/javascript';
script.src = 'https://cdnjs.cloudflare.com/ajax/libs/iframe-resizer/4.1.1/iframeResizer.min.js';
script.charset = 'utf-8';
script.onload = function() {
    window.iFrameResize({}, '.liquidTag');
};
parent.appendChild(script);
</script>    
