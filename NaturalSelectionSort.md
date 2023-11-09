# Natural Selection Sort

## Description

Natural Selection Sort is a conceptual sorting algorithm that mimics the process of natural selection. The algorithm generates a set of duplicate arrays with slight variations—in this case, swapped pairs of elements. It then evaluates the "fitness" of each array by counting the number of correctly ordered consecutive element pairs. The array with the highest fitness is selected, and the process is repeated until an array is found to be sorted.

## Time Complexity

- **Best**: Undefined, as the algorithm relies on a stochastic process.
- **Average**: Undefined, for the same reason.
- **Worst**: Undefined, since it could, in theory, take an infinite amount of time.

The time complexity cannot be easily defined due to the algorithm's reliance on random successful mutations for progress.

## Space Complexity

- **Worst**: O(n^2), as it could potentially store numerous duplicate arrays before a sorted one is achieved.

## Stability

- Not stable

## Pseudo Code

```plaintext
procedure naturalSelectionSort(A : array of items)
    while isNotSorted(A) do
        let duplicates := generateDuplicates(A, n)
        for each duplicate in duplicates do
            swapRandomPair(duplicate)
        end for
        A := selectFittest(duplicates)
    end while
    return A
end procedure

procedure generateDuplicates(A, n)
    let duplicates := an empty list
    while size of duplicates < n do
        append a copy of A to duplicates
    end while
    return duplicates
end procedure

procedure swapRandomPair(A)
    let i, j := two random indices in A
    swap A[i] with A[j]
end procedure

procedure selectFittest(duplicates)
    let fittest := first item in duplicates
    for each duplicate in duplicates do
        if fitness(duplicate) > fitness(fittest) then
            fittest := duplicate
        end if
    end for
    return fittest
end procedure

function fitness(A)
    let score := 0
    for i := 0 to length(A) - 2 do
        if A[i] <= A[i + 1] then
            increment score
        end if
    end for
    return score
end function

function isNotSorted(A)
    for i := 0 to length(A) - 2 do
        if A[i] > A[i + 1] then
            return true
        end if
    end for
    return false
end function
```
