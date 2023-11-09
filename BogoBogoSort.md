# BogoBogo Sort

## Description

BogoBogo Sort is a variation of the already impractical Bogo Sort. This algorithm, designed to be even less efficient and more impractical for comedic or educational purposes, involves recursively applying Bogo Sort to increasingly larger pre-sorted sections of the list until the list is sorted or until the heat death of the universe, whichever comes first.

## Time Complexity

- **Best**: Unbounded; relies on a random chance that could theoretically sort the array in a finite amount of time.
- **Average**: Worse than factorial time, making it even more impractical than Bogo Sort.
- **Worst**: Infinite; the algorithm may theoretically never complete.

## Space Complexity

- **Worst**: O(1) auxiliary

Like Bogo Sort, BogoBogo Sort uses a constant amount of space.

## Stability

- Not applicable

## Pseudo Code

```plaintext
procedure bogobogoSort(A : array of items)
    n := length(A)
    for i := 1 to n inclusive do
        while isNotSorted(A[0..i]) do
            shuffle(A[0..i])
        end while
    end for
end procedure

procedure isNotSorted(A)
    for j := 0 to length(A) - 2 inclusive do
        if A[j] > A[j + 1] then
            return true
        end if
    end for
    return false
end procedure

procedure shuffle(A)
    for j := 0 to length(A) - 1 inclusive do
        swap A[j] with A[random(j, length(A) - 1)]
    end for
end procedure
```
