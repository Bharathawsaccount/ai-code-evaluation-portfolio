# React Component — Bounded Counter with Reset

Build a `<Counter max={n} />` component with increment/decrement buttons, a reset button, and a value display. The increment button must be disabled (not just ignored) when at `max`, and decrement disabled at `0`.

## Props
- `max: number` (required)
- `initial?: number` (default `0`)

## Behavior to Test
- Clicking increment near the `max` boundary — button should become disabled exactly at `max`, not before or after
- Clicking reset restores `initial` (not `0`) after several clicks
- Invalid props (`initial > max`) should be clamped or throw — pick one behavior and document it explicitly (this ambiguity is intentional — a good solution should surface the assumption, not silently guess)
