# Common complexities

- O(1) constant
- O(n) Linear/Linear search
- O(n2) Quadratic
- O(log n) Binary search
- O(n log n) Sorting
- O(2n) Exponential reccursion

<hr style="border: 1px solid black;">

1. O(1) — Constant Time

### Meaning

- Time does NOT change with input size
- Whether input has 1 item or 1 million, it runs the same time

### Example

```
function getFirst(arr) {
  return arr[0];
}
```

### Why O(1)?

- Always 1 operation
- No loops
- No conditions depending on size

<hr style="border: 1px solid black;">

2. O(n) — Linear Time

### Meaning

- Time grows linearly with input size
- If input doubles → work doubles

### Example (Linear Search)

```
function linearSearch(arr, target) {
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] === target) return i;
  }
  return -1;
}
```

### Why O(n)?

- Worst case: check every element
- n elements → n steps

### Real life example

- Searching a name in an unsorted list
- Finding a word in a paragraph

### Remember

- “One loop = O(n)”

<hr style="border: 1px solid black;">

3. O(n²) — Quadratic Time

### Meaning

- For every element, you loop over all elements again
- Very slow for large inputs

### Example

```
function printPairs(arr) {
  for (let i = 0; i < arr.length; i++) {
    for (let j = 0; j < arr.length; j++) {
      console.log(arr[i], arr[j]);
    }
  }
}
```

### Why O(n²)?

- First loop → n
- Second loop → n
- Total → n \* n

### Real life example

- Comparing every student with every other student
- Bubble Sort, Selection Sort

### Remember

- “Nested loops = O(n²)”

<hr style="border: 1px solid black;">

4. O(log n) — Logarithmic Time

### Meaning

- You cut the problem in half each step
- Very fast

### Example (Binary Search)

```
function binarySearch(arr, target) {
  let left = 0;
  let right = arr.length - 1;

  while (left <= right) {
    let mid = Math.floor((left + right) / 2);

    if (arr[mid] === target) return mid;
    else if (arr[mid] < target) left = mid + 1;
    else right = mid - 1;
  }

  return -1;
}
```

### Why O(log n)?

- Every step removes half the data
- 16 → 8 → 4 → 2 → 1

### Real life example

- Guessing a number by saying “higher or lower”
- Dictionary search

### Remember

- “Divide by 2 = O(log n)”

<hr style="border: 1px solid black;">

5. O(n log n) — Linearithmic Time

### Meaning

- Combination of divide & process
- Best possible for comparison sorting

### Example (Merge Sort concept)

```
function mergeSort(arr) {
  if (arr.length <= 1) return arr;

  const mid = Math.floor(arr.length / 2);
  const left = mergeSort(arr.slice(0, mid));
  const right = mergeSort(arr.slice(mid));

  return merge(left, right);
}
```

### Why O(n log n)?

- log n → splitting
- n → merging all elements

### Real life example

- Efficient sorting
- Database sorting large records

### Remember

- “Best sorting time = O(n log n)”

<hr style="border: 1px solid black;">

6. O(2ⁿ) — Exponential Time

### Meaning

- Each step doubles the work
- Extremely slow

### Example (Recursive Fibonacci)

```
function fib(n) {
  if (n <= 1) return n;
  return fib(n - 1) + fib(n - 2);
}
```

### Why O(2ⁿ)?

- Each function call creates 2 more calls
- Grows explosively

### Real life example

- Brute-force password cracking
- Subset problems

### Remember

- “Recursive branching = O(2ⁿ)”

<hr style="border: 1px solid black;">

## Big-O Comparison (Important!)

```
Fastest
O(1)
O(log n)
O(n)
O(n log n)
O(n²)
O(2ⁿ)
Slowest
```

### Interview Tip (Very Important)

- “What is the time complexity?”
- Worst case
- Then explain briefly why

###

- “Binary search is O(log n) because we divide the array by half each time.”
