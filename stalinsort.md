# Stalin Sort

## Description

Stalin Sort is a tongue-in-cheek sorting algorithm that "sorts" a list by simply removing any element that is not in order. The name is a dark humor reference to the way Joseph Stalin's regime would remove ("purge") people who didn't fit the party line. In the context of sorting, if an element is found that is not greater than its predecessor (thereby not in sorted order), it is removed from the list, much like sending it to the "gulag".

## Time Complexity

- **Best**: O(n)
- **Average**: O(n)
- **Worst**: O(n)

The time complexity is linear because it involves a single pass through the data.

## Space Complexity

- **Worst**: O(1) auxiliary

Stalin Sort effectively operates in-place, modifying the input array without using any additional space beyond variables for iteration control.

## Stability

- Not applicable

The concept of stability in sorting algorithms does not apply to Stalin Sort, as the algorithm fundamentally alters the set of data by removing elements, instead of reordering them.

## Pseudo Code

```plaintext
procedure stalinSort(A : array of items)
    int i := 0
    while i < length(A) - 1 do
        if A[i] > A[i + 1] then
            remove A[i + 1]
        else
            i := i + 1
        end if
    end while
end procedure
```

## Remarks

Stalin Sort is a humorous sorting algorithm that's not meant for practical use, as it distorts the dataset by removing elements. It serves as a satirical reminder of historical events and an example of how not all sorting algorithms are concerned with preserving the integrity of the data.
