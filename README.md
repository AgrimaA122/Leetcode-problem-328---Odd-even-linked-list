# Leetcode-problem-328---Odd-even-linked-list
Solution to problem 328


### Approach

Use two pointers to separate the linked list into odd-positioned and even-positioned nodes. Then connect the odd list to the even list.

### Algorithm

1. If the list is empty or has only one node, return `head`.

2. Initialize:

   * `odd = head` (first odd node)

   * `even = head->next` (first even node)

   * `evenHead = even` (store the start of the even list)

3. Traverse the list while `even` and `even->next` exist:

   * Connect the current odd node to the next odd node.

   * Move `odd` to the next odd node.

   * Connect the current even node to the next even node.

   * Move `even` to the next even node.

4. Connect the last odd node to `evenHead`.

5. Return `head`.

### Complexity Analysis

* Time Complexity: `O(n)` — Each node is visited once.

* Space Complexity: `O(1)` — Only a few pointers are used; no extra data structures are required.
