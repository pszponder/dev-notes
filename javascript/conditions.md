# If Conditionals
```js
if ( condition ) {
    // Do stuff if condition is true
};
```

# If-Else Conditionals
```js
if ( condition ) {
    // Do stuff if condition is true
} else {
    // Do something else if condition is false
};
```

# If-Else If-Else Conditionals
```js
if ( condition1 ) {
    // Do stuff if condition1 is true
} else if ( condition2 ) {
    // Do stuff if condition1 is false and if condition 2 is true
} else if ( condition3 ) {
    // Do stuff if condition1 and condition2 are false and if condition3 is true
} else {
    // If none of the above conditions evaluate to true, do stuff in this else condition instead
};
```

# Switch Statements
```js
/**
 * Differentiate between Weekday and Weekend
 * day 1 => Monday => Weekday
 * day 2 => Tuesday => Weekday
 * day 3 => Wednesday => Weekday
 * day 4 => Thursday => Weekday
 * day 5 => Friday => Weekday
 * day 6 => Saturday => Weekend
 * day 7 => Sunday => Weekend
 */

let day = prompt('What is today\'s number?');

switch (day) {
    case 6:
        text = 'It\'s the Weekend!';
        break;
    case 7:
        text = 'It\'s the Weekend!';
        break;
    default :
        text = 'It\'s a Weekday.';
}
```