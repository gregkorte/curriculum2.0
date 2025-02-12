## Array Methods

The [.map()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map), 
[.filter()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter), and [.find()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/find) are special tools called array methods. 
With practice you can accomplish lot of the same things you learnbed how to do with loops. Each array method map, filer, find (there are many other)  serve special purpose.

When you use .map(), .filter(), or .find(), you pass a 
function as an argument. The passed function has one argument representing the element 
being iterated over.

## Special purposes of each array method 
- The `.map()` changes/transforms every item in the array based on what the function tells it to do.
- The `.filter()` keeps only the items that pass the function’s test.
- The `.find()` looks for the first item that matches the function’s condition and returns it.

### Let's examine each array method in more detail

#### .map()
```js
[🌳, 🏖️, 🧵, 🏺].map(manufacture) => [📄, 🥂, 👕, ☕️]
```
The .map functions is called on an array with items (tree, sand, cotton, clay)
It returns a new array with equal number of transformed items (paper, glass, t-shirt, mug)
`manufacture` is a function that converts a raw material into product.

#### .filter()
```js
[📄, 🥂, 👕, ☕️].filter(isFragile) => [🥂, ☕️]
```
The .filter functions is called on an array with items (paper, glass, t-shirt, mug)
It returns a new array with equal or fewer number of elements.
`isFragile` is the function that returns true or false and decides which items to keep.

#### .find()
```js
[📄, 🥂, 👕, ☕️].find(findDrinkWare) => 🥂
```
The .find functions is called on an array with items (paper, glass, t-shirt, mug)
It returns the first found element or `undefined` if not found.

`findDrinkWare` is the function that returns true or false and determine which item is drinkware.
(Notice there is 2 drinkware glass and mug but only the first "glass" is returned)


### Chaining
Array methods that return new arrays (.map, .filter) can be `chained` together to combine into more complicated operations:

For example we may choose to manufacture the raw materials into products then filter down to fragile items then find our drinkware all in one step: 

```js
[🌳, 🏖️, 🧵, 🏺]
    .map(manufacture)
    .filter(isFragile)
    .find(findDrinkWare) => 🥂
```

## Your turn with .map()

**Please implement the `manufacture` function so that you see `Test Passed ✅` instead of `Test Failed ❌`. Only modify the function where it says 'TODO: your code here!!!'** 
<script async src="//jsfiddle.net/gczipr/ez6ytfqb/11/embed/js,result/dark/"></script>

## Your turn with .filter()

**Please implement the `isFragile` function so that you see `Test Passed ✅` instead of `Test Failed ❌`. Only modify the function where it says 'TODO: your code here!!!'** 
<script async src="//jsfiddle.net/gczipr/sqahvkuf/5/embed/js,result/dark/"></script>

## Your turn with .find()

**Please implement the `findDrinkWare` function so that you see `Test Passed ✅` instead of `Test Failed ❌`. Only modify the function where it says 'TODO: your code here!!!'** 
<script async src="//jsfiddle.net/gczipr/sqahvkuf/7/embed/js,result/dark/"></script>