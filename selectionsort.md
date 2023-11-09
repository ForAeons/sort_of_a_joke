# Selection Sort

## Description

Selection Sort is a simple and intuitive sorting algorithm. The algorithm divides the input list into two parts: a sorted sublist of items which is built up from left to right at the front (left) of the list, and a sublist of the remaining unsorted items that occupy the rest of the list. Initially, the sorted sublist is empty, and the unsorted sublist is the entire input list. The algorithm proceeds by finding the smallest (or largest, depending on the sorting order) element in the unsorted sublist, exchanging (swapping) it with the leftmost unsorted element (putting it in sorted order), and moving the sublist boundaries one element to the right.

## Time Complexity

- **Best**: O(n^2) as the algorithm always runs O(n^2) operations regardless of the input.
- **Average**: O(n^2) as the algorithm gradually selects the next-smallest element from the unsorted section.
- **Worst**: O(n^2) for the same reasons as the best and average cases.

## Space Complexity

- **Worst**: O(1) auxiliary (no additional memory space is needed besides the input array).

## Stability

- [ ] Not stable

## Pseudo Code

```plaintext
procedure selectionSort( A : array of items )
   int n = length(A)
   int minIndex
   
   for i = 0 to n - 1 inclusive do:
      /* set current element as minimum*/
      minIndex = i
      
      /* check the element to be minimum */
      for j = i+1 to n exclusive do:
         if A[j] < A[minIndex] then
            minIndex = j
         end if
      end for
      
      /* swap the minimum element with the current element*/
      if minIndex != i then
         swap A[i] with A[minIndex]
      end if
      
   end for
   
end procedure
```

## Remarks

Selection Sort is not difficult to implement and performs well on small lists. However, because it uses two nested loops, it has poor performance on larger lists compared to more advanced algorithms such as quicksort, mergesort, or heapsort. It does not adapt to the data in any way (so its runtime is always quadratic), and it is not stable (does not preserve the order of equal elements), but it does have the property of minimizing the number of swaps.
