# Merge Sort

## Description

Merge Sort is an efficient, general-purpose, and comparison-based sorting algorithm. Most implementations produce a stable sort, which means that the implementation preserves the input order of equal elements in the sorted output. It is a divide and conquer algorithm that was invented by John von Neumann in 1945.

## Time Complexity

- **Best**: O(n log n)
- **Average**: O(n log n)
- **Worst**: O(n log n)

Unlike some other sorting algorithms, such as quicksort and heapsort, merge sort's worst-case time complexity is the same as its average and best-case performance.

## Space Complexity

- **Worst**: O(n) auxiliary. Merge sort requires additional space proportional to the size of the input array.

## Stability

- [X] Stable

## Pseudo Code

```plaintext
procedure mergesort(array A as list)
    if length(A) <= 1
        return A
    end if

    var middle := length(A) / 2
    var left := A[0..middle-1]
    var right := A[middle..end]

    left := mergesort(left)
    right := mergesort(right)

    return merge(left, right)
end procedure

procedure merge(array left as list, array right as list)
    var result as list

    while length(left) > 0 or length(right) > 0
        if length(left) > 0 and length(right) > 0
            if first(left) <= first(right)
                append first(left) to result
                left := rest(left)
            else
                append first(right) to result
                right := rest(right)
            end if
        else if length(left) > 0
            append first(left) to result
            left := rest(left)
        else if length(right) > 0
            append first(right) to result
            right := rest(right)
        end if
    end while

    return result
end procedure
```

## Remarks

Merge Sort is particularly good for sorting linked lists and large data sets stored on external devices. It's also well-suited for parallel processing, as the separate parts of the array can be sorted concurrently. However, its space complexity can be a disadvantage when working with large arrays on systems with limited space.
