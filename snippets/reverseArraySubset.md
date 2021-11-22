---
title: reverseArraySubset
tags: array,beginner
firstSeen: 2021-11-22T13:39:02
---

Reverses a subset of an array in-place

- Takes an array, start index and end index
- Reverses the array in place
- Returns the array with subset reversed

```js
const reverseArraySubset = (arr, start, end) => {
  const arraySize = arr.length;
  let startIndex = Math.max(0, start) || 0;
  let endIndex = Math.min(arraySize - 1, end) || arraySize - 1;
  while (startIndex < endIndex) {
    [arr[startIndex], arr[endIndex]] = [arr[endIndex], arr[startIndex]];
    startIndex++;
    endIndex--;
  }
  return arr;
};
```

```js
reverseArraySubset([1, 2, 3, 4, 5], 1, 4); // [1, 5, 4, 3, 2]
```
