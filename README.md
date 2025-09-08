# 🚀 JavaScript Interview Coding Questions

> **Great learning doesn’t come from shortcuts — it comes from challenging yourself. ✨**  
> That’s why when you solve coding problems, don’t just stop at the inbuilt function solution.

- 👉 **First**, try it with inbuilt functions to quickly understand the logic.
- 👉 **Then**, for real growth and mastery, give yourself the homework of solving the same problem _without_ inbuilt functions.

This way, you build both **practical efficiency** (knowing built-ins) and **deep understanding** (mastering logic step by step). 💪

> **Keep pushing your limits** — every line of code you write without shortcuts makes you a stronger programmer. 🔥

---

![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-yellow.svg)
![License](https://img.shields.io/badge/License-MIT-blue.svg)
![Maintenance](https://img.shields.io/badge/Maintained-Yes-green.svg)

A comprehensive collection of JavaScript interview questions with solutions, explanations, and multiple approaches.

---

## 📚 Table of Contents

1. [Sum Function](#1--sum-function)
2. [Maximum Number in Array](#2-write-a-javascript-program-to-find-the-maximum-number-in-an-array)
3. [Palindrome Check](#3-write-a-javascript-function-to-check-if-a-given-string-is-a-palindrome)
4. [Reverse String](#4-write-a-javascript-program-to-reverse-a-given-string)
5. [Return Even Numbers From Array](#5-write-a-javascript-function-that-takes-an-array-of-numbers-and-returns-a-new-array-with-only-the-even-numbers)
6. [Calculate Factorial](#6-write-a-javascript-program-to-calculate-the-factorial-of-a-given-number)
7. [Check Prime Number](#7-write-a-javascript-function-to-check-if-a-given-number-is-prime)
8. [Largest Element in Nested Array](#8-write-a-javascript-program-to-find-the-largest-element-in-a-nested-array)
9. [Fibonacci Sequence](#9-write-a-javascript-function-that-returns-the-fibonacci-sequence-up-to-a-given-number-of-terms)
10. [Title Case a String](#10write-a-javascript-program-to-convert-a-string-to-title-case)
11. [Sort Array of Objects by Key](#11write-a-function-that-takes-an-array-of-objects-and-a-key-and-returns-a-new-array-sorted-based-on-the-values-of-that-key)
12. [Deep Clone Object/Array](#12-implement-a-deep-clone-function-in-javascript-that-creates-a-copy-of-a-nested-object-or-array-without-any-reference-to-the-original)
13. [Recursive Factorial](#13-write-a-recursive-function-to-calculate-the-factorial-of-a-given-number)
14. [Merge Two Sorted Arrays](#14-implement-a-function-that-takes-two-sorted-arrays-and-merges-them-into-a-single-sorted-array-without-using-any-built-in-sorting-functions)
15. [Check for Anagrams](#15write-a-function-that-determines-if-two-strings-are-anagrams-of-each-other)
16. [Remove Duplicates from Array of Objects](#16-remove-the-duplicate-from-array-of-object)
17. [Remove Duplicates Without Inbuilt Functions](#17-remove-the-duplicates-from-array-without-using-inbuilt-functions)
18. [Sum of Array Elements](#18-implement-a-function-to-find-the-sum-of-all-the-numbers-in-an-array)
19. [Count Character Occurrences](#19-given-a-string-write-a-function-to-count-the-occurrences-of-each-character-in-the-string)

---

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

---

## 2. Write a JavaScript program to find the maximum number in an array.

```javascript
function MaximumNumberinArray(arr) {
    return Math.max(...arr);
}
let arr = [1, 2, 3, 4, 5, 66, 7];
console.log(MaximumNumberinArray(arr));
```

---

## 3. Write a JavaScript function to check if a given string is a palindrome.

```javascript
function checkPalindrome(str){
    return str === str.split("").reverse().join("")
}
let str="pop"
console.log(checkPalindrome(str))
```

---

## 4. Write a JavaScript program to reverse a given string.

```javascript
function reverseString(str){
    return str.split("").reverse().join("")
}
let str="Vikas"
console.log(reverseString(str))
```

---

## 5. Write a JavaScript function that takes an array of numbers and returns a new array with only the even numbers.

```javascript
function returnEven(arr){
    return arr.filter(n=>n%2===0)
}
let arr=[1,2,3,4,5,6,7,8,9,10]
console.log(returnEven(arr))
```
> **Explanation:**  
> The `.filter()` method is a built-in JavaScript function used with arrays.  
> It goes through each item in an array and keeps only the items that pass a test you define.

---

## 6. Write a JavaScript program to calculate the factorial of a given number.

**Iterative Solution:**
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

**Recursive Solution:**
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
> **Recursion:** A function that calls itself to solve a smaller part of a problem, until it reaches a base case.

---

## 7. Write a JavaScript function to check if a given number is prime.

```javascript
function isPrime(n){
    if (n<=1){
        return false
    }
    for(let i=2 ; i<=Math.sqrt(n) ; i++){
        if( n % i === 0){
            return false
        }
    }
    return true
}
let n=3
console.log(isPrime(n))
```

---

## 8. Write a JavaScript program to find the largest element in a nested array.

```javascript
function findLargest(arr){
    return Math.max(...arr.flat(Infinity))
}
let arr=[1,2,3,4,5,[6,77,90]]
console.log(findLargest(arr))
```
> **What does `arr.flat(Infinity)` do?**  
> It flattens nested arrays into a single-level array, no matter how deeply nested.

---

## 9. Write a JavaScript function that returns the Fibonacci sequence up to a given number of terms.

```javascript
function fibonacci(n){
    let sequence=[]
    if(n>=1) sequence.push(0)
    if(n>=2) sequence.push(1)
    for(let i=2;i<n;i++){
        let next=sequence[i-1]+sequence[i-2]
        sequence.push(next)
    }
    return sequence
}
console.log(fibonacci(10))
```

---

## 10. Write a JavaScript program to convert a string to title case (capitalize the first letter of each word).

```javascript
function capitalFirstLetter(str){
    return str.split(" ").map(word=>word.charAt(0).toUpperCase()+word.slice(1)).join(" ")
}
console.log(capitalFirstLetter("hello world"))
```

---

## 11. Write a function that takes an array of objects and a key, and returns a new array sorted based on the values of that key in ascending order.

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

---

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

const copy = structuredClone(original)
copy.name = "Yash"
copy.address.city = "Bhandup Mumbai"
console.log("Original", original)
console.log("Copy", copy)
```
> **Note:** `structuredClone()` is a modern deep clone utility available in most browsers and Node.js.

---

## 13. Write a recursive function to calculate the factorial of a given number.

```javascript
function factorial(n){
    if(n<=1) {
        return 1
    }
    else{
        return  n * factorial(n-1)
    }
}
console.log(factorial(5))
```

---

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

    while (j < arr2.length) {
        merged.push(arr2[j]);
        j++;
    }

    return merged;
}

const a = [1, 3, 5, 7];
const b = [2, 4, 6, 8, 10];

console.log(mergeSortedArrays(a, b)); 
```

---

## 15. Write a function that determines if two strings are anagrams of each other.

```javascript
function Anagram(str1, str2){
    return str1.split("").sort().join("") === str2.split("").sort().join("")
}
console.log(Anagram("anagram", "nagaram"))
```

---

## 16. Remove the duplicate from Array of Objects.

```javascript
let obj = [
  { id: 1, name: "Alice", email: "alice@example.com", active: true },
  { id: 1, name: "Alice", email: "alice@example.com", active: true },
  { id: 2, name: "Bob", email: "bob@example.com", active: false },
  { id: 3, name: "Charlie", email: "charlie@example.com", active: true }
];

let unique = obj.filter((value, index, self) =>
 index === self.findIndex((t) => (
     t.id === value.id && t.email === value.email
 ))
)
console.log(unique)
```

---

## 17. Remove the duplicates from array without using inbuilt functions.

```javascript
let arr = [1,2,3,4,5,5,5,5,6,6,7,7,78,0]
let uniquearr = []

for(let i=0;i<arr.length;i++){
    let isDuplicate=false
    for(let j=0;j<uniquearr.length;j++){
        if(arr[i] === uniquearr[j]){
            isDuplicate=true
            break;
        }
    }
    if(!isDuplicate){
        uniquearr.push(arr[i])
    }
}
console.log(uniquearr)

/// With inbuilt functions:
let arr2 = [1,2,3,4,5,5,5,5,6,6,7,7,78,0]
let result = [...new Set(arr2)]
console.log(result)
```

---

## 18. Implement a function to find the sum of all the numbers in an array.

```javascript
function Sum(arr){
    return arr.reduce((acc, num) => acc + num, 0)
}
console.log(Sum([1,2,3,4,5,6,7,8,9,10]))
```

---

## 19. Given a string, write a function to count the occurrences of each character in the string.

```javascript
function countCharacters(str){
    let charCount = {}
    for(let i=0;i<str.length;i++){
        let char = str[i]
        if(charCount[char]){
            charCount[char]++
        }
        else{
            charCount[char]=1
        }
    }
    return charCount
}
console.log(countCharacters("Hello world"))
```

---

## 🏁 Tips for Mastery

- **Try each question without built-ins first!**
- **Understand the logic before optimizing with ES6+ features.**
- **Practice writing comments and explanations for your code.**
- **Do mock interviews or code reviews with a friend.**

---

## 🤝 Contributions

Feel free to submit PRs with new questions, alternative solutions, or improvements!

---

## 📢 License

MIT

---

_Keep challenging yourself and happy coding!_
