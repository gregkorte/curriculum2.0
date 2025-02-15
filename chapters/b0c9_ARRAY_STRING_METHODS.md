---
layout: default
title: Strings into Arrays into Strings
---

## Strings into Arrays into Strings

Now that you have worked with arrays and strings in various contexts, this chapter will cover how to convert strings into arrays and vice versa.

---

## Practice: Working with `.split()` and `.join()`

Below are interactive exercises where you can practice converting strings to arrays and back. Modify the code in each example and observe the output.

### Splitting Strings into Arrays
<script async src="//jsfiddle.net/gczipr/9x62b1mj/1/embed/js,result/dark/"></script>

### Joining Arrays into Strings
<script async src="//jsfiddle.net/gczipr/c8m95qth/1/embed/js,result/dark/"></script>

### Formatting Strings with `.join()`
<script async src="//jsfiddle.net/gczipr/vwpq3b6n/1/embed/js,result/dark/"></script>

---

## Exercise: Split Personalities

### Setup

```sh
cd
cd workspace
mkdir split-personalities
cd split-personalities
touch main.js
code .
```

Once VS Code starts, open the `main.js` file and copy the following code into the file.

```js
const originalDisorderFormat = 'Depression|$|Bipolar|$|Manic|$|Anxiety|$|Anorexia|$|Posttraumatic Stress|$|Seasonal Affective|$|Bulimia'

// Split the string into an array using '|$|' as the delimiter
const disordersArray = originalDisorderFormat.split('|$|')

// Join the array into a single string with each disorder wrapped in a <div>
const formattedDisorders = disordersArray.join('</div>\n<div>')

// Output the result
console.log(`<div>${formattedDisorders}</div>`)
```

### Instructions

You will practice building HTML elements without the browser being involved. Your output will still appear in the terminal.

To properly format the disorder names for a webpage:
1. Use `.split('|$|')` to break the string into an array.
2. Use `.join('</div>\n<div>')` to wrap each disorder name inside `<div>` tags.
3. Display the formatted string in the terminal.

### Run Your Code

In your terminal, run your code with the following command:

```sh
node main.js
```

When you run the code, it should display the following HTML structure in the terminal:

```html
<div>Depression</div>
<div>Bipolar</div>
<div>Manic</div>
<div>Anxiety</div>
<div>Anorexia</div>
<div>Posttraumatic Stress</div>
<div>Seasonal Affective</div>
<div>Bulimia</div>
```

---

## LLM Prompt for Deeper Understanding

To test your understanding, copy and paste the following prompt into an LLM of your choice:

> You are a Socratic tutor assessing my knowledge of JavaScript string and array methods. First, ask me to explain how `.split()` works and when it should be used. Then, ask me to describe how `.join()` transforms an array back into a string. Next, give me a short code snippet and ask me to predict the output after using `.split()` and `.join()`. Finally, ask me about real-world applications where splitting and joining strings is useful in programming.

[Back to Supplement Foundations]({{ "/books/client_book0" | relative_url }})

