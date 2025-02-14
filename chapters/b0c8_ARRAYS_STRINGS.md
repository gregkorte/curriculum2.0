---
layout: default
title: A String Within a String
---

# A String Within a String

In this exercise, you will use a `for..of` loop and conditional logic with `if/else` blocks again. You will also use a new tool to find a smaller string value within a bigger string value. Additionally, you will use the logical OR operator `||`, which is similar to the logical AND operator `&&` used in previous exercises.

---

## Practice: Searching for Substrings

Below are interactive exercises where you can practice using `String.includes()` in conditional statements. Modify the code in each example and observe the output.

### Finding Words in Strings
<script async src="//jsfiddle.net/gczipr/jdbyr3o6/1/embed/js,result/dark/"></script>

### Counting Matches in an Array
<script async src="//jsfiddle.net/gczipr/m68wr0vp/1/embed/js,result/dark/"></script>

### Using OR Conditions in Search
<script async src="//jsfiddle.net/gczipr/q4jto9xv/1/embed/js,result/dark/"></script>

---

## Exercise: How Do You Take Your Coffee?

### Setup

```sh
cd
cd workspace
mkdir coffee-effects
cd coffee-effects
touch main.js
code .
```

Once VS Code starts, open the `main.js` file and copy the following code into the file.

```js
const coffees = [
    "light colombian roast", "hawaiian dark roast", "guatemalan blend medium roast",
    "dark madagascar blend", "jamaican dark blue", "jamaican medium roast",
    "salvador robusto light"
]

let output = ""

for (const coffee of coffees) {
    if (coffee.includes("light")) {
        output += `I'll have the ${coffee} and drink it black.`
    }
    else if (coffee.includes("medium")) {
        output += `I'll have the ${coffee} and add cream only.`
    }
    else if (coffee.includes("dark")) {
        output += `I'll have the ${coffee} and add cream and sugar.`
    }
    output += "\n"
}

console.log(output)
```

### Instructions

You start with an array of different coffee roasts around the world that you enjoy. Depending on the roast, you prepare the coffee differently. If it is a light roast, you drink it black. If it is a medium roast, you put cream in it. If it is a dark roast, you put cream and sugar in it.

Your job is to iterate the `coffees` array and output the following sentences for each coffee, replacing `xxx` with the full name of the coffee.

### Run Your Code

In your terminal, run your code with the following command.

```sh
node main.js
```

When you run the code, your output should follow these rules:

For light roast:

`"I'll have the xxx and drink it black."`

For medium roast:

`"I'll have the xxx and add cream only."`

For dark roast:

`"I'll have the xxx and add cream and sugar."`

---

## LLM Prompt for Deeper Understanding

To test your understanding, copy and paste the following prompt into an LLM of your choice:

> You are a Socratic tutor assessing my knowledge of using `String.includes()` and logical operators in JavaScript. First, ask me to explain how `String.includes()` works. Then, ask me to describe how to use logical OR (`||`) to check multiple conditions. Next, give me a short code snippet with an array of strings and ask me to filter specific values using `includes()`. Finally, ask me about real-world applications of substring searches in programming.

[Back to Supplement Foundations]({{ "/books/client_book0" | relative_url }})

