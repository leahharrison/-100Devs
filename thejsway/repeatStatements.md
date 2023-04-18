# Repeat statements

## Carousel

Write a program that launches a carousel for 10 turns, showing the turn number each time.
```
for(i = 1; i <= 10; i++) {
  console.log(i);
}
```

When it's done, improve it so that the number of turns is given by the user.
```
let turns = Number(prompt('Input number of carousel turns:'))
while(turns <= 10) {
  console.log(turns);
  turns++;
}
```

## Parity

Check the following program that shows even numbers (divisible by 2) between 1 and 10.
```
for (let i = 1; i <= 10; i++) {
  if (i % 2 === 0) {
    console.log(`${i} is even`);
  }
}
```

This program uses the modulo operator ```%```, which calculates the remainder after division of one number by another. It's often used to assess number parity.
```
console.log(10 % 2); // 0 because 10 = 5 * 2 + 0
console.log(11 % 2); // 1 because 11 = 5 * 2 + 1
console.log(18 % 3); // 0 because 18 = 3 * 6 + 0
console.log(19 % 3); // 1 because 19 = 3 * 6 + 1
console.log(20 % 3); // 2 because 20 = 3 * 6 + 2
```

Improve the program so that it also shows odd numbers.
```
for(let i = 1; i <= 10; i++) {
  if(i % 2 === 0) {
    console.log(`${i} is even`);
  } else {
    console.log(`${i} is odd`);
  }
}
```

Improve it again to replace the initial number ```1``` by a number given by the user.
```
for(let i = Number(prompt('Input a number 1-10')); i <= 10; i++) {
  if(i % 2 === 0) {
    console.log(`${i} is even`);
  } else {
    console.log(`${i} is odd`);
  }
}
```

## Input validation

Write a program that continues to ask the user for a number until the entered number is less than or equal to 100.
```
while(Number(prompt('Enter a number less than or equal to 100')) > 100) {
  console.log('Please enter number less than or equal to 100')
 }
```

When you are done with the above, improve the program so that the terminating number is between 50 and 100.
```
let num = Number(prompt('Enter a number between 50 and 100'));
  while(num < 50 || num > 100) {
    num = Number(prompt('Please enter number between 50 and 100'));
  }
```

## Multiplication Table

Write a program that asks the user for a number, then shows the multiplication table for this number.
```
let n = Number(prompt('Please enter a number'));
for (i = 1; i <= 10; i++) {
  console.log(i * n);
}
```

When you are done, improve the program so it only accepts numbers between 2 and 9 (use the previous exercise as a blueprint).
```
let number = Number(prompt('Please enter a number'));
for (i = 1; i <= 10; i++) {
  if (number < 2 || number > 9) {
    number = Number(prompt('Please enter a number between 2 and 9'));
  } else {
    console.log (i * number);
  }
}
```

## Neither yes nor no

Write a program that plays "neither yes, nor no" with the user. Specifically, the programs asks the user to enter text until either "yes" or "no" is typed, which ends the game.

## FizzBuzz

Write a program that shows all numbers between 1 and 100 with the following exceptions:
- It shows "Fizz" instead if the number is divisible by 3.
- It shows "Buzz" instead if the number is divisible by 5 and not by 3.
- It shows "FizzBuzz" instead for numbers divisible both by 3 and by 5.
```
for (let i = 1; i <= 100; i++) {
  if (i % 3 === 0 && i % 5 === 0) {
    console.log ('FizzBuzz')
  } else if (i % 3 === 0) {
    console.log ('Fizz')
  } else if (i % 5 === 0) {
    console.log ('Buzz')
  } else {
    console.log (i)
  }
}
```
