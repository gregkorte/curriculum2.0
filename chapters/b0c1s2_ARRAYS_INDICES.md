---
layout: default
title: Position of Items in an Array
---

## Position of Items in an Array

As mentioned in the introduction, the most common type of collection in JavaScript is the array. An array can be identified by the use of square brackets. The `[` and the `]` characters define an array. Here's a simple definition of an array. Think of it as an empty basket. Nothing is in it yet.

```js
const appleBasket = []
```

This is different from previous exercises where you assigned very concrete values to variables, like these.

```js
const age = 37  // Clear, concrete numeric value
const name = "Edward McKnight" // Clear, concrete string value
```

You can either declare a new array as empty, like above, or you can provide it with initial values upon declaration. For example, if you want some common color names to be in your array, you can provide those inside the square brackets.

```js
const myFavoriteColors = [ "red", "violet", "pink", "green", "white", "orange" ]
```

The `myFavoriteColors` variable still has a single value, but it is more abstract. Its value is a collection of strings, or more specifically, an array of strings.

The placement of each value in that array is called its "index." The indexing of an array starts at zero, not one. That is, the item at index 0 of the above array is the string value "red."

- The item at index 0 is the string "red"
- The item at index 1 is the string "violet"
- The item at index 2 is the string "pink"
- The item at index 3 is the string "green"
- The item at index 4 is the string "white"
- The item at index 5 is the string "orange"

You can, if you need to, look at the item at a specific index by using the following syntax.

```js
arrayVariable[index number]
```

So if you want to `console.log()` the color "white," you would write the following code.

```js
const whiteColor = myFavoriteColors[4]
console.log(whiteColor)
```

If you want to `console.log()` the color "violet," you would write the following code.

```js
const violetColor = myFavoriteColors[1]
console.log(violetColor)
```

---

## Practice: Exploring Indexing in Arrays

Below are interactive exercises where you can practice accessing elements in an array. Modify the code in each example and observe the output.

### Accessing Elements by Index
<script async src="//jsfiddle.net/gczipr/4s7m8fap/1/embed/js,result/dark/"></script>

### Modifying Elements at a Specific Index
<script async src="//jsfiddle.net/gczipr/v2p36wxm/1/embed/js,result/dark/"></script>

### Finding the Last Element of an Array
<script async src="//jsfiddle.net/gczipr/kuy43dpt/1/embed/js,result/dark/"></script>

---

## Exercise: Glass Scrubber

### Setup

```sh
cd
cd workspace
mkdir glass-scrubber
cd glass-scrubber
touch main.js
code .
```

Once VS Code starts, open the `main.js` file and copy the following code into the file.

```js
const dishes = [
    "Dinner plate", "Water glass", "Salad bowl",
    "Dinner plate", "Wine glass", "Spoon",
    "Spoon", "Fork", "Salad bowl", "Whiskey glass",
    "Fork", "Spoon", "Fork"
]

/*
    Declare three variables to store the string value
    of a glass in the array. Use the correct index to
    get the right value.
*/

console.log("I am cleaning the following glasses:")

// Put each variable in one of the parentheses below
console.log()
console.log()
console.log()
```

### Instructions

Your job is to identify the 3 dirty glasses by using their index in the array and assign each one to its own variable.

### Run Your Code

In your terminal, run your code with the following command.

```sh
node main.js
```

When you run the code, it should display the following.

```sh
I am cleaning the following glasses:
Water glass
Wine glass
Whiskey glass
```

---

## LLM Prompt for Deeper Understanding

To test your understanding, copy and paste the following prompt into an LLM of your choice:

> You are a Socratic tutor assessing my knowledge of JavaScript array indexing. First, ask me to explain how JavaScript arrays are indexed. Then, ask me to describe how to access an element at a specific index. Next, give me a short code snippet with an array and ask me to identify the values stored at certain indices. Finally, ask me about the benefits of using indexed collections over individual variables.

[Back to Supplement Foundations]({{ "/books/client_book0" | relative_url }})

