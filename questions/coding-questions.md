# Coding Questions:

*Question: What is the value of `foo`?*
```javascript
var foo = 10 + '20';
```
*Answer:* `'1020'`. The `+` operator works against numbers and strings. The string in the expression causes JavaScript to assume string concatenation instead of numerical calculation.

*Question: What will be the output of the code below?*
```javascript
console.log(0.1 + 0.2 == 0.3);
```
*Answer:* `false`. Floating point calculations in JavaScript are weird.

*Question: How would you make this work?*
```javascript
add(2, 5); // 7
add(2)(5); // 7
```
*Answer:* [https://codepen.io/awayken/pen/MXaPjp?editors=0012]

*Question: What value is returned from the following statement?*
```javascript
"i'm a lasagna hog".split("").reverse().join("");
```
*Answer:* `"goh angasal a m'i"`. `split()` turns string to array, `reverse()` reverses array, `join()` turns array into string.

*Question: What is the value of `window.foo`?*
```javascript
( window.foo || ( window.foo = "bar" ) );
```
*Answer:* `"bar"`. The `||` will fail on `window.foo` since `undefined` is falsey and will then execute the right-hand side defining `window.foo` as equal to `"bar"`.

*Question: What is the outcome of the two alerts below?*
```javascript
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);
```
*Answer:* Alert 1: `"Hello World"`. Alert 2: `"Hello undefined"` / Throws: Uncaught ReferenceError: bar is not defined

*Question: What is the value of `foo.length`?*
```javascript
var foo = [];
foo.push(1);
foo.push(2);
```
*Answer:* 2.

*Question: What is the value of `foo.x`?*
```javascript
var foo = {n: 1};
var bar = foo;
foo.x = foo = {n: 2};
```
*Answer:* `undefined`. I think the right-hand side operation undefines the left hand side.

*Question: What does the following code print?*
```javascript
console.log('one');
setTimeout(function() {
  console.log('two');
}, 0);
console.log('three');
```
*Answer:* `onethreetwo`.

*Question: What is the difference between these four promises?*
```javascript
doSomething().then(function () {
  return doSomethingElse();
});

doSomething().then(function () {
  doSomethingElse();
});

doSomething().then(doSomethingElse());

doSomething().then(doSomethingElse);
```
*Answer:* First will return the result of doing something else. Second will do something else but not return anything. Third will execute something else immediately but result will follow proper then. Fourth is equivalent to second by passing function reference instead. [https://codepen.io/awayken/pen/pKjxKw?editors=0012]
