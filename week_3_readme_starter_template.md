# README Starter Template

# Week 3: The Royal Rail Ledger

## Summary
Write 3 to 6 lines that explain:
- what this assignment does
- which functions you implemented
- which linked-list types are used
- what part was hardest for you

**Starter prompt:**
This assignment focuses on linked-list operations in a railway story setting. I implemented functions for building and reading a singly linked list, finding the first repeated value, removing banned cargo from a doubly linked list, and checking whether a train is a palindrome. The assignment uses both singly linked lists and doubly linked lists. The hardest part was handling the pointer updates correctly in the doubly linked list.

---

## Approach
Use bullets. For each function, explain your basic strategy.

### `build_sll_from_list(values)`
- I started with creating an empty linked list.
- I built the list by creating nodes and linking them using the next pointer.
- I made sure the values stayed in the correct order by adding nodes one by one.

### `sll_to_list(sll)`
- I started at the head of the list
- I traversed the list by moving to the next node
- I collected values in a Python list by appending each value

### `find_first_repeat_sll(sll)`
- I tracked values I had already seen by using a set.
- When I found a repeated value, I returned it immediately
- If I reached the end with no repeat, I returned None

### `remove_all_from_dll(dll, target)`
- I traversed the list using a current pointer
- When I found the target value, I updated prev and next links
- I checked special cases such as removing head, tail, and all nodes

### `is_train_palindrome(dll)`
- I compared values from head and tail
- I stopped when both pointers met in the middle
- I returned `True` or `False` based on value matched.

---

## Complexity
For each required function, list:
- **Time complexity:** O(n)
- **Space complexity:** O(n)
- **Why:we create n nodes and traverse once

### `build_sll_from_list(values)`
- **Time complexity:** O(n)
- **Space complexity:** O(n)
- **Why: Because I go through all the values once and create a new node for each value.

### `sll_to_list(sll)`
- **Time complexity:** O(n)
- **Space complexity:** O(n)
- **Why:we traverse all nodes and store values

### `find_first_repeat_sll(sll)`
- **Time complexity:** O(n)
- **Space complexity:** O(n)
- **Why:we store seen values in a set

### `remove_all_from_dll(dll, target)`
- **Time complexity:** O(n)
- **Space complexity:** O(1)
- - **Why:** we traverse once and update pointers without extra space

### `is_train_palindrome(dll)` *(stretch)*
- **Time complexity:** O(n)
- **Space complexity:** O(1)
- **Why:we compare from both ends without extra space

### Complexity notes to think about
You should be ready to explain ideas like:
- linked lists do not give direct indexed access like Python lists
- traversal is usually linear
- pointer updates can be efficient when you already know where to modify the list
- different structures make different tradeoffs

---

## Edge-Case Checklist
Mark each item after you test it.

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
List any help you used.

### AI use
- I used AI: Yes 
- It helped me understand linked lists and debug errors

### Other sources
- Class notes:yes
- Slides:yes
- Book:yes 
- Websites: no 
- Other: no

---

## Debugging Notes
Write 2 to 5 bullets about what went wrong and how you fixed it.

- I first got stuck on writing functions inside functions
- The failing test that helped me most was the remove function
- I fixed the issue by correcting indentation and pointer updates
- One mistake I will avoid next time is incorrect function structure

---

## Final Reflection
Write 2 to 4 lines.
This assignment helped me understand how linked lists work and how to update pointers correctly. Doubly linked lists were harder because both next and prev must be updated. I learned to carefully handle edge cases like empty lists and removing nodes.

Possible prompts:
- What did this assignment teach you about linked lists?
- Which was harder: SLL or DLL, and why?
- What edge case surprised you the most?
- What would you review before the next quiz or assignment?

