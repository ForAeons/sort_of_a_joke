# Heap Sort

## Description

Heap Sort is a popular and efficient comparison-based sorting algorithm. Heapsort can be thought of as an improved selection sort: like selection sort, heapsort divides its input into a sorted and an unsorted region, and it iteratively shrinks the unsorted region by extracting the largest element from it and inserting it into the sorted region. Unlike selection sort, heapsort does not waste time with a linear-time scan of the unsorted region; rather, heap sort maintains the unsorted region in a heap data structure to more quickly find the largest element in each step.

## Time Complexity

- **Best**: O(n log n) 
- **Average**: O(n log n)
- **Worst**: O(n log n)

The time complexity of heapsort is O(n log n) for all cases which makes it very predictable in terms of performance.

## Space Complexity

- **Worst**: O(1) auxiliary

Heapsort is an in-place algorithm, but it is not a stable sort.

## Stability

- Not stable

Heap Sort is typically not stable because operations on the heap can change the relative order of equal elements.

## Pseudo Code

```plaintext
procedure heapify(A, count)
    start := floor((count - 2) / 2)
    
    while start >= 0 do
        siftDown(A, start, count - 1)
        start := start - 1
    end while
end procedure

procedure siftDown(A, start, end)
    root := start

    while (root * 2 + 1) <= end do
        child := root * 2 + 1
        swap := root
        
        if A[swap] < A[child] then
            swap := child
        end if
        if child+1 <= end and A[swap] < A[child+1] then
            swap := child + 1
        end if
        if swap = root then
            return
        else
            exchange A[root] with A[swap]
            root := swap
        end if
    end while
end procedure

procedure heapsort(A, count)
    heapify(A, count)
    
    end := count - 1
    while end > 0 do
        exchange A[end] with A[0]
        end := end - 1
        siftDown(A, 0, end)
    end while
end procedure
```

## Remarks

Heap Sort is particularly useful for data that is already stored in a random access data structure. The sort is not stable, which means that the relative order of equal sort items is not preserved. It is, however, particularly memory-efficient, as it sorts in place and requires no additional memory allocation.
