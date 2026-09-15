# Longest Substring with At Most K Distinct Characters

Given a string `s` and an integer `k`, return the length of the longest substring containing at most `k` distinct characters.

## Signature
```python
def longest_substring_k_distinct(s: str, k: int) -> int
```

## Examples
| Input | Output | Notes |
|---|---|---|
| `longest_substring_k_distinct("eceba", 2)` | `3` | `"ece"` |
| `longest_substring_k_distinct("aa", 1)` | `2` | whole string, only one distinct char |
| `longest_substring_k_distinct("a", 0)` | `0` | `k=0` means no characters allowed — classic off-by-one trap |
| `longest_substring_k_distinct("", 5)` | `0` | empty string, edge case |

## Constraints
- `0 <= len(s) <= 5×10^4`
- `0 <= k <= 50`
- Deliberately includes `k=0` and empty-string cases, since sliding-window solutions frequently mishandle window-shrink boundaries here.
