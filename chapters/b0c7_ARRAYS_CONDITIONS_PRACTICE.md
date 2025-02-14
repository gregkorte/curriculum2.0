---
layout: default
title: Conditions in Loops
---

## Conditions in Loops

You are going to practice your `for..of` loops some more. In this exercise, you are going to add an `if/else` code block inside the loop.

A quick example first.

```js
const wines = [ "red", "white", "white", "white", "red", "white", "red" ]
const wineCellar = []
const wineRefrigerator = []

for (const wine of wines) {
    if (wine === "red") {
        wineCellar.push(wine)
    }
    else {
        wineRefrigerator.push(wine)
    }
}

console.log(`
Contents of wine cellar: ${wineCellar}
Contents of wine refrigerator: ${wineRefrigerator}
`)
```

Feel free to copy that code into the editor and run it to see what happens.

In that example, you still iterate through the entire array, but depending on the value of the `wine` variable, one of two different things happens.

---

## Practice: Sorting Data with Conditions

Below are interactive exercises where you can practice using conditions inside loops. Modify the code in each example and observe the output.

### Sorting Elements into Two Categories
<script async src="//jsfiddle.net/gczipr/8wjstp4n/1/embed/js,result/dark/"></script>

### Counting Items in Categories
<script async src="//jsfiddle.net/gczipr/xv3j72bd/1/embed/js,result/dark/"></script>

### Using Conditions to Filter Data
<script async src="//jsfiddle.net/gczipr/4mpx9zqc/1/embed/js,result/dark/"></script>

---

## Exercise: Sleep Mode

### Instructions

You decide to track how much your sleep affects your mood on a day-to-day basis. You notice that if you get less than 7 hours of sleep, you are grumpy all day long. If you get 7 or more hours of sleep, you are in a happy mood all day.

You start recording how many hours of sleep you get every night for two weeks. Based on the hours of sleep, you want to generate a readable report that shows you how many days you were grumpy and how many days you were happy.

There is an array provided to you in the starter code for your tracked hours of sleep. You need to complete the code using the example above as a guide. One thing you will do differently is instead of putting the array in the output like the example does, you need to display the number of items in `grumpyHours` and the number of items in the `happyHours` arrays.

### Setup

```sh
cd
cd workspace
mkdir moods
cd moods
touch main.js
code .
```

Once VS Code starts, open the `main.js` file and copy the following code into the file.

```js
const hours = [ 6, 9, 7, 8, 6, 6, 8, 5, 9, 8, 7, 6, 7, 7, 8, 6, 9 ]
const grumpyHours = []
const happyHours = []

for (const sleep of hours) {
    if (sleep < 7) {
        grumpyHours.push(sleep)
    } else {
        happyHours.push(sleep)
    }
}

console.log(`I was grumpy on ${grumpyHours.length} days.`)
console.log(`I was happy on ${happyHours.length} days.`)
```

### Run Your Code

In your terminal, run your code with the following command.

```sh
node main.js
```

When you run the code, it should display the following.

```sh
I was grumpy on 6 days.
I was happy on 11 days.
```

---

## LLM Prompt for Deeper Understanding

To test your understanding, copy and paste the following prompt into an LLM of your choice:

> You are a Socratic tutor assessing my knowledge of using conditions inside loops in JavaScript. First, ask me to explain how an `if/else` statement works inside a `for..of` loop. Then, ask me to describe how to sort elements into different categories using conditionals. Next, give me a short code snippet and ask me to predict how the array will be split. Finally, ask me about the benefits of using conditionals inside loops for data processing.

[Back to Supplement Foundations]({{ "/books/client_book0" | relative_url }})

