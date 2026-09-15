# Group Anagrams

Given a list of strings, group the ones that are anagrams of each other. Return the groups in any order, but preserve original order within each group.

## Signature
```python
def group_anagrams(words: list[str]) -> list[list[str]]
```

## Examples
| Input | Output | Notes |
|---|---|---|
| `group_anagrams(["eat","tea","tan","ate","nat","bat"])` | `[["eat","tea","ate"],["tan","nat"],["bat"]]` | three anagram groups |
| `group_anagrams([""])` | `[[""]]` | single empty string, edge case |
| `group_anagrams(["a"])` | `[["a"]]` | single character, no anagram partners |

## Constraints
- `1 <= len(words) <= 10^4`
- Lowercase letters only
- `0 <= len(word) <= 100`
