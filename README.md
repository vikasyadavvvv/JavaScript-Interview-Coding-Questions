# JavaScript-Interview-Coding-Questions

## 1. Write a JavaScript function to calculate the sum of two numbers.

```javascript
function Sum(a, b) {
    return a + b;
}
let result = Sum(10, 5);
console.log(result);
```

## 2. Write a JavaScript program to find the maximum number in an array.

```javascript
function MaximumNumberinArray(arr) {
    return Math.max(...arr);
}
let arr = [1, 2, 3, 4, 5, 66, 7];
console.log(MaximumNumberinArray(arr));
```

## 3. Write a JavaScript function to check if a given string is a palindrome (reads the same forwards and backwards). 
```javascript
function checkPalindrome(str){
    return str === str.split("").reverse().join("")
}
let str="pop"
console.log(checkPalindrome(str))
```

## 4. Write a JavaScript program to reverse a given string. 
```javascript
function reverseString(str){
    return str.split("").reverse().join("")
}
let str="Vikas"
console.log(reverseString(str))
```

## 5. Write a JavaScript function that takes an array of numbers and returns a new array with only the even numbers. 
```javascript
function returnEven(arr){
    return arr.filter(n=>n%2===0)
}
let arr=[1,2,3,4,5,6,7,8,9,10]
console.log(returnEven(arr))
```
The .filter() method is a built-in JavaScript function used with arrays.

It goes through each item in an array and keeps only the items that pass a test you define.
The result is a new array containing only those items.
In simple words:.filter() helps you pick out the elements you want from an array, based on a condition.


