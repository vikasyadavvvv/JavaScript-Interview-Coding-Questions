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
