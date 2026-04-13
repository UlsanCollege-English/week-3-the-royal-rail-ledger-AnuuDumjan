# Week 3: The Royal Rail Ledger

## Summary
This assignment focuses on implementing linked-list operations using a railway-themed problem. I implemented functions to build and convert a singly linked list, find the first repeated value, remove specific values from a doubly linked list, and check if a train forms a palindrome. The assignment uses both singly linked lists (SLL) and doubly linked lists (DLL). The most challenging part was correctly updating the prev and next pointers in the doubly linked list.

---

## Approach

### `build_sll_from_list(values)`
- I created an empty singly linked list.
- I initialized the head with the first value.
- I iterated through the remaining values and linked nodes using the next pointer.

### `sll_to_list(sll)`
- I started from the head node.
- I traversed the list using the next pointer.
- I appended each node’s value to a Python list.

### `find_first_repeat_sll(sll)`
- I used a set to track visited values.
- While traversing, I checked if a value already exists in the set.
- I returned the first repeated value, or None if no repetition exists.

### `remove_all_from_dll(dll, target)`
- I traversed the list using a current pointer.
- When I found the target value, I updated both prev and next links.
- I handled special cases like removing the head, tail, and all nodes.

### `is_train_palindrome(dll)`
- I used two pointers: one from the head and one from the tail.
- I compared values while moving inward.
- I stopped when the pointers met or crossed and returned True or False.

---

## Complexity

### `build_sll_from_list(values)`
- **Time complexity:** O(n)
- **Space complexity:** O(n)
- **Why:** We traverse all values once and create a node for each value.

### `sll_to_list(sll)`
- **Time complexity:** O(n)
- **Space complexity:** O(n)
- **Why:** We traverse the entire list and store values in a list.

### `find_first_repeat_sll(sll)`
- **Time complexity:** O(n)
- **Space complexity:** O(n)
- **Why:** We traverse once and store seen values in a set.

### `remove_all_from_dll(dll, target)`
- **Time complexity:** O(n)
- **Space complexity:** O(1)
- **Why:** We only traverse the list once and update pointers in place.

### `is_train_palindrome(dll)`
- **Time complexity:** O(n)
- **Space complexity:** O(1)
- **Why:** We compare values from both ends without extra storage.

---

## Edge-Case Checklist

- [x] empty SLL
- [x] empty DLL
- [x] single-node SLL
- [x] single-node DLL
- [x] no repeated values in SLL
- [x] repeated value appears later in SLL
- [x] repeated value includes the head value
- [x] removing from DLL when target is at head
- [x] removing from DLL when target is at tail
- [x] removing consecutive target values in DLL
- [x] removing all nodes from DLL
- [x] palindrome with odd length
- [x] palindrome with even length
- [x] non-palindrome DLL

---

## Assistance & Sources

### AI use
- I used AI: Yes  
- It helped me understand linked list operations and fix pointer-related errors.

### Other sources
- Class notes: Yes  
- Slides: Yes  
- Book: Yes  

---

## Debugging Notes

- I initially struggled with pointer updates in the doubly linked list.
- Some tests failed when removing nodes at the head and tail.
- I fixed these issues by carefully updating both prev and next references.
- I also improved my palindrome logic to handle edge cases correctly.

---

## Final Reflection

This assignment helped me better understand how linked lists work, especially pointer manipulation. Doubly linked lists were more challenging because both directions must be handled carefully. I learned the importance of testing edge cases and writing clean logic.