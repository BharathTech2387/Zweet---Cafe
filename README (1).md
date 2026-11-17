# Experiment No. 1 — Interpolation Search

**Subject:** CS5303 – Design and Analysis of Algorithms
**Programme:** B.E. Computer Science and Engineering

## Problem Statement
Given a sorted array of uniformly distributed integers, implement Interpolation
Search to find the position of a target element. Compare its performance with
Binary Search for different dataset sizes (1000, 5000, 10000, 50000, 100000 elements).

## Aim
To implement the Interpolation Search algorithm in Python and analyze its time
complexity by measuring execution time on sorted datasets of varying sizes.

## Files
| File | Description |
|------|-------------|
| `interpolation_search.py` | Full Python implementation with performance analysis |
| `index.html` | Visual report of pseudocode, program, and sample output |
| `README.md` | This file |

## How to Run
```bash
python interpolation_search.py
```

## Algorithm Overview
Interpolation Search improves on Binary Search by estimating the probable
position of the target using the formula:

```
pos = low + ((target - arr[low]) * (high - low)) / (arr[high] - arr[low])
```

- **Time Complexity:** O(log log n) average (uniform data), O(n) worst case
- **Space Complexity:** O(1)

## Sample Output
```
Array: [2, 5, 10, 15, 23, 35, 48, 60, 75, 90, 105, 120]
Searching for: 35
Found at index: 5, Comparisons: 2

      Size   IS Time(ms)   BS Time(ms) IS Comparisons BS Comparisons
---------------------------------------------------------------------------
      1000        0.0021        0.0035                3               10
      5000        0.0025        0.0042                3               13
     10000        0.0028        0.0048                4               14
     50000        0.0031        0.0061                4               16
    100000        0.0035        0.0068                5               17
```

## Result
The Interpolation Search algorithm was successfully implemented. It found the
target element at index 5 with only 2 comparisons. Performance analysis shows
that Interpolation Search consistently requires fewer comparisons (O(log log n))
compared to Binary Search (O(log n)) for uniformly distributed sorted data.

## Inference
Interpolation Search outperforms Binary Search when data is uniformly
distributed, achieving near O(log log n) complexity. It is highly efficient for
large, uniformly spaced datasets but degrades to O(n) for skewed distributions.
For real-world applications with uniform data (e.g., phone books), Interpolation
Search is the preferred algorithm.

## Practice Problems
1. Implement Interpolation Search on a sorted array of student roll numbers
   (range 1 to 10000) and count the number of probes required to find a given
   roll number. Compare results with Binary Search.
2. Modify Interpolation Search to work on a sorted array of floating-point
   numbers (uniformly distributed between 0.0 and 1000.0) and analyze how many
   comparisons are needed for different dataset sizes (10000, 50000, 100000).
