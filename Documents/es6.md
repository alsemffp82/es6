---
theme : "serif"
transition: "slide"
highlightTheme: "darkula"
---

## The 'find' Helper

#### find will return the record if a particular element is found in the array.


---

# Syntax
### arr.find(callback[, thisArg])
<a href="#" class="navigate-down">
    
</a>

--

## Parameters

### callback
> Function to execute on each value in the array, 
taking three arguments:

--

* element
>The current element being processed in the array.
* index(*optional*)
>The index of the current element being processed in the array.
* array(*optional*)
>The array find was called upon.

--

### thisArg(*optional*)
>Object to use as this when executing callback.

--

## Return value
A value in the array if an element passes the test; otherwise, undefined.

---

### Example
```
let x = [
    {name:"jay", age:1},
    {name:"hulu", age:30}
]
x.find(obj => obj.name === "jay")
```

<div style="text-align: left; margin-left: 50px;"> then It will return </div>
```
{name:"jay",age:1}
```

---

## The 'every' Helper

#### if all elements in an array pass a test


---

## Syntax
### arr.every(callback[, thisArg])
<a href="#" class="navigate-down"></a>

--

## Parameters

### callback
> Function to test for each element, taking three arguments:

--

* currentValue (*required*)
>The current element being processed in the array.
* index(*Optional*)
>The index of the current element being processed in the array.
* array(*optional*)
>The array every was called upon.

--

### thisArg(*optional*)
>Value to use as this when executing callback.

--

## Return value
**true** if the callback function returns a truthy value for every array element; otherwise, **false**

---

### Example
```
[12, 5, 8, 130, 44].every(x => x >= 10); // false
[12, 54, 18, 130, 44].every(x => x >= 10); // true
```

---

## The 'some' Helper

#### if any of the elements in an array pass a test


---

## Syntax
### arr.some(callback[, thisArg])
<a href="#" class="navigate-down"></a>

--

## Parameters

### callback
> Function to test for each element, taking three arguments:

--

* currentValue 
>The current element being processed in the array.
* index(*Optional*)
>The index of the current element being processed in the array.
* array(*optional*)
>The array some() was called upon.

--

### thisArg(*optional*)
>Value to use as this when executing callback.

--

## Return value
**true** if the callback function returns a truthy value for any array element; otherwise, **false**

---

### Example

```
[2, 5, 8, 1, 4].some(x => x > 10);  // false
[12, 5, 8, 1, 4].some(x => x > 10); // true
```

---

## Spread syntax

### It allows an iterable to expand in places where 0+ arguments are expected.

---

## Syntax
1. myFunction(...iterableObj); => function calls
2. [...iterableObj, '4', 'five', 6]; => array literals or strings
3. let objClone = { ...obj }; => object literals

---

### Example
<a href="#" class="navigate-down"></a>


```
function myFunction(x, y, z) { }
var args = [0, 1, 2];
myFunction(...args);
```

--

```
function myFunction(v, w, x, y, z) { }
var args = [0, 1];
myFunction(-1, ...args, 2, ...[3]);
```

--

```
var obj1 = { one: '1' };
var obj2 = { two: '2', ...obj1 };
```

--

---

## Rest syntax

### It allows us to represent an indefinite number of arguments as an array.

---

## Syntax
1. function f(a, b, ...theArgs) {
  // ...
}

---

### Example

<a href="#" class="navigate-down"></a>

```
function fun1(...theArgs) {
  console.log(theArgs.length);
}

fun1();  // 0
fun1(5); // 1
fun1(5, 6, 7); // 3
```

--

```
function multiply(multiplier, ...theArgs) {
  return theArgs.map(function(element) {
    return multiplier * element;
  });
}

var arr = multiply(2, 1, 2, 3); 
console.log(arr); // [2, 4, 6]
```

--

```
function sortArguments() {
  var args = Array.from(arguments);
  var sortedArgs = args.sort();
  return sortedArgs;
}
console.log(sortArguments(5, 3, 7, 1)); // 1, 3, 5, 7
```
---