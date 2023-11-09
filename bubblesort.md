# Bubble Sort

## Description

Bubble Sort is a simple comparison-based algorithm in which each pair of adjacent elements is compared and the elements are swapped if they are not in order. This process is repeated until no swaps are needed, which indicates that the list is sorted. It is named for the way smaller elements "bubble" to the top of the list.

## Time Complexity

- **Best**: O(n) when the list is already sorted.
- **Average**: O(n^2) when the elements are in random order.
- **Worst**: O(n^2) when the list is in reverse order.

## Space Complexity

- **Worst**: O(1) auxiliary (no additional memory space is required aside from the input array).

## Stability

- [X] Stable

## Pseudo Code

```plaintext
procedure bubbleSort( A : list of sortable items )
    n := length(A)
    repeat
        swapped := false
        for i := 1 to n-1 inclusive do
            /* if this pair is out of order */
            if A[i-1] > A[i] then
                /* swap them and remember something changed */
                swap( A[i-1], A[i] )
                swapped := true
            end if
        end for
        /* If no elements were swapped, then the list is sorted */
    until not swapped
end procedure
```

## Remarks

Bubble Sort is among the most intuitive sorting algorithms to understand and implement but is inefficient for large datasets. It is useful for educational purposes to demonstrate basic sorting mechanics but is outperformed by more advanced algorithms like Quick Sort or Merge Sort in practical applications.
