# Clean Code

## 1. Use Clear and Descriptive Names

Bad:
```python
def fxn(a, b):
    return a + b
```
Good:

```python
def add_prices(price1, price2):
    return price1 + price2
```
Meaningful names make the code easier to read and maintain.

## 2. Keep Functions Small
Instead of writing one long function that does multiple things, break it down into smaller, focused functions.
Bad:
```python
def process_order(order):
    # validate, calculate, send email all in one
```
Good:

```python
def validate_order(order):
    ...
def calculate_total(order):
    ...
def send_confirmation_email(order):
    ...
```
## 3. Avoid Deep Nesting
Too much indentation makes code hard to follow. Use early returns.

Bad:
```python
def check_user(user):
    if user:
        if user.is_active:
            if user.has_permission:
                return True
```
Good:

```python
def check_user(user):
    if not user or not user.is_active or not user.has_permission:
        return False
    return True
```
## 4. Write Comments That Explain “Why”
Explain the reasoning behind decisions — not what the code is doing (that should be obvious from the code).

Bad:

```python
# loop through users
for user in users:
    ...
```
Good:

```python
# Skip inactive users to save processing time
for user in users:
    if not user.is_active:
        continue
```
## 5. Delete Unused Code
Always remove commented-out code or unused functions. It clutters the codebase and adds confusion!
Hope these tips can help you out!
