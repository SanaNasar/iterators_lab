# Iterators Lab
## Functional Programming


### Description

In the iterators lab we will be continuing our exploration of iterators and building a few more useful methods. These methods will belong to an Iterators namespace, which we discussed in class. We also will try to use various testing methods to verify that our code is working. 


### Phase-1

Research the following term and summarize your findings on it two to three sentences:

* Higher-order function : 
Ans:  -> Functions that operate on other functions, either by taking them as arguments or returning them, are called 			Higher order functions.
	-> Higher-order functions allow us to abstract over actions, not just values.
	-> An example for higher-order function is JSON. 
	-> Also all the array methods like forEach, filter and map.
	-> The higher-order operation that represents the pattern of heirarchy is called 'reduce'.


Pretending we implemented the following methods, update this README with a description of each of the following and an example you've created:


* `max`:
Ans:	The Math.max() function returns the largest of zero or more numbers.
Example : Syntax:

Math.max(value1, value2, ... valueN ) ;

* `min`: 
Ans: Math.min() Function:
	Find the minimum number in the array list. 

Syntax:
	min(number1,number2,.......numbern) 

Description:
	Because min is a static method of Math, you always use it as Math.min(), rather than as a method of a Math object you created. 

* `foreach`
Ans: This function goes through each element of array and runs it through action. forEach is the higher-order function, since it works on the first-class function passed through the action parameter.

function forEach(array, action) {
  for (var i = 0; i < array.length; ++i)
    action(array[i]);
}


* `map`
Ans:	This function goes through all the elements of array, applies func to each one, and returns a new array with those transformed elements.
Here's an example of getting the squares of an array of numbers:

function square(x) {
  return x * x;
}
 
var numbers = [1, 2, 3, 4, 5];
var result = map(square, numbers);
Print.printLine(result.join(", "));
Print.display();


* `filter`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)
Ans:	This function filters out any element in array that doesn't return true for the condition.
The JavaScript Array filter method iterates over each value of an array passing it to a callback function. If the callback function returns true, the current value is then pushed into the resulting array.


* `reduce`: [note](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce)
Ans:	Javascript array reduce() method applies a function simultaneously against two values of the array (from left-to-right) as to reduce it to a single value.

Syntax:

array.reduce(callback[, initialValue]);


* `reject`: [note](http://underscorejs.org/#reject)
Ans:	This method returns all the elements for which the iterator returned false.
		The optional context parameter is what the iterator function will be bound to. If used, the this keyword inside the iterator will point to the object given by the argument.

Syntax:

	Iterator.reject([context]);

Extra Notes:
JavaScript supports many arithmetic operations as well as the following math functions (or, more precisely, methods of the Math object):

Math.abs(a)     // the absolute value of a
Math.acos(a)    // arc cosine of a
Math.asin(a)    // arc sine of a
Math.atan(a)    // arc tangent of a
Math.atan2(a,b) // arc tangent of a/b
Math.ceil(a)    // integer closest to a and not less than a
Math.cos(a)     // cosine of a
Math.exp(a)     // exponent of a (Math.E to the power a)
Math.floor(a)   // integer closest to a, not greater than a
Math.log(a)     // log of a base e
Math.max(a,b)   // the maximum of a and b
Math.min(a,b)   // the minimum of a and b
Math.pow(a,b)   // a to the power b
Math.random()   // pseudorandom number 0 to 1.
Math.round(a)   // integer closest to a.
Math.sin(a)     // sine of a
Math.sqrt(a)    // square root of a
Math.tan(a)     // tangent of a


 
### Phase-2 

* Write a test in the `test` folder for `min` and implement it in the `src/iterators.js` folder. There is a test for a `max` method already if you'd like to use that as inspiration. 

* Re-implement the `each` function we did in class, but write the spec for it first. Continue this exercise with `map` and `filter`.


### Phase-3

Implement the remaining iterator methods in the namespace.


### Phase-4

Refactor the following code using `map` to make only one call to the `map` function versus the two below.


```
var myNumbers = [ -1, 2, -3, 4, -5, 6];

var square = function(num) {
	return num * num;
};

var sqrRoot = function(num) {
	return Math.sqrt(num);
};


var sqrNumbers = map(myNumbers, square);
var absNumbers = map(sqrNumbers, sqrRoot);
```




