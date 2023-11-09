# Quick Sort

## Description

Quick Sort is a highly efficient sorting algorithm and is based on partitioning of an array of data into smaller arrays. A large array is partitioned into two arrays, one of which holds values smaller than the specified value, called pivot, based on which the partition is made and another array holds values greater than the pivot value.

Quick Sort partitions an array and then calls itself recursively twice to sort the two resulting subarrays. This algorithm is quite efficient for large-sized data sets and is one of the fastest sorting methods in practice.

## Time Complexity

- **Best**: O(n log n) when the partitions are evenly balanced.
- **Average**: O(n log n)
- **Worst**: O(n^2) when the partition process always picks the greatest or smallest element as the pivot.

However, with good pivot selection methods, this worst-case scenario is rare.

## Space Complexity

- **Worst**: O(log n) auxiliary (naive) to O(n) auxiliary (Sedgewick 1978). The space complexity of quicksort is dependent on the version used - the in-place version has a space complexity of O(log n) due to the stack space taken up by recursion.

## Stability

- [X] Stable

## Pseudo Code

```plaintext
procedure quickSort(A, low, high)
    if low < high then
        pi := partition(A, low, high)
        quickSort(A, low, pi - 1)  // Before pi
        quickSort(A, pi + 1, high) // After pi
    end if
end procedure

procedure partition(A, low, high)
    // pivot (Element to be placed at right position)
    pivot := A[high]  

    i := (low - 1)  // Index of smaller element

    for j := low to high - 1 do
        // If current element is smaller than or equal to pivot
        if A[j] <= pivot then
            i := i + 1
            swap A[i] with A[j]
        end if
    end for

    swap A[i + 1] with A[high])
    return (i + 1)
end procedure
```

## Remarks

Quick Sort is generally considered to be very efficient and fast. However, it is not a stable sort; the relative order of equal sort items is not preserved. It is also not naturally a stable sort, meaning that the same element in an array could be placed in any equal element's position. Moreover, careful attention must be paid to the choice of pivot to avoid poor performance, and its recursive nature can lead to stack overflow errors on very large arrays if not implemented with tail recursion or other mitigations.
