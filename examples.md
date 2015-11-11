# Examples

## Arrays

// Your code here...
// `Array.some()`, `Array.every()`, `Array.filter()`, `Array.map()`

## Ternary operator

```js
var age = 25
var allowed = age > 18 ? 'Yes' : 'No' // yes

// you can nest ternary operators
var ageGroup = age > 41 ? 'Over 41' : 
  age > 31 ? 'Over 31' : 
  age > 21 ? 'Over 21' : 
  age > 18 ? 'Over 18' :
  'Underaged'
```

## Alternative to try...catch

```js
// if this evaluates to true it returns o.getName() (the right hand side)
// if this evaluates to false it returns o (the left hand side)
var name = o && o.getName()
```

## Use forEach() instead of `for loops`

```js
var a = [1, 2, 3, 4, 5]

// for loop
for (var i = 0; i < a.length; i++) {
  console.log(i)
}

// forEach() in ECMAScript 5
a.forEach(function(number){
  console.log(number)
})

// forEach() in ECMAScript 6
a.forEach(number => console.log(number))
```

## DOM examples

```js
var img = document.querySelector('img')
img.src = 'img/pic.png'

var footer = document.querySelector('footer')
var div = document.createElement('div') // <div></div>
div.textContent = 'I am awesome' // <div>I am awesome</div>

/* Use .textContent instead .innerHTML */

var people = ['Alice', 'Bob', 'Charlie']
people.forEach( function (name) {
  var element = document.createElement('h1') // <h1></h1>
  element.textContent = name // <h1>Alice</h1>
  document.querySelector('header').appendChild(element)
})

// document.querySelectorAll returns a nodelist
// Array.from() turns the nodelist into an Array object
// then we chain .filter() and .forEach()

Array.from(document.querySelectorAll('header h1'))
.filter(element => element.id !== 'title')
.forEach(element => element.remove())

function myQuerySelectorAll (selector) {
  Array.from(document.querySelectorAll(selector))
}

myQuerySelectorAll('img') // get all image elements that are returned as an Array object

```
