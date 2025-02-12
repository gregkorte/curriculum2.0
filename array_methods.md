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

Please implement `manufacture` 
```js
function manufacture(item) {
    //TODO your code here!!!
}

// Test - Do not change any code starting here
const rawMaterials = ['🌳', '🏖️', '🧵', '🏺'];
const expectedProducts = ['📄', '🥂', '👕', '☕️'];

const result = rawMaterials.map(manufacture);

expect(result).toEqual(expectedProducts); 
// Test - Do not change any code end here
```

## Your turn with .filter()

Please implement `isFragile`

```js
function isFragile(item) {
    //TODO your code here!!!
}

// Test - Do not change any code starting here
const items = ['📄', '🥂', '👕', '☕️'];
const result = items.filter(isFragile);
expect(result).toBe(['🥂', '☕️']);
// Test - Do not change any code ending here
```

## Your turn with .find()

Please implement `findDrinkWare`

```js
function findDrinkWare(item) {
  //TODO your code here!!!
}

// Test - Do not change any code starting here
const items = ['📄', '🥂', '👕', '☕️'];
const result = items.find(findDrinkWare);
expect(result).toBe('🥂');
// Test - Do not change any code ending here
```

<script async src="//jsfiddle.net/gczipr/9wmgb8vn/1/embed/js,result/dark/"></script>