# Week 3: The Royal Rail Ledger

## Summary

This assignment focuses on implementing linked-list operations using a railway-themed problem. I implemented functions to build and convert a singly linked list, find the first repeated value, remove specific values from a doubly linked list, and check if a train forms a palindrome.

The assignment uses both singly linked lists (SLL) and doubly linked lists (DLL). The most challenging part was correctly updating the `prev` and `next` pointers in the doubly linked list.

---

## Approach

### `build_sll_from_list(values)`

- Created an empty singly linked list.
- Initialized the head with the first value.
- Iterated through remaining values and linked nodes using the `next` pointer.

### `sll_to_list(sll)`

- Started from the head node.
- Traversed the list using the `next` pointer.
- Appended each node’s value into a Python list.

### `find_first_repeat_sll(sll)`

- Used a `set` to track visited values.
- Checked whether a value had already been seen.
- Returned the first repeated value or `None` if no repetition exists.

### `remove_all_from_dll(dll, target)`

- Traversed the list using a current pointer.
- Updated both `prev` and `next` links when removing a node.
- Handled special cases such as removing the head, tail, consecutive matches, and all nodes.

### `is_train_palindrome(dll)`

- Used two pointers: one from the head and one from the tail.
- Compared values while moving inward.
- Stopped when pointers met or crossed and returned `True` or `False`.

---

## Complexity

### `build_sll_from_list(values)`

- **Time Complexity:** `O(n)`
- **Space Complexity:** `O(n)`

Why: The function traverses all values once and creates one node per value.

### `sll_to_list(sll)`

- **Time Complexity:** `O(n)`
- **Space Complexity:** `O(n)`

Why: The function traverses the full linked list and stores values in a Python list.

### `find_first_repeat_sll(sll)`

- **Time Complexity:** `O(n)`
- **Space Complexity:** `O(n)`

Why: The function traverses once while storing visited values in a set.

### `remove_all_from_dll(dll, target)`

- **Time Complexity:** `O(n)`
- **Space Complexity:** `O(1)`

Why: The function performs a single traversal and updates pointers in place.

### `is_train_palindrome(dll)`

- **Time Complexity:** `O(n)`
- **Space Complexity:** `O(1)`

Why: The function compares values from both ends without using extra storage.

---

## Edge-Case Checklist

- [x] Empty SLL
- [x] Empty DLL
- [x] Single-node SLL
- [x] Single-node DLL
- [x] No repeated values in SLL
- [x] Repeated value appears later in SLL
- [x] Repeated value includes the head value
- [x] Removing target from DLL head
- [x] Removing target from DLL tail
- [x] Removing consecutive target values
- [x] Removing all nodes from DLL
- [x] Palindrome with odd length
- [x] Palindrome with even length
- [x] Non-palindrome DLL

---

## Assistance & Sources

### AI Use

**Used AI:** Yes

AI helped me understand linked list operations and fix pointer-related errors.

### Other Sources

- Class notes
- Slides
- Course book

---

## Debugging Notes

- Initially struggled with pointer updates in the doubly linked list.
- Some tests failed when removing nodes at the head and tail.
- Fixed these issues by carefully updating both `prev` and `next` references.
- Improved palindrome logic to handle edge cases correctly.

---

## Final Reflection

This assignment improved my understanding of linked lists, especially pointer manipulation. Doubly linked lists were more challenging because both directions must be updated carefully. I learned the importance of testing edge cases and writing clean, organized logic.