# API Endpoint — User Registration with Validation

Build a REST endpoint `POST /users` that accepts JSON `{email, password, age}`, validates it, and stores the user (in-memory dict is fine) or returns a clear error.

## Validation Rules
- `email` must match a valid email pattern and be unique
- `password` must be 8+ characters with at least one digit
- `age` must be an integer between 13 and 120

## Examples
| Scenario | Result | Notes |
|---|---|---|
| Valid payload | `201 Created`, returns the new user's ID | happy path |
| Duplicate email | `409 Conflict` with message `"email already registered"` | uniqueness check |
| `password: "short"` | `400 Bad Request` with message identifying which rule failed | validation error, must be specific |

## Constraints
- Use any framework (Flask/FastAPI)
- No real database needed — clarity of validation logic and error handling is what's being tested
