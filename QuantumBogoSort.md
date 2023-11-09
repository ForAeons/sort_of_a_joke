# Quantum Bogo Sort

## Description

Quantum Bogo Sort is a whimsical sorting algorithm that uses the principles of quantum mechanics to sort a list. The algorithm relies on the many-worlds interpretation of quantum mechanics, wherein every possible permutation of the list exists in a separate universe. The algorithm 'sorts' the list by destroying every universe in which the list is not sorted, leaving only the universe in which the list is in sorted order.

It's important to note that Quantum Bogo Sort is a theoretical concept and not an actual sorting algorithm that can be implemented or run on a classical computer or even a quantum computer. It's a joke about the absurdity of some interpretations of quantum mechanics and is not meant to be taken seriously.

## Time Complexity

- **Best**: O(n), where n is the number of items to sort. Theoretically, it sorts the list in a single operation, by finding the universe where the list is already sorted.
- **Average**: Not applicable.
- **Worst**: Not applicable.

The algorithm is said to have a best-case performance of O(n), under the assumption that it takes one step to find the correct universe.

## Space Complexity

- **Worst**: O(1) auxiliary

The space complexity is theoretically constant, as the algorithm does not require extra space for data manipulation in a classical sense.

## Stability

- Not applicable

Like with Bogo Sort, stability is not applicable to Quantum Bogo Sort due to its non-deterministic and theoretical nature.

## Pseudo Code

```plaintext
procedure quantumBogoSort(A : array of items)
    destroy all universes where A is not sorted
    if this universe still exists then
        the list A is sorted
    end if
end procedure
```
