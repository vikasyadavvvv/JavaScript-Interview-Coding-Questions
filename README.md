# 🚀 JavaScript Interview Coding Questions

![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-yellow.svg)
![License](https://img.shields.io/badge/License-MIT-blue.svg)
![Maintenance](https://img.shields.io/badge/Maintained-Yes-green.svg)

A comprehensive collection of JavaScript interview questions with solutions, explanations, and multiple approaches.


## 1. ➕ Sum Function

### Basic Implementation
```javascript
function sum(a, b) {
    return a + b;
}

// Example Usage
const result = sum(10, 5);
console.log(result); // Output: 15
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


## 6. Write a JavaScript program to calculate the factorial of a given number. 
Solution 1
```javascript
function calculateFactorial(n){
    if(n === 0 || n === 1){
        return 1;
    }
    let result=1
    for(let i=2 ; i<=n ; i++){
        result*=i
    }
    return result 
}
let n=5
console.log(calculateFactorial(n))

```
Solution 2
```javascript
function calculateFactorial(n){
    if(n === 0 || n === 1){
        return 1;
    }
    else{
       return n*calculateFactorial(n-1)
    }
     
}
let n=5
console.log(calculateFactorial(n))
```
Recursion is when a function calls itself to solve a smaller part of a problem, until it reaches a stopping point (called the base case).

In simple words:A function that solves a big problem by repeating itself on smaller pieces of the problem.


## 7. Write a JavaScript function to check if a given number is prime. 
```javascript
function isPrime(n){
    if (n<=1){
        return false
    }
   for(let i=2 ; i<Math.sqrt(n) ; i++){
       if( n% i === 0){
           return false
       }
   }
   return true
}
let n=3
console.log(isPrime(n))
```


## 8. Write a JavaScript program to find the largest element in a nested array. 
```javascript
function findLargest(arr){
    return Math.max(...arr.flat(Infinity))
}
let arr=[1,2,3,4,5,[,6,77,90]]
console.log(findLargest(arr))
```
 What does arr.flat(Infinity) do?
In JavaScript, the .flat() method creates a new array where nested arrays are flattened (i.e., turned into a single-level array).
By default, .flat() only flattens one level deep.
If you use .flat(Infinity), it flattens the array all the way down, no matter how deeply nested the elements are.


## 9. Write a JavaScript function that returns the Fibonacci sequence up to a given number of terms. 
```javascript
function fibonacci(n){
    let sequence=[]
    if(n>=1) sequence.push(0)
    if(n>=2) sequence.push(1)
    
    for(let i=2;i<=n;i++){
        let next=sequence[i-1]+sequence[i-2]
        sequence.push(next)
    }
    return sequence
}
console.log(fibonacci(10))
```


## 10.Write a JavaScript program to convert a string to title case (capitalize the first letter of each word). 
```javascript
function capitalFirstLetter(str){
    return str.split(" ").map(word=>word.charAt(0).toUpperCase()+word.slice(1)).join(" ")
}
console.log(capitalFirstLetter("hello world"))
```


## 11.Write a function that takes an array of objects and a key, and returns a new array sorted based on the values of that key in ascending order. 
```javascript
function sortByKey(arr,key){
    return arr.slice().sort((a,b)=>{
        if(a[key]<b[key]) return -1;
        if(a[key]>b[key]) return 1;
        return 0;
    })
}
const users = [
  { name: "Vikas", age: 25 },
  { name: "Yash", age: 22 },
  { name: "Chirag", age: 27 }
];

const sortedByAge = sortByKey(users, "age");
console.log(sortedByAge);

```


## 12. Implement a deep clone function in JavaScript that creates a copy of a nested object or array without any reference to the original. 
```javascript
const original = {
  name: "Vikas",
  age: 20,
  hobbies: ["coding", "gym"],
  address: {
    city: "Mumbai",
    pin: 400070
  }
};

const copy=structuredClone(original)
copy.name="Yash"
copy.address.city="Bhandup Mumbai"
console.log("Original",original)
console.log("Copy",copy)
```


## 13. Write a recursive function to calculate the factorial of a given number. 
```javascript
function factorial(n){
    if(n<=1) {
        return 1
    }
    else{
        return  n *factorial(n-1)
    }
}
console.log(factorial(5))
```

## 14. Implement a function that takes two sorted arrays and merges them into a single sorted array without using any built-in sorting functions. 
```javascript
function mergeSortedArrays(arr1, arr2) {
    let merged = [];
    let i = 0;
    let j = 0;

    while (i < arr1.length && j < arr2.length) {
        if (arr1[i] < arr2[j]) {
            merged.push(arr1[i]);
            i++;
        } else {
            merged.push(arr2[j]);
            j++;
        }
    }

    while (i < arr1.length) {
        merged.push(arr1[i]);
        i++;
    }

    while (j < arr2.length) { // Fixed: changed i to j
        merged.push(arr2[j]);
        j++;
    }

    return merged;
}

const a = [1, 3, 5, 7];
const b = [2, 4, 6, 8, 10];

console.log(mergeSortedArrays(a, b)); 

```

## 15.Write a function that determines if two strings are anagrams of each other
```javascript
function Anagram(str1,str2){
    return str1.split("").sort().join("") === str2.split("").sort().join("")
}
console.log(Anagram("anagram","nagaram"))
```

## 16. Remove the duplicate from Array of Object
```javascript
let obj = [
  { id: 1, name: "Alice", email: "alice@example.com", active: true },
  { id: 1, name: "Alice", email: "alice@example.com", active: true },
  { id: 2, name: "Bob", email: "bob@example.com", active: false },
  { id: 3, name: "Charlie", email: "charlie@example.com", active: true }
];

let unique=obj.filter((value,index,self)=>
 index === self.findIndex((t)=>(
     t.id === value.id && t.email === value.email
     ))
)
console.log(unique)
```






