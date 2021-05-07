# Number
```js
let myFavoriteNumber = 10;
```


# Float
```js
let pi = 3.1415;
```


# String
```js
let name = "Bob";
```
## Common String Methods
```js
let continent = 'Antartica';

// Create a new line within a string
// The \n will create a new line charachter and the "new line" string will appear on a seperate line
'this is a \n new line'

// Print length of string
continent.length

// Find the index of the first occurance of specified value
continent.indexOf('ar')

// Return a section of the string based on the specified indicies
continent.slice(3, 5)

// Convert string to all uppercase
continent.toUpperCase()

// Convert string to all lowercase
continent.toLowerCase()

// Return the value of the string at the specified index
continent[5]

// Split a string based on a delimeter and return the seperated values in an array
continent.split('')   // Split by charachter
continent.split(' ')  // Split by space
continent.split(',')  // Split by comma

```


# Boolean
```js
let a = true;
let b = false;
```


# Array
```js
let favorites = ['bananna', 9, true, 5.89]
```

## Ways to Define an Array
```js
let dessert = ['Pie', 'Ice Cream', 'Cake', 'Cookie'];
let dessert = new Array('Pie', 'Ice Cream', 'Cake', 'Cookie');
```

## Access an Element from an Array at a Specified Index
```js
let dessert = ['Pie', 'Ice Cream', 'Cake', 'Cookie'];

dessert[2];  // returns 'Cake'
```

## Change an Element in an Array at a Specified Index
```js
let dessert = ['Pie', 'Ice Cream', 'Cake', 'Cookie'];

dessert[2] = 'Yogurt'; // Returns ['Pie', 'Ice Cream', 'Yogurt', 'Cookie'];
```

## Use an Array in a for loop to iterate over the values in the array
```js
let dessert = ['Pie', 'Ice Cream', 'Cake', 'Cookie'];

for (let i = 0; i < dessert.length; i++) {
    console.log(dessert[i]);
}
```

## Common Array Methods
```js
let dessert = ['Pie', 'Ice Cream', 'Cake', 'Cookie'];

// Convert an array into a string
dessert.toString(); // returns 'PieIceCreamCakeCookie'

// Join the values of an array using a charachter(s) and return the string
dessert.join('-'); // returns 'Pie-IceCream-Cake-Cookie'

// Remove the last item in the array and return the removed item
dessert.pop(); // returns 'Cookie'

// Append an item to the end of the array
dessert.push('Jello');
dessert[dessert.length] = 'Jello';

// Add to an array using a for loop
let myArray = [];
for (let i = 0; i < 5; i++) {
    myArray[i] = i;
}

// Combine Arrays
let moreDessert = ['Watermelon', 'Pudding', 'Chocolate'];
dessert.concat(moreDessert);

// Slice Arrays
dessert.slice[2:4];

// Reverse Arrays
dessert.reverse();

// Sort Arrays
dessert.sort();

// Sort In Ascending Order
let numbers = [5, 3, 2, 4, 1, 0];
numbers.sort(function(a, b) {return a-b});

// Sort in Descending Order
let numbers = [5, 3, 2, 4, 1, 0];
numbers.sort(function(a, b) {return b-a});
```


# Object
```js
let dog = {name: 'Spot', legs: 4, bark: true};
```

```js
let name = {
    first: 'John',
    last: 'Doe',
    age: 45,
    height: 180,
    info: function (){
        return this.first + '\n' + this.last;
    }
};

// Access the value of a key in an Object
name.first    // evaluates to 'John'
name['first'] // evaluates to 'John'

name.last    // evaluates to 'Doe'
name['last'] // evaluates to 'Doe'

// Change value in the Object
name.first = 'Bob';  // Changes the value of first from 'John' to 'Bob

// Run a method from the object
name.info();

```


# Undefined
```js
let something;
```


# Null
```js
let zilch = null;
```