---
layout: default
title: Adding Items to an Array
---

## Adding Items to an Array

In this chapter, you will learn how to add items to an array.

## Review of String Interpolation

Before you read this chapter, this is a quick reminder about string interpolation. That weird word means that you can inject a variable's value into a string.

#### Example

```js
const giveUp = "give you up"
const letDown = "let you down"

console.log(`Never gonna ${giveUp}, never gonna ${letDown}`)
```

Output is "Never gonna give you up, never gonna let you down."

## Array Push

There is a classic hip-hop song from the 1980s that I always think of when I want to add a new value to an array. Arrays have a method on them named `.push()`. That method lets you add a new value as the last item in the array.

You will start off with this simple example where you have three pieces of paper that need to be copied. The original pieces of paper should not be touched. Therefore, you will end up with a new collection—an array—that will contain the copies.

Here's how you can add a new piece of paper to the collection that needs to be copied.

```js
const originals = [ "Original paper 1", "Original paper 2", "Original paper 3" ]

originals.push("Original paper 4")

console.log(originals)
```

This is the new content of the array:

```js
[ "Original paper 1", "Original paper 2", "Original paper 3", "Original paper 4"]
```

## Making Copies

Now it is time to combine the `for` loop with the `push()` method on an array to make a copy for each item in the `originals` array.

```js
const originals = [ "Original paper 1", "Original paper 2", "Original paper 3" ]
const copies = []  // Blank array that will contain the copies

for (const paper of originals) {
    const copy = `Copy of ${paper}`
    copies.push(copy)
}

console.log(copies)
```

---

## Practice: Exploring the Push Method

Below are interactive exercises where you can practice using the `.push()` method. Modify the code in each example and observe the output.

### Adding Elements with Push
<script async src="//jsfiddle.net/gczipr/j5em9z4x/1/embed/js,result/dark/"></script>

### Looping and Pushing into an Array
<script async src="//jsfiddle.net/gczipr/x1vwn06q/1/embed/js,result/dark/"></script>

### Creating a Dynamic List with Push
<script async src="//jsfiddle.net/gczipr/h9a2m4vk/1/embed/js,result/dark/"></script>

---

## Exercise: Making Mugs

### Setup

```sh
cd
cd workspace
mkdir making-mugs
cd making-mugs
touch main.js
code .
```

Once VS Code starts, open the `main.js` file and copy the following code into the file.

```js
const clay = [ "Clay", "Clay", "Clay", "Clay" ]
const toFireInKiln = []

for (const chunk of clay) {
    const mug = `${chunk} coffee mug`
    toFireInKiln.push(mug)
}

console.log(toFireInKiln)
```

### Instructions

Your task is to iterate over the array containing the chunks of clay, and after your code is done, the `toFireInKiln` array should contain the string value "Clay coffee mug" for every string in the `clay` array.

### Run Your Code

In your terminal, run your code with the following command.

```sh
node main.js
```

When you run the code, it should display the following:

```sh
[ "Clay coffee mug", "Clay coffee mug", "Clay coffee mug", "Clay coffee mug" ]
```

---

## LLM Prompt for Deeper Understanding

To test your understanding, copy and paste the following prompt into an LLM of your choice:

> You are a Socratic tutor assessing my knowledge of adding items to arrays in JavaScript. First, ask me to explain how the `.push()` method works. Then, ask me to describe how a `for` loop can be combined with `.push()` to dynamically add items to an array. Next, give me a short code snippet and ask me to predict the resulting array after using `.push()`. Finally, ask me about the advantages of using `.push()` over manually modifying an array.

[Back to Supplement Foundations]({{ "/books/client_book0" | relative_url }})

