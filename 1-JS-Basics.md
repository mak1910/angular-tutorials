# Javascript Basics

## Data types

- There is no distinction between floating point numbers and integers.

```javascript
    
    var x = 'Morgan Stanley';
    var y = 12;
    var z = 13.0;

```

- Arrays and nulls are objects. Function is a special type.

```javascript
    
    var a = null;
    var b = [1, 2, 3];
    var c = { name: 'Mridul', age: 18 };
    var d = function add(a, b) {
        return a + b;
    };

```

- Java null is similar to Javascript undefined.


```javascript
    
    var x = 12;
    var y = '12';

    console.log( x == y );
    console.log( x === y );

```
# Equality Operator

- Type checking with `===`

```javascript
    
    var x = { name: 'Mridul' };
    var y = { name: 'Mridul' };

    console.log( x == y );
    console.log( x === y );

```

- How to compare two objects then?


```javascript

    var person = {
        firstName: "John",
        lastName : "Doe",
        id       : 5566,
        fullName : function() {
            return this.firstName + " " + this.lastName;
        }
    };
    console.log( person.fullName() );

```

- x and y are objects while z is a primitive string.

```javascript

var x = new String("alpha")
var y = new String("alpha")
var z = "alpha"

console.log(x == y)
console.log(x == z)

```

# Arithmetic Operations

- Automatic rounding off
- NaN ( Not a number )
- Removal of decimal point based on language rules

```javascript
var num = ( 10 / 3 ) * 3;
var num = 100 / "Apple";
var num = 10/0
var num = 10.0
```

- Array operations

```javascript
var x = ["Red", "Blue", "Green", [1, 2, 3]];
var y = x.map(item => item.length)
var z = y.reduce((a,b) => a + b)
```

# Objects and Context

- Execution context

```javascript
var x = {
    firstName: 'Mridul',
    getFirstName: function() { return this.firstName }
}
var y = x.getFirstName

console.log( x.getFirstName() )
console.log( y() )
console.log( y.call(x) )
```

- Returning functions 


```javascript
function additionTemplate(x) {
    return function(y) {
        return x + y
    }
}

var addOne = additionTemplate(1)
var addTwo = additionTemplate(2)

addTwo(addOne(2))
```

- Variable hoisting

```javascript
function hoisting() {
    console.log(i); 
    for (var i = 0; i < 2 ; i++) {
        console.log(i); 
    }
    console.log(i); 
}
hoisting();  

```

- Scope concepts

```javascript

function naturalNumberFactory() {
    var count = 0;
    return function () {
        count++;
        return count;
    }
}

var factory1 = naturalNumberFactory();
var factory2 = naturalNumberFactory();
console.log(factory1())
console.log(factory1())
console.log(factory2())
console.log(factory2())

function naturalNumberFactory() {
    var count = 0;
    return function () {
        count++;
        return count;
    }
}

var factory1 = naturalNumberFactory();
var factory2 = naturalNumberFactory();
console.log(factory1())
console.log(factory1())
console.log(factory2())
console.log(factory2())
```




