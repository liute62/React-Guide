
# React-Guide

## 1.Fundamentals of JavaScript

 ### Types

 1. #### Primitive
```
let a = 1; const a = 1; // Number, are Always 64-bit Floating Point
let a = 'a'; const a = 'a'; // String
let a = True; const a = False; // Boolean
let a = null; const a = null; // Null
let a = undefined; const a = undefined; // undefined
```
1) undefined represents a variable that has not been assigned a value, while null   represents a deliberate non-value.
2) JavaScript uses the + operator for both addition and concatenation. If you add two numbers, the result will be a number. If you add a number and a string, the result will be a string concatenation.
3) The  `typeof`  operator returns the type of a variable or an expression.
4) In JavaScript, a variable without a value, has the value  `undefined`. The type is also  `undefined`. While an empty string has both a legal value and a type.

 2. #### Object
 ```
 // 1.Declare an object
 const myObject = { 
	 key1: 'value1', 
	 key2: 'value2', 
	 key3: function() { 
		   return  this.key1 + " " + this.key2;
     } 
 };

// 2.Assign values
myObject.key1 = 'new value'; 
console.log(myObject.key1); // Output: "new value" 
myObject['newKey'] = 'new property'; 
console.log(myObject.newKey); // Output: "new property"

// 3.If the object key is a variable
let var = 'myVar'
let varObject = {}
varObject[var] = 'value' // equals to varObject[myVar] = 'value'

// 4.Iterate keys
`Object.keys()` is a built-in method in JavaScript that returns an array containing the names of all the enumerable properties (i.e., keys) of a given object. The array is returned in the same order as the object's keys are enumerated.

const myObject = { 
	name: "John", 
	age: 30, 
	gender: "male" 
}; 
const keys = Object.keys(myObject); 
console.log(keys); // Output: ["name", "age", "gender"]
```

 3. #### Array
```
//1. forEach
// The `forEach` method does not return anything and simply iterates over the array.

const myArray = [1, 2, 3]; 
myArray.forEach(function(element, index) { 
	console.log(element); 
}); 
// Output: 1 2 3


//2. map
The `map` method returns a new array with the same number of elements as the original array, but with each element transformed by the callback function.

const myArray = [1, 2, 3]; 
const newArray = myArray.map(function(element) { 
	return element * 2; 
}); 
// Output: [2, 4, 6]


//3. filter
The `filter` method returns a new array with only the elements that passed the test.

const myArray = [1, 2, 3]; 
const newArray = myArray.filter(function(element) { 
	return element > 1; 
}); 
// Output: [2, 3]


//4. reduce
The `reduce` method returns the final value of the accumulator.

const myArray = [1, 2, 3]; 
const sum = myArray.reduce(function(accumulator, element) { 
	return accumulator + element; 
}, 0); 
// Output: 6


//5. sort
The `sort` is a method in JavaScript that is used to sort the elements in an array.

const myArray = [3, 2, 1]; 
myArray.sort(); // Output: [1, 2, 3]  
const newArray = myArray.sort(function(a, b) { 
	return b - a; 
}); 
// Output: [3, 2, 1]


//6. indexOf
The `indexOf` is a method in JavaScript that is used to find the index of the first occurrence of a specified value in an array. If the value is not found in the array, `indexOf` returns -1.

const myArray = [1, 2, 3]; 
const index = myArray.indexOf(2); // Output: 1


//7. concat
The  `concat()`  method creates a new array by merging (concatenating) existing arrays.

const myArray1 = [1, 2, 3]; 
const myArray2 = [4, 5, 6]; 
const newArray = myArray1.concat(myArray2); // Output: [1, 2, 3, 4, 5, 6]


//8. push
`push` is a method in JavaScript that is used to add one or more elements to the end of an array.

const myArray = [1, 2, 3]; 
const newLength = myArray.push(4, 5); // Output: 5  
// myArray is now [1, 2, 3, 4, 5]


//9. shift
`shift`: `shift` is a method in JavaScript that is used to remove the first element from an array and return it.

const myArray = [1, 2, 3]; 
const firstElement = myArray.shift(); // Output: 1  
// myArray is now [2, 3]

```


#### Scope
In JavaScript, scope refers to the accessibility of variables and functions within the code. Specifically, it determines where in the code a variable or function can be accessed.

There are two types of scope in JavaScript: global scope and local scope.

Variables declared with `let` or `const` have block scope, meaning they are only accessible within the block they are defined in, such as a loop or an if statement.

```
// 1.Scope by block {}
if (true) { 
  const myVariable = 'I am inside the if statement'; 
  console.log(myVariable); // Output: "I am inside the if statement" 
} 
console.log(myVariable); // Error: "myVariable is not defined"

// 2.Shadow variables
// It is generally considered a good practice to avoid using the same variable name in different scopes to prevent shadowing
const myVariable = 'global'; 
function  myFunction() { 
	const myVariable = 'local'; 
	console.log(myVariable); // Output: "local" 
} 
myFunction(); 
console.log(myVariable); // Output: "global"

```


#### Promise

Promises are often used to handle asynchronous operations, such as network requests or file I/O, where the result is not immediately available.
```
// 1.New promise
const myPromise = new Promise((resolve, reject) => { 
// Do some asynchronous operation, then call resolve() or reject() 
// if success resolve(result)
// else reject(error)
});

// 2.Resolve promise
myPromise.then(result => { // Do something with the result }) 
.catch(error => { // Handle the error })
.finally()=>{
};

// 3.Promise.all()
const promise1 = new Promise((resolve, reject) => { 
	setTimeout(() => { resolve('Promise 1'); }, 2000); 
}); 
const promise2 = new  Promise((resolve, reject) => { 
	setTimeout(() => { resolve('Promise 2'); }, 1000); 
}); 

Promise.all([promise1, promise2]).then(results => { 
  console.log(results); // Output: ["Promise 1", "Promise 2"] 
}).
catch(error => { 
 console.error(error); 
});
```

## 2.Fundamentals of React


### Class component



### Function component
