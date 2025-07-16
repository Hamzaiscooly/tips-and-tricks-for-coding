# Clean Code
Clean code is readable, understandable, and easy to maintain.

---

## Use Descriptive Names
Names should clearly show what the variable or function does.

```js
let userData = getUserData(userId);
```
## Keep Functions Short
Each function should do one thing. If it’s doing too much, split it.

## Avoid Deep Nesting
Use early returns to keep code flat and readable.

```python
if not user or not user.is_active:
    return
```
## Comment the "Why", Not the "What"
Explain decisions or intent — not obvious actions.

```js
// Skip banned users
```
## Delete Unused Code
Old, unused code clutters your files. Remove it — Git has the history.

## Stay Consistent
Use the same formatting, naming style, and structure across your codebase.
