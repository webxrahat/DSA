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
