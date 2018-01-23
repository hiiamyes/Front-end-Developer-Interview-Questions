# Front-end Job Interview Questions

This file contains a number of front-end interview questions that can be used when vetting potential candidates. It is by no means recommended to use every single question here on the same candidate (that would take hours). Choosing a few items from this list should help you vet the intended skills you require.

**Note:** Keep in mind that many of these questions are open-ended and could lead to interesting discussions that tell you more about the person's capabilities than a straight answer would.

## Table of Contents

1. [General Questions](#general-questions)
1. [HTML Questions](#html-questions)
1. [CSS Questions](#css-questions)
1. [JS Questions](#js-questions)
1. [Testing Questions](#testing-questions)
1. [Performance Questions](#performance-questions)
1. [Network Questions](#network-questions)
1. [Coding Questions](#coding-questions)
1. [Fun Questions](#fun-questions)

## Getting Involved

1. [Contributors](#contributors)
1. [How to Contribute](https://github.com/h5bp/Front-end-Developer-Interview-Questions/blob/master/CONTRIBUTING.md)
1. [License](https://github.com/h5bp/Front-end-Developer-Interview-Questions/blob/master/LICENSE.md)

#### General Questions:

* What did you learn yesterday/this week?

> graphql mutation

* What excites or interests you about coding?

> Give your the ability, power to make your imagine true.
> Able to fast prototyping, scaling up, and not limited a lot by hardware.

* What is a recent technical challenge you experienced and how did you solve it?

> Auto deploy the api service of my side project on a linode machine.

> First try using jenkins, and finally learned that only gitbook is needed and enough.

* What UI, Security, Performance, SEO, Maintainability or Technology considerations do you make while building a web application or site?
* Talk about your preferred development environment.

> vscode, git, docker, ci

* Which version control systems are you familiar with?

> git

* Can you describe your workflow when you create a web page?

> create-react-app > deploy to netlify

* If you have 5 different stylesheets, how would you best integrate them into the site?
* Can you describe the difference between progressive enhancement and graceful degradation?
* How would you optimize a website's assets/resources?

> cdn?

* How many resources will a browser download from a given domain at a time?

  * What are the exceptions?

> check http://www.browserscope.org/?category=network&v=1

* Name 3 ways to decrease page load (perceived or actual load time).
* If you jumped on a project and they used tabs and you used spaces, what would you do?

> If there is editor config setted, just use it for auto formatting. If not, set it down or discuss with ppl for choosing one and setting it down

* Describe how you would create a simple slideshow page.

> statis site generator + css framework, gastby.js + netlify + bluma/bootstrap

* If you could master one technology this year, what would it be?

>

* Explain the importance of standards and standards bodies.
* What is Flash of Unstyled Content? How do you avoid FOUC?
* Explain what ARIA and screenreaders are, and how to make a website accessible.
* Explain some of the pros and cons for CSS animations versus JavaScript animations.
* What does CORS stand for and what issue does it address?

#### HTML Questions:

* What does a `doctype` do?

> Tell browser how to compile the code.

> Without the DOCTYPE you are forcing the browsers to render in Quirks Mode.

> Informs the browser which version of HTML (or XML) you used to write the document. Doctype is a declaration, not a tag; you can also refer to it as "document type declaration", or "DTD" for short.

> Quirks Mode and Standards Mode. https://goo.gl/8R2XaG

* What's the difference between full standards mode, almost standards mode and quirks mode?
* What's the difference between HTML and XHTML?
* Are there any problems with serving pages as `application/xhtml+xml`?
* How do you serve a page with content in multiple languages?
* What kind of things must you be wary of when design or developing for multilingual sites?
* What are `data-` attributes good for?

> https://developer.mozilla.org/en-US/docs/Learn/HTML/Howto/Use_data_attributes

> data-\* attributes allow us to store extra information on standard, semantic HTML elements without other hacks such as non-standard attributes, extra properties on DOM, or Node.setUserData().

```
// html
<article
  data-columns="3">
...
</article>

// js
article.dataset.columns // "3"

// css
article::before {
  content: attr(data-columns);
}
article[data-columns='3'] {
  width: 400px;
}
```

> Do not store content that should be visible and accessible in data attributes, because assistive technology may not access them. In addition, search crawlers may not index data attributes' values.

* Consider HTML5 as an open web platform. What are the building blocks of HTML5?
* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.

> http://jerryzou.com/posts/cookie-and-web-storage/

* Describe the difference between `<script>`, `<script async>` and `<script defer>`.
* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?
* What is progressive rendering?
* Why you would use a `srcset` attribute in an image tag? Explain the process the browser uses when evaluating the content of this attribute.
* Have you used different HTML templating languages before?

#### CSS Questions:

* What is the difference between classes and IDs in CSS?
* What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?

> Like reset, it's goal is consistency across browsers. But it does so by preserving useful style defaults rather than "erasing" all styles. It helps correct common bugs that reset doesn't deal with (font inheritance by form elements, button styling in iOS).

* Describe Floats and how they work.

> It's a box that is pulled to the left or right and let the following content flow along its side. They are still in the flow of the page, but whereas the elements used to be stacked vertically, now they're side by side. Very commonly used for things like navigations. Has an annoying collapsing effect on the parent container. Fixed by clearing the float in the container.

* Describe z-index and how stacking context is formed.

> https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Positioning/Understanding_z_index/The_stacking_context

* Describe BFC(Block Formatting Context) and how it works.

> http://lucybain.com/blog/2015/css-block-formatting-context/

> https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Block_formatting_context

> http://maxdesign.com.au/jobs/sample-block-formatting-context/index.htm

* What are the various clearing techniques and which is appropriate for what context?
* Explain CSS sprites, and how you would implement them on a page or site.
* What are your favourite image replacement techniques and which do you use when?
* How would you approach fixing browser-specific styling issues?

> rewrite with another solution

* How do you serve your pages for feature-constrained browsers?
  * What techniques/processes do you use?
* What are the different ways to visually hide content (and make it available only for screen readers)?

> #1: visibility: hidden

> #2: width: 0; height: 0;

> #3: text-indent: -1000px

> #4: absolute position off the screen

* Have you ever used a grid system, and if so, what do you prefer?
* Have you used or implemented media queries or mobile specific layouts/CSS?
* Are you familiar with styling SVG?
* How do you optimize your webpages for print?
* What are some of the "gotchas" for writing efficient CSS?
* What are the advantages/disadvantages of using CSS preprocessors?

  > Advantages
  >
  > * better oranization from nesting them
  > * ability to define variables and mixins
  > * have mathematical functions
  > * joining multiple files
  > * in some cases, cleaner syntaxes

  > Disadvantages
  >
  > * mainly for designers not comfortable on the command line or programming concepts

* Describe what you like and dislike about the CSS preprocessors you have used.

* How would you implement a web design comp that uses non-standard fonts?

  > #1: use @font-face to render a font (uses src for hard resources)

  > #2: can just link to a webfont as a stylesheet, use @import, or javascript

* Explain how a browser determines what elements match a CSS selector.

> Browsers read selectors from right-to-left. First looks for all elements matching the key selector (the right-most). Then checks if it matches or is under the next (left-most) element.

* Describe pseudo-elements and discuss what they are used for.
* Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.

> For display purpose, every element in the page is considered a box. The box model refers to the specification of the box attributes such as the width, padding, border and margin. You can change the box model by setting the box-sizing property. Some values are: content-box (default), padding-box, and border-box

> * Content-box: width & height includes content but not padding/border/margin

> * Padding-box: include up to padding

> * Border-box: include up to border, but not margin

* What does `* { box-sizing: border-box; }` do? What are its advantages?

> make all dom's box-sizing to be border-box so that width and height will not be affected by padding and marging

* List as many values for the display property that you can remember.
* What's the difference between inline and inline-block?
* What's the difference between a relative, fixed, absolute and statically positioned element?
* The 'C' in CSS stands for Cascading. How is priority determined in assigning styles (a few examples)? How can you use this system to your advantage?

- What existing CSS frameworks have you used locally, or in production? How would you change/improve them?
- Have you played around with the new CSS Flexbox or Grid specs?
- How is responsive design different from adaptive design?
- Have you ever worked with retina graphics? If so, when and what techniques did you use?
- Is there any reason you'd want to use `translate()` instead of _absolute positioning_, or vice-versa? And why?

#### JS Questions:

* Explain event delegation

> JavaScript event delegation is a simple technique by which you add a single event handler to a parent element in order to avoid having to add event handlers to multiple child elements.

* Explain how `this` works in JavaScript

> `this` is neither a reference to the function itself, nor is it a reference to the function's lexical scope. `this` is actually a binding that is made when a function is invoked, and what it references is determined entirely by the call-site where the function is called.

* Explain how prototypal inheritance works

> http://lucybain.com/blog/2014/prototypal-inheritance/ > `[[Prototype]]`

* What do you think of AMD vs CommonJS?
* Explain why the following doesn't work as an IIFE: `function foo(){ }();`.
  * What needs to be changed to properly make it an IIFE?
* What's the difference between a variable that is: `null`, `undefined` or undeclared?

> Undeclared variables are those that are not declared at all.

> Undefined variables are declared variables that were not given a value. It is also a type.

> Null is an object that indicates lack of a value.

* How would you go about checking for any of these states?

> Null and undefined are the same value but different types:

> null == undefined // true

> null === undefined // false

* What is a closure, and how/why would you use one?

> Closure is when a function can remember and access its lexical scope even when it's invoked outside its lexical scope.

* Can you describe the main difference between a `forEach` loop and a `.map()` loop and why you would pick one versus the other?
* What's a typical use case for anonymous functions?
* How do you organize your code? (module pattern, classical inheritance?)
* What's the difference between host objects and native objects?
* Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?
* What's the difference between `.call` and `.apply`?

> Explicit Binding
> They both take, as their first parameter, an object to use for the this , and then invoke the function with that this specified.
> With respect to this binding, call(..) and apply(..) are identical.
> The fundamental difference is that call() accepts an argument list, while apply() accepts a single array of arguments.
> `func.apply(thisArg, [argsArray])` > `fun.call(thisArg[, arg1[, arg2[, ...]]])`

* Explain `Function.prototype.bind`.

> Hard Binding
> Unfortunately, explicit binding alone still doesn't offer any solution to the issue mentioned previously, of a function "losing" its intended this binding, or just having it paved over by a framework, etc.
> Since hard binding is such a common pattern, it's provided with a built-in utility as of ES5: Function.prototype.bind.
> bind(..) returns a new function that is hard-coded to call the original function with the this context set as you specified.

* When would you use `document.write()`?
* What's the difference between feature detection, feature inference, and using the UA string?
* Explain Ajax in as much detail as possible.
* What are the advantages and disadvantages of using Ajax?
* Explain how JSONP works (and how it's not really Ajax).
* Have you ever used JavaScript templating?
  * If so, what libraries have you used?
* Explain "hoisting".
* Describe event bubbling.

[Event Propagation](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Examples#Example_5:_Event_Propagation)

> `event.stopPropagation()` stops the move upwards, but on the current element all other handlers will run.
> `event.stopImmediatePropagation()` stops the bubbling and prevent handlers on the current element from running.

![event flow](https://javascript.info/article/bubbling-and-capturing/eventflow.png)

* What's the difference between an "attribute" and a "property"?
* Why is extending built-in JavaScript objects not a good idea?
* Difference between document load event and document DOMContentLoaded event?
* What is the difference between `==` and `===`?
* Explain the same-origin policy with regards to JavaScript.
* Make this work:

```javascript
duplicate([1, 2, 3, 4, 5]); // [1,2,3,4,5,1,2,3,4,5]
```

* Why is it called a Ternary expression, what does the word "Ternary" indicate?
* What is `"use strict";`? what are the advantages and disadvantages to using it?
* Create a for loop that iterates up to `100` while outputting **"fizz"** at multiples of `3`, **"buzz"** at multiples of `5` and **"fizzbuzz"** at multiples of `3` and `5`
* Why is it, in general, a good idea to leave the global scope of a website as-is and never touch it?
* Why would you use something like the `load` event? Does this event have disadvantages? Do you know any alternatives, and why would you use those?
* Explain what a single page app is and how to make one SEO-friendly.
* What is the extent of your experience with Promises and/or their polyfills?
* What are the pros and cons of using Promises instead of callbacks?
* What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?
* What tools and techniques do you use debugging JavaScript code?
* What language constructions do you use for iterating over object properties and array items?
* Explain the difference between mutable and immutable objects.
  * What is an example of an immutable object in JavaScript?
  * What are the pros and cons of immutability?
  * How can you achieve immutability in your own code?
* Explain the difference between synchronous and asynchronous functions.
* What is event loop?
  * What is the difference between call stack and task queue?
* Explain the differences on the usage of `foo` between `function foo() {}` and `var foo = function() {}`
* What are the differences between variables created using `let`, `var` or `const`?

#### Testing Questions:

* What are some advantages/disadvantages to testing your code?
* What tools would you use to test your code's functionality?
* What is the difference between a unit test and a functional/integration test?
* What is the purpose of a code style linting tool?

#### Performance Questions:

* What tools would you use to find a performance bug in your code?
* What are some ways you may improve your website's scrolling performance?
* Explain the difference between layout, painting and compositing.

#### Network Questions:

* Traditionally, why has it been better to serve site assets from multiple domains?

> It's because browsers usually have limits on the number of concurrent downloads from a domain at a moment. So, serving assets from multiple domains can increase the concurrent level.

* Do your best to describe the process from the time you type in a website's URL to it finishing loading on your screen.

> When I enter a website's URL, in the transport layer, it will ask a local DNS what is the IP of the provided URL. We know the IP of the local DNS server by the DHCP protocol, when a node connects to internet and gets an IP address. After that, a browser will try to establish a TCP connection with a server having the retrieved IP by 3-way handshake. When it establish a TCP connection, the browser will form an HTTP request containing an HTTP header and body. After the HTTP request is sent and the server responds with an HTTP response, the browser will parse the HTTP response header and body, and will render the website. If the document contains additional assets, the browser will create HTTP requests for the assets and send them like above.

* What are the differences between Long-Polling, Websockets and Server-Sent Events?

- Explain the following request and response headers:

  * Diff. between Expires, Date, Age and If-Modified-...

    > Expires headers tell the browser whether they should request a specific file from the server or whether they should grab it from the browser's cache.

    > Date: The date and time that the message was sent

    > The Age response-header field conveys the sender's estimate of the amount of time since the response (or its revalidation) was generated at the origin server.

    > The If-Modified-Since request-header field is used with a method to make it conditional: if the requested variant has not been modified since the time specified in this field, an entity will not be returned from the server; instead, a 304 (not modified) response will be returned without any message-body.

  * Do Not Track
    > Do Not Track: disable either its tracking or cross-site user tracking.
  * Cache-Control
    > Cache-Control: Tells all caching mechanisms from server to client whether they may cache this object. It is measured in seconds.
  * Transfer-Encoding
    > Transfer-Encoding: The form of encoding used to safely transfer the entity to the user. Currently defined methods are: chunked, compress, deflate, gzip, identity.
  * ETag
    > ETag: An identifier for a specific version of a resource.
  * X-Frame-Options
    > X-Frame-Options can be used to indicate whether or not a browser should be allowed to render a page in a `<frame>`, `<iframe>` or `<object>`.

- What are HTTP methods? List all HTTP methods that you know, and explain them.

  > GET: The GET method is used to retrieve information from the given server using a given URI. Requests using GET should only retrieve data and should have no other effect on the data.

  > HEAD: Same as GET, but transfers the status line and header section only.

  > POST: A POST request is used to send data to the server, for example, customer information, file upload, etc. using HTML forms.

  > PUT: Replaces all current representations of the target resource with the uploaded content.

  > DELETE: Removes all current representations of the target resource given by a URI.

  > CONNECT: Establishes a tunnel to the server identified by a given URI.

  > OPTIONS: Describes the communication options for the target resource.

  > TRACE: Performs a message loop-back test along the path to the target resource.

#### Coding Questions:

_Question: What is the value of `foo`?_

```javascript
var foo = 10 + "20";
```

```
// https://developer.mozilla.org/en-US/docs/Mozilla/js-ctypes/Using_js-ctypes/Type_conversion
1020
```

_Question: What will be the output of the code below?_

```javascript
console.log(0.1 + 0.2 == 0.3);
```

```
false
// 0.1+0.2=0.30...4
```

_Question: How would you make this work?_

```javascript
add(2, 5); // 7
add(2)(5); // 7
```

```javascript
function add(a, b) {
  var sum = function(b) {
    return a + b;
  };
  if (typeof b == "undefined") {
    return sum;
  } else {
    return sum(b);
  }
}
```

_Question: What value is returned from the following statement?_

```javascript
"i'm a lasagna hog"
  .split("")
  .reverse()
  .join("");
```

`"goh angasal a m'i"`

_Question: What is the value of `window.foo`?_

```javascript
window.foo || (window.foo = "bar");
```

`bar`

_Question: What is the outcome of the two alerts below?_

```javascript
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);
```

```
Hello World
Uncaught ReferenceError: bar is not defined
```

_Question: What is the value of `foo.length`?_

```javascript
var foo = [];
foo.push(1);
foo.push(2);
```

2

_Question: What is the value of `foo.x`?_

```javascript
var foo = { n: 1 };
var bar = foo;
foo.x = foo = { n: 2 };
```

```js
// https://stackoverflow.com/questions/32342809/javascript-code-trick-whats-the-value-of-foo-x
// Let lref be the result of evaluating LeftHandSideExpression.
// Let rref be the result of evaluating AssignmentExpression.

foo
{n: 2}
bar
{n: 1, x: {n:2}}
```

_Question: What does the following code print?_

```javascript
console.log("one");
setTimeout(function() {
  console.log("two");
}, 0);
console.log("three");
```

one three two

> But the bottom line is console.log(1) and (4) are executed 'in-line' and 2 and 3 are placed in the event queue, and don't get executed until the all of the in-line code is executed.

_Question: What is the difference between these four promises?_

```javascript
doSomething().then(function() {
  return doSomethingElse();
});

doSomething().then(function() {
  doSomethingElse();
});

doSomething().then(doSomethingElse());

doSomething().then(doSomethingElse);
```

> https://pouchdb.com/2015/05/18/we-have-a-problem-with-promises.html

#### Fun Questions:

* What's a cool project that you've recently worked on?
* What are some things you like about the developer tools you use?
* Who inspires you in the front-end community?
* Do you have any pet projects? What kind?
* What's your favorite feature of Internet Explorer?
* How do you like your coffee?

#### Contributors:

This document started in 2009 as a collaboration of [@paul_irish](https://twitter.com/paul_irish) [@bentruyman](https://twitter.com/bentruyman) [@cowboy](https://twitter.com/cowboy) [@ajpiano](https://twitter.com/ajpiano) [@SlexAxton](https://twitter.com/slexaxton) [@boazsender](https://twitter.com/boazsender) [@miketaylr](https://twitter.com/miketaylr) [@vladikoff](https://twitter.com/vladikoff) [@gf3](https://twitter.com/gf3) [@jon_neal](https://twitter.com/jon_neal) [@sambreed](https://twitter.com/sambreed) and [@iansym](https://twitter.com/iansym).

It has since received contributions from over [100 developers](https://github.com/h5bp/Front-end-Developer-Interview-Questions/graphs/contributors).
