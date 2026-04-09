# Problems
Problem 1: Transaction Fee Sorting for Audit Compliance
Scenario: A banking application processes 10,000 daily transactions. Auditors require
transactions sorted by fee amount for compliance reviews.
Problem Statement:
Implement a fee‐sorting system that:
● Sorts transactions by fee in ascending order using Bubble Sort (for small batches
≤ 100).
● Sorts by fee + timestamp using Insertion Sort (for medium batches 100–1,000).
● Handles duplicates (stable sort required).
● Flags high‐fee outliers (> $50).
Concepts Covered:
● Bubble Sort: adjacent swaps, early termination.
● Insertion Sort: building sorted subarray, shift operations.
● Time complexity: O(n2) analysis, best/worst cases.
● Stability in sorting.
Hints:
● Use ArrayList<Transaction> with fee and timestamp.
● Bubble: nested loops, compare i and i+1, swap if needed.
● Insertion: for each element, shift larger ones right.
● Count passes/swaps for optimization.
Use Cases:
● Citi transaction audit reports.
● Fraud detection by fee patterns.
● Compliance fee threshold analysis.
Sample Input/Output:
Input transactions:
id1, fee=10.5, ts=10:00
id2, fee=25.0, ts=09:30
id3, fee=5.0, ts=10:15
BubbleSort (fees): [id3:5.0, id1:10.5, id2:25.0] // 3 passes, 2 swaps
InsertionSort (fee+ts): [id2:25.0@09:30, id3:5.0@10:15, id1:10.5@10:00]
High-fee outliers: none

