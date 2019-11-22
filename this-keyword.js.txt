
// this - refers to an object that is set at the creation of the 
// new execution context (function invocation)
const person = {
  name: 'Chiku',
  greet: function () { console.log('Hello, ' + this.name)},
}

person.greet () // 'Hello, Chiku'
const greet = person.greet
greet() // 'Hello, '

const xyz = {
  name: 'ABCD',
}

xyz.greet = person.greet

xyz.greet() // 'Hello, ABCD'