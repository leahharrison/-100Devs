# Functions

## [Is "else" required?](https://javascript.info/function-basics#is-else-required)

The following function returns ```true``` if the parameter ```age``` is greater than ```18```.

Otherwise it asks for a confirmation and returns its result:

```
function checkAge(age) {
  if (age > 18) {
    return true;
  } else {
    // ...
    return confirm('Did parents allow you?');
  }
}
```

Will the function work differently if else is removed?

```
function checkAge(age) {
  if (age > 18) {
    return true;
  }
  // ...
  return confirm('Did parents allow you?');
}
```

No difference! In both cases, return confirm('Did parents allow you?') executes exactly when the if condition is falsy.


## [Rewrite the function using '?' or '||'](https://javascript.info/function-basics#rewrite-the-function-using-or)

The following function returns ```true``` if the parameter ```age``` is greater than ```18```.

Otherwise it asks for a confirmation and returns its result.

```
function checkAge(age) {
  if (age > 18) {
    return true;
  } else {
    return confirm('Did parents allow you?');
  }
}
```

Rewrite it, to perform the same, but without ```if```, in a single line.

Make two variants of ```checkAge```:

1. Using a question mark operator ```?```
```
function checkAge(age) {
  return (age > 18) ? true : confirm('Did parents allow you?');
}
```

2. Using OR ```||```
```
function checkAge(age) {
  return (age > 18) || confirm('Did parents allow you?');
}
```


## [Function min(a, b)](https://javascript.info/function-basics#function-min-a-b)

Write a function ```min(a,b)``` which returns the least of two numbers ```a``` and ```b```.

For instance:
```
min(2, 5) == 2
min(3, -1) == -1
min(1, 1) == 1
```

A solution using ```if```:
```
function min(a, b) {
  if (a < b) {
    return a;
  } else {
    return b;
  }
}
```

A solution with a question mark operator ```'?'```:
```
function min(a, b) {
  return a < b ? a : b;
}
```


## [Funtion pow(x, n)](https://javascript.info/function-basics#function-pow-x-n)

Write a function ```pow(x,n)``` that returns ```x``` in power ```n```. Or, in other words, multiplies ```x``` by itself ```n``` times and returns the result.
```
pow(3, 2) = 3 * 3 = 9
pow(3, 3) = 3 * 3 * 3 = 27
pow(1, 100) = 1 * 1 * ...* 1 = 1
```
Create a web-page that prompts for ```x``` and ```n```, and then shows the result of ```pow(x,n)```.

P.S. In this task the function should support only natural values of ```n```: integers up from ```1```.

```
function pow(x, n) {
  let result = x;

  for (let i = 1; i < n; i++) {
    result *= x;
  }

  return result;
}

let x = prompt("x?", '');
let n = prompt("n?", '');

if (n < 1) {
  alert(`Power ${n} is not supported, use a positive integer`);
} else {
  alert( pow(x, n) );
}
```
