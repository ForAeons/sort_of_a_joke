# Bogo Sort

## Description

Bogo Sort, also known as permutation sort, stupid sort, or random sort, is a particularly ineffective algorithm based on the generate and test paradigm. The function successively generates permutations of its input until it finds one that is sorted. It is considered a highly inefficient sorting algorithm and is used primarily as an educational exercise to illustrate algorithmic inefficiency.

## Time Complexity

- **Best**: O(n), occurring with a chance of 1/(n!) if the list happens to be sorted immediately.
- **Average**: O((n+1)!), which is factorial time, making it impractical for even modest n.
- **Worst**: Unbounded; in theory, it could run indefinitely.

## Space Complexity

- **Worst**: O(1) auxiliary

Bogo Sort requires only a constant amount of additional space, but the time complexity makes it impractical for sorting.

## Stability

- Not applicable

## Pseudo Code

```plaintext
procedure bogoSort(A : array of items)
    while isNotSorted(A) do
        shuffle(A)
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

procedure shuffle(A)
    for i := 0 to length(A) - 1 inclusive do
        swap A[i] with A[random(i, length(A) - 1)]
    end for
end procedure
```
