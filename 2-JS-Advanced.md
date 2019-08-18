# Javascript Advanced

## Javascript Closure

A closure is a function defined inside another function (called the parent function), and has access to variables that are declared and defined in the parent function scope.

The closure has access to variables in three scopes:

- Variables declared in their own scope
- Variables declared in a parent function scope
- Variables declared in the global namespace

```javascript
function randomNumberGenerator() {

    function randomNumber() {
        
        // Ensure n has correct value
        console.log('Function has been called ' + n + ' times');
        return Math.random();
    }

    return randomNumber;
}
var generatorObj = randomNumberGenerator();
console.log(generatorObj());
console.log(generatorObj());
console.log(generatorObj());
```


## Event Loop

- [Animated Demo](http://latentflip.com/loupe/)

```javascript
    console.log("1")
    setTimeout(function() {
        console.log("2")
    }, 1000);
    setTimeout(function() {
        console.log("3")
    }, 0);
    console.log("4")
```

## Callback functions

- Long running operations like rest calls in a single-threaded environment.

```javascript
    
    function getUser(cb) {
        // Rest call simulation
        setTimeout(() => {
            cb({
                name : 'John Doe',
                age: 28
            });
        }, 2000);
    }

    // Write code to call getUser and print user details

```

- Applying concept of callback to print keyboard entries

```javascript
    function onKeyUp(event) {
        // Complete this function to print the character entered
    }

    window.addEventListener("keyup", onKeyUp);
```

