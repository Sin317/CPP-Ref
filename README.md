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
