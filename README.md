# Coding Cheatsheet

# Binary search
```
l = -1
r = len(nums)
while l + 1 < r:
  mid = (r+l)//2
  if nums[mid] >= target:
    r = mid
  else:
    l = mid
return r
```

# Indexes
## 2d matrix can be accessed via 1d matrix 
- Suppose n_cols and n_rows, 
```
index is any index in 1d access between [0, n_rows * n_cols - 1] 
mid_row = index // n_cols 
mid_col = index % n_cols 
```

## Diagonal properties
- diagonal has r == c so (r-c) will be same for all diagonals (top left to bottom right)
- anti diagonal has (r+c) to be constant so that can be checked (top right to bottom left)

## Tree or Heap properties
- if we number the nodes in a BT or arrange them in heap array the indexing will be  
`left_child = 2 * parent_idx + 1`  
`right_child = 2 * parent_idx + 2`

# Trees
- Complete tree iff no empty node before complete nodes OR numbering of node < total_nodes_of_tree (LC 958)

# Graph Traversal

## BFS
- When to use level wise popping vs simple popping?
```
In shortest path problems specifically:

Level size IS needed when:

- You need to track distance/steps (like in the Knight moves problem)
- You need to increment some count per level
- You need to process all nodes at current distance before moving to next
Eg: Level order traversal of tree, RHS View of Tree, Shortest Distance

Simple queue is fine when:

- You're just looking for first occurrence/path
- You're maintaining distance in the queue items themselves (Imp point to note for shortest distance problems)
- You have a visited set handling distance implicitly
```

# Bitwise operations
- xor with itself will be 0
- In the binary representation, the least significant 1-bit in n always corresponds to a 0-bit in n−1. Therefore, anding the two numbers n and n−1 always flips the least significant 1-bit in n to 0, and keeps all other bits the same.
- fun gimmicks:
 ```
x // 2 can be written as x >> 1
x % 2 can be written as x & 1
```
