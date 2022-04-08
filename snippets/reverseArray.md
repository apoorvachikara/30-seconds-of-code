---
title: Reverse Array
tags: array
expertise: intermediate
firstSeen: 2022-04-07T11:11:28+03:00
lastUpdated: 2022-04-08T20:24:30+03:00
---

Reverses an array.

- Reverses an array without an in-built reverse function.
- It will only take half the iteration i.e O(logn).
- We are using the two pointers mechanism to iterate through the array.
- On every iteration, we swap both the first and last element, decrement end pointer and increment start pointer.

```js
const reverseArray = (array) => {
    let start = 0;
    let end = array.length - 1;

    while (start < end) {
        const temp = array[start];
        array[start] = array[end];
        array[end] = temp;
        start++;
        end--;
    }
    return array;
}
```

```js
reverseArray([1, 2, 3, 4, 5]); // [5, 4, 3, 2, 1]
reverseArray([-2, -1, 0, 8, 9, 10]); // [10, 9, 8, 0, -1, -2]
```
