# Lowest Common Ancestor in a Binary Tree

Given the root of a binary tree and two node values `p` and `q` (both guaranteed to exist in the tree), return the value of their lowest common ancestor.

## Signature
```python
def lowest_common_ancestor(root: TreeNode, p: int, q: int) -> int
```

## Examples
| Input | Output | Notes |
|---|---|---|
| Tree `[3,5,1,6,2,0,8,null,null,7,4]`, `p=5, q=1` | `3` | standard case, ancestor is root |
| Same tree, `p=5, q=4` | `5` | a node can be its own ancestor |
| Single-node tree `[1]`, `p=1, q=1` | `1` | trivial case, same node twice |

## Constraints
- Number of nodes in `[1, 10^4]`
- All node values unique
- `p != q`
- Both values guaranteed present in the tree
