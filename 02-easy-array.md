# Merge Overlapping Intervals

Given a list of intervals `[start, end]`, merge all overlapping intervals and return the merged list, sorted by start time.

## Signature
```python
def merge_intervals(intervals: list[list[int]]) -> list[list[int]]
```

## Examples
| Input | Output | Notes |
|---|---|---|
| `merge_intervals([[1,3],[2,6],[8,10]])` | `[[1,6],[8,10]]` | `[1,3]` and `[2,6]` overlap |
| `merge_intervals([])` | `[]` | empty list, edge case |
| `merge_intervals([[1,4],[4,5]])` | `[[1,5]]` | touching intervals count as overlapping |

## Constraints
- `0 <= len(intervals) <= 10^4`
- `start <= end` for each interval
