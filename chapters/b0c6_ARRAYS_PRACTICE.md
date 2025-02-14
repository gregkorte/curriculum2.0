---
layout: default
title: Traveling Salesperson
---

# Traveling Salesperson

## Instructions

In this exercise, you will be doing what you did in the last one, but you will need to write more code yourself. You can even open up the last exercise in another browser window so that you can easily look at that code and write code here.

---

## Practice: Calculating Averages from an Array

Below are interactive exercises where you can practice summing and averaging numbers in an array. Modify the code in each example and observe the output.

### Summing Values in an Array
<script async src="//jsfiddle.net/gczipr/7ojafk92/1/embed/js,result/dark/"></script>

### Calculating an Average from an Array
<script async src="//jsfiddle.net/gczipr/2abn3w48/1/embed/js,result/dark/"></script>

### Finding the Total and Average Miles Traveled
<script async src="//jsfiddle.net/gczipr/8skym4z1/1/embed/js,result/dark/"></script>

---

## Setup

```sh
cd
cd workspace
mkdir traveling-salesperson
cd traveling-salesperson
touch main.js
code .
```

## Starter Code

```js
// You fill in some sample weekly miles traveled in this array
const weeklyMiles = [ 120, 150, 135, 160, 145, 170 ]

// Declare a variable to store the total. Initial value is 0.
let totalMiles = 0;

/*
    Iterate the array of miles with a for..of loop.
    Add each mileage to the total mileage variable.
*/
for (const miles of weeklyMiles) {
    totalMiles += miles;
}

// Declare a new variable to store the average miles over time
const averageMiles = totalMiles / weeklyMiles.length;

// Output the average miles and the total miles to the console
console.log(`I average ${averageMiles.toFixed(1)} miles each week.`);
console.log(`I have driven a total of ${totalMiles} miles.`);
```

## Run Your Code

In your terminal, run your code with the following command.

```sh
node main.js
```

When you run the code, it should display the following, but with actual numbers instead of the `xxx`.

```sh
I average xxx miles each week.
I have driven a total of xxx miles.
```

---

## LLM Prompt for Deeper Understanding

To test your understanding, copy and paste the following prompt into an LLM of your choice:

> You are a Socratic tutor assessing my knowledge of iterating over arrays and calculating totals and averages in JavaScript. First, ask me to explain how a `for..of` loop works. Then, ask me to describe how I can sum values inside an array. Next, give me a short code snippet with an array of numbers and ask me to calculate the total and average. Finally, ask me about practical scenarios where calculating averages from arrays is useful in programming.

[Back to Supplement Foundations]({{ "/books/client_book0" | relative_url }})

