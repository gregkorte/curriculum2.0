---
layout: default
title: Using the Length of an Array
---

## Using the Length of an Array

Arrays have a `.length` property that tells you how many items are in the array.

---

## Rainfall

You can perform whatever task you want inside a `for` loop. In the previous exercises, you have used the `.push()` method to build up a new array based on the items in another array. Here is an example of building up a total value.

A meteorologist wants to determine the total rainfall for a year and then calculate the average rainfall per month.

```js
const rainfallPerMonth = [ 5, 12, 18, 20, 22, 17, 29, 21, 20, 22, 30, 9 ]
let totalRainfall = 0  // Start at 0 and add to it in the loop

for (const rain of rainfallPerMonth) {
    totalRainfall += rain
}

// To find the average, you take the total and divide by the number of items
const averageRainfall = totalRainfall / rainfallPerMonth.length

console.log(`Total rainfall was ${totalRainfall} inches`)
console.log(`Average rainfall was ${averageRainfall} inches`)
```

Put that code into the code editor and run it to see the output.

---

## Practice: Using `.length` in Calculations

Below are interactive exercises where you can practice using the `.length` property in calculations. Modify the code in each example and observe the output.

### Summing Values in an Array
<script async src="//jsfiddle.net/gczipr/7ojafk92/1/embed/js,result/dark/"></script>

### Calculating an Average from an Array
<script async src="//jsfiddle.net/gczipr/2abn3w48/1/embed/js,result/dark/"></script>

### Finding the Length of a Dynamically Updated Array
<script async src="//jsfiddle.net/gczipr/8skym4z1/1/embed/js,result/dark/"></script>

---

## Exercise: Grocery Expenses

### Setup

```sh
cd
cd workspace
mkdir grocery-expenses
cd grocery-expenses
touch main.js
code .
```

Once VS Code starts, open the `main.js` file and copy the following code into the file.

```js
const monthlyExpenses = [ 201.43, 189.22, 132.09, 238.85, 195.41 ]
let totalExpense = 0

for (const expense of monthlyExpenses) {
    // Add the current monthly cost to the value of totalExpense
    totalExpense += expense
}

// Calculate your average monthly food costs
const averageExpense = totalExpense / monthlyExpenses.length

// Make sure you use backticks for multi-line string output
console.log(`On average, I spend ${averageExpense.toFixed(1)} dollars on groceries per month.`)
console.log(`So far this year, I have spent ${totalExpense.toFixed(0)} dollars on groceries.`)
```

### Instructions

Update the code to calculate your average monthly grocery expenses for the five months' worth of expenses that have been recorded in the array.

### Run Your Code

In your terminal, run your code with the following command.

```sh
node main.js
```

When you run the code, it should display the following.

```sh
On average, I spend 191.4 dollars on groceries per month.
So far this year, I have spent 957 dollars on groceries.
```

---

## LLM Prompt for Deeper Understanding

To test your understanding, copy and paste the following prompt into an LLM of your choice:

> You are a Socratic tutor assessing my knowledge of using the `.length` property in JavaScript arrays. First, ask me to explain how `.length` works and what it returns. Then, ask me to describe how I can use `.length` to calculate an average value from an array. Next, give me a short code snippet and ask me to predict the output based on the array’s length. Finally, ask me about practical scenarios where using `.length` is essential in programming.

[Back to Supplement Foundations]({{ "/books/client_book0" | relative_url }})

