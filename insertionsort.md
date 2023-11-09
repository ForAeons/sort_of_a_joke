# Insertion Sort

## Description

Insertion Sort is a simple and efficient comparison-based sorting algorithm. It builds the final sorted array (or list) one item at a time. It is much less efficient on large lists than more advanced algorithms such as quicksort, heapsort, or merge sort; however, it has several advantages such as simple implementation, efficient for (quite) small data sets, more efficient in practice than most other simple quadratic algorithms such as selection sort or bubble sort, and is stable.

## Time Complexity

- **Best**: O(n) when each element is at most one position away from its target position.
- **Average**: O(n^2) when elements are in random order.
- **Worst**: O(n^2) when the list is in reverse order.

## Space Complexity

- **Worst**: O(1) auxiliary (only a constant amount of additional memory space is required).

## Pseudo Code

```plaintext
procedure insertionSort( A : array of items )
   int holePosition
   int valueToInsert
   
   for i = 1 to length(A) inclusive do:
   
     /* select value to be inserted */
     valueToInsert = A[i]
     holePosition = i
      
     /*locate hole position for the element to be inserted */
     
     while holePosition > 0 and A[holePosition-1] > valueToInsert do:
       A[holePosition] = A[holePosition-1]
       holePosition = holePosition -1
     end while
     
     /* insert the number at hole position */
     A[holePosition] = valueToInsert
     
   end for
   
end procedure
```

## Remarks

Insertion sort is often used when the array is nearly sorted or when the dataset is small. Due to its simplicity, it can be faster than more complicated algorithms in certain scenarios. It is also a stable sort, meaning that the order of equal elements is preserved, and a in-place sort (it only requires a constant amount O(1) of additional memory space), making it efficient in terms of space complexity.
