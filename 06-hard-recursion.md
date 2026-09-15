# Thread-Safe Bounded Counter

Implement a counter class that multiple threads can increment concurrently, but that never exceeds a fixed maximum value. Calls that would exceed the max should return `False` (and not increment); successful increments return `True`.

## Signature
```python
class BoundedCounter:
    def __init__(self, max_value: int): ...
    def increment(self) -> bool: ...
    def value(self) -> int: ...
```

## Examples
| Scenario | Result | Notes |
|---|---|---|
| `c = BoundedCounter(2)` then `c.increment()` | `True` (value=1) | first increment succeeds |
| `c.increment()` again | `True` (value=2) | second increment succeeds, now at max |
| `c.increment()` a third time | `False` (value stays 2) | max reached, rejected |
| 10 threads calling `increment()` simultaneously on `BoundedCounter(5)` | `value() == 5` | must never exceed max, never undercount, due to race conditions |

## Constraints
- Must be safe under concurrent calls from multiple threads
- This is specifically designed to catch race conditions (check-then-act bugs) that look correct in single-threaded testing but fail under load
