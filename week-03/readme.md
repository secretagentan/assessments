# Mechanical pt 1.

The following questions are all available in main.js

Solve them there as well!

# Arrays

Given the following array 

```
var list = [1, 2, 3, 4, 5];
```

Remove one from the beginning of the array and add it to the end

```
var zero = list.splice(0,1);
return zero;
list.push(zero);

```

# Objects

Create an object with key value pairs for `name` - a string, `isAlive` - a boolean, and `hobbies` an array.
Assign the object to the variable `user`

```
var user = {
    'name': 'Steve',
    'isAlive': false,
    'hobbies': ['groan', 'eat brains']
};

```

Add 'golf' to the `user`'s `hobby` array.

```
user.hobbies = "golf";

```

# Functions

Define a function `sayHello` that takes a name string and returns "Hello" plus that name and an exclamation point.
Example: 

```
sayHello('Mer') // "Hello Mer!"

```

```
var sayHello = function(name) {
    return "Hello " + name + "!";
}
sayHello('Mer');

```

Define a function `createRange` that takes `min` and `max` as parameters and returns an array with all the numbers
between min and max
Example: 

```
createRange(4, 8) // [4, 5, 6, 7, 8]
```

```
var createRange = function(min, max) {
    var range = [];
    range.push(min);
    for (var i = min; i <= (max-min).length; i++) {
        range.push(min + 1);
        return range;
    }
}
createRange(4,8);

```

# Callbacks

Given the following array...

use `.filter` to select only odd numbers
then `.map` to double each filtered number
then `.reduce` to sum the doubled numbers

```
var list = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
```

```
for (var i = 0; i < list.length; i++) {
    var selectOdd = function(x) {
    if (x % 2 === 1) {
    return list[i];
    } else {
    return false;
    }
}
};
 list.call(selectOdd);

var doubleEach = function() {
    var double = list.map(list[i] * 2)
}






```

#Scope

Create a variable in the global scope called name, then write a function called thisName, which creates another variable inside the function called name, and returns name. What do you think the output would be when you invoke the function thisName? What happens to the variable name in the global scope?

```
var name;
var thisName = function() {
    var name = 'Steve';
    return name;
}
thisName();

```

```
- Returns "Steve"

- var name would be undefined in the global scope


```
