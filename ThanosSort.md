# Thanos Sort

## Description

Thanos Sort is a fictional sorting algorithm inspired by the Marvel character Thanos. In the spirit of Thanos' philosophy of restoring balance by randomly eliminating half of all life, Thanos Sort "balances" an array by randomly removing half of the elements in the hope that the remaining array is sorted. This process is repeated until the array is sorted or a single element reamins, which forms a trivially sorted array.

## Time Complexity

- **Best**: O(n), assuming that the random removal results in a sorted list.
- **Average**: O(n), since the expected number of steps to sort the array is a series that converges to a constant multiplied by n.
- **Worst**: Unbounded, as there is a possibility that the list may never be sorted with this method.

## Space Complexity

- **Worst**: O(1) auxiliary

Thanos Sort would theoretically operate in place, "snapping away" elements without requiring additional space.

## Stability

- Not applicable

## Pseudo Code

```plaintext
procedure thanosSort(A : array of items)
    while isNotSorted(A) do
        snap(A)
    end while
end procedure

procedure isNotSorted(A)
    for i := 0 to length(A) - 2 inclusive do
        if A[i] > A[i + 1] then
            return true
        end if
    end for
    return false
end procedure

procedure snap(A)
    for i := 0 to length(A) - 1 inclusive do
        if randomBoolean() then
            remove A[i]
        end if
    end for
    // Compacting the array after removals
    A := compactArray(A)
end procedure

function randomBoolean()
    // Returns true or false randomly
    return random(0, 1) == 1
end function

function compactArray(A)
    // Returns a new array with non-removed elements
    newArray := []
    for each element in A do
        if element is not removed then
            append element to newArray
        end if
    end for
    return newArray
end function
```
