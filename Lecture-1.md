# Lecture 1

## HTML

- Hyper Text Markup Language 
- Can only use tags that the browser supports
- XML like syntax

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset='utf-8'>
  <meta http-equiv='X-UA-Compatible' content='IE=edge'>
  <meta name='viewport' content='width=device-width, initial-scale=1'>
  <title>ToDo App</title>
</head>
<body>
  <!-- Heading -->
  <h1 class="heading" style="color: yellow;"> ToDo List</h1>
  <!-- Paragraph -->
  <p> My list of todo items</p>
  <!-- Unordered List -->
  <ul>
    <li> Item 1 </li>
    <li> Item 2 </li>
  </ul>
</body>
</html>
```
- Browser usually renders static html. Two options for this : 
  - Server side rendering ( eg. Django, Express )
  - Front end rendering ( eg. Angular, React )
- Further reading <https://www.w3schools.com/html/>

## CSS

- Cascading Style Sheets
- Select html on the basis of tags or class or id
- Cascading effect

```html
<!DOCTYPE html>
<html>
<head>
  <style>
    p {
      color: red;
    }
    .heading {
      color: blue;
    }
  </style>
</head>
<body>
  <p class="heading" style="color: green;"> Heading paragraph </p>
</body>
</html>
```
- Further reading <https://www.w3schools.com/css/>

## Rest Service

- GET, PUT, POST, DELETE
- HTTP protocol
- URI and Schema

Calling a Function 
1. Function reference
2. Input parameters & return type

Rest Call
1. Reference : url eg. http://abc.com/getUserName 
2. Input Schema/Output Schema ( Usually JSON )

- Further reading : <https://www.geeksforgeeks.org/rest-api-introduction/>


## Javascript

- Programming language of the web.
- Started out with need to make dynamic rest calls and animations.
- Interoperability with JSON 
- Today used everywhere from backend to web to native applications
- Asynchronus nature of Javascript and the event loop
- Single threaded by default and in most use cases

```javascript
console.log(1)
setTimeout(function() { console.log(2) }, 1000)
console.log(3)
```
```javascript
console.log(1)
setTimeout(function() { console.log(2) }, 1000)
setTimeout(function() { console.log(3) }, 1000)
```
```javascript
console.log(1)
setTimeout(function() { console.log(2) }, 0)
setTimeout(function() { console.log(3) }, 1000)
console.log(4)
```
- Further reading : <https://www.w3schools.com/js/>
- Video on event loop : <https://www.youtube.com/watch?v=8aGhZQkoFbQ&t=810s>