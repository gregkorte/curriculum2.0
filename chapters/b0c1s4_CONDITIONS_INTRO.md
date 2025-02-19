---
layout: default
title: Fast Food
---

## Fast Food

If you have ever had the pleasure of working in a fast food restaurant, you remember how important automation and repetition are. There is very little variation in the food offerings, and machines and processes ensure that each product is produced in the same amount of time, with the exact same quantity of ingredients.

In this exercise, you are going to use the same processes as in the last chapter, but you will introduce an `if/else` code block inside the `for` loop. You will still have two arrays: the first contains the raw ingredients for food, and you will use the `.push()` method to add the finished food product to the other array. However, what value gets inserted into the new array will depend on what the raw ingredient is.

---

## Practice: Transforming Ingredients with Conditionals

Below are interactive exercises where you can practice using `if/else` logic in loops. Modify the code in each example and observe the output.

### Sorting Ingredients into Categories
<script async src="//jsfiddle.net/gczipr/1fwb6stz/1/embed/js,result/dark/"></script>

### Transforming Ingredients into Finished Food
<script async src="//jsfiddle.net/gczipr/4qv3nj86/1/embed/js,result/dark/"></script>

### Using Multiple Conditions for Sorting
<script async src="//jsfiddle.net/gczipr/xn38zypq/1/embed/js,result/dark/"></script>

---

## Exercise

### Setup

```sh
cd
cd workspace
mkdir fast-food
cd fast-food
touch main.js
code .
```

Once VS Code starts, open the `main.js` file and copy the following code into the file.

```js
const rawIngredients = [ "beef patty", "egg", "potato", "egg", "potato", "beef patty", "beef patty", "potato" ]
const finishedFood = []

for (const ingredient of rawIngredients) {
    if (ingredient === "egg") {
        finishedFood.push("biscuit");
    } else if (ingredient === "beef patty") {
        finishedFood.push("burger");
    } else if (ingredient === "potato") {
        finishedFood.push("fries");
    }
}

console.log(finishedFood);
```

### Instructions

You need to fill in the proper sections of the `for` loop to iterate over the `rawIngredients` array.

* If the current ingredient is "egg", then add "biscuit" to the finished foods array.
* If the current ingredient is "beef patty", then add "burger" to the finished foods array.
* If the current ingredient is "potato", then add "fries" to the finished foods array.

Don't hesitate to look at the code in your last exercise to help out with this one.

### Run Your Code

In your terminal, run your code with the following command.

```sh
node main.js
```

When you run the code, it should display the following:

```js
[ "burger", "biscuit", "fries", "biscuit", "fries", "burger", "burger", "fries" ]
```

---

## LLM Prompt for Deeper Understanding

To test your understanding, copy and paste the following prompt into an LLM of your choice:

> You are a Socratic tutor assessing my knowledge of using `if/else` conditionals inside loops in JavaScript. First, ask me to explain how an `if/else` statement works. Then, ask me to describe how conditionals can be used to transform data in an array. Next, give me a short code snippet with an array of raw ingredients and ask me to predict the resulting transformed array. Finally, ask me about real-world scenarios where automating transformations like this is useful in programming.

[Back to Supplement Foundations]({{ "/books/client_book0" | relative_url }})

