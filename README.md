# What I Learned in Week 10

## Week 10 taught me about responsive layouts, Bootstrap, objects, and the array methods `.map()` and `.filter()`.

### `@media` Queries

Responsive design allows for the layout of a web page to change based on properties of the display window.  The width and height of the window determine which css properties apply.  In the example below, a window that is sized below 700px wide has its `div` backgrounds turn red, while anything wider becomes blue:
```
@media all and (max-width: 700px) {
	div {
		background-color: red;
	}
}

@media all and (min-width: 700px) {
	div {
		background-color: blue;
	}
}
```

### Bootstrap

Bootstrap is a stylesheet library that provides a whole bunch of prefabricated styles for various elements of a web page.  This includes popup boxes, progress bars, different kinds of buttons and forms, etc.

### `Array.map()`

This array method returns a modified version of the original array.  `map()` is provided with a function identifier, which gets called for each element in the array, and the return value of the function is mapped to that element's spot in the resulting array.  The example below multiplies each element of an array by 5:

```
const myArray = [1, 2, 3, 4, 5];
myArray.map(entry => entry * 5); // [5, 10, 15, 20, 25]
```

### `Array.filter()`

This array method returns a new array with certain elements filtered out.  The syntax is the same as `.map()`, the argument being a function.  If the function returns `true`, the element makes it into the resulting array.  The example below filters out odd numbers and results in an array with only even numbers:

```
const myArray = [1, 2, 3, 4, 5];
myArray.filter(entry => entry % 2 == 0); // [2, 4];