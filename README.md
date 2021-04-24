# insert-sort
First implementation of insertion sort--from conceptual description.

```javascript
function insertionSort (arr) {
  for(let currIndex=1; currIndex < arr.length;){
    loopBack(arr[currIndex], currIndex++, arr)
  }
  return arr
}

function loopBack(currItem, currIndex, arr){
  // Loop backwards through arr starting at currIndex
  // shifts currItem right if > item. Item lands at
  // currIndex when currItem <= item, no shift occurs.
  let prevIndex = currIndex - 1;
  for(prevIndex; prevIndex >= -1;){
    let prevItem = arr[prevIndex--];
    if(prevItem > currItem) arr[currIndex--] = prevItem;
    else return (arr[currIndex] = currItem)
  }
}

unsortedArray = [
  21, 18,  8,  3,  2,  2, 24, 22, 38, 20,
  38, 19,  3, 31, 34, 12, 27,  7, 22, 11,
  29, 19, 16,  2,  4, 23, 12, 19, 24, 22,
  25, 30, 30, 29, 33, 31,  3,  2, 33, 33
];

/*

[
   2,  2,  2,  2,  3,  3,  3,  4,  7,  8,
  11, 12, 12, 16, 18, 19, 19, 19, 20, 21,
  22, 22, 22, 23, 24, 24, 25, 27, 29, 29,
  30, 30, 31, 31, 33, 33, 33, 34, 38, 38
]

*/

```
