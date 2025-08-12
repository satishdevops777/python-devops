**1. What are Python’s advantages over Bash scripting for automation in DevOps?**
- Cross-platform: Python runs on Linux, Windows, macOS without major changes.
- Rich libraries: Modules for AWS (boto3), Kubernetes (kubernetes), REST APIs (requests), etc.
- Better readability & maintainability than complex Bash scripts.
- Error handling: Try/except makes debugging easier.
- Integration with APIs is much simpler in Python.
- Bash is great for quick shell commands; Python is better for complex automation, APIs, and cross-platform work.

**2. Difference between is and ==
- == → compares values
- is → compares memory addresses (whether both refer to the same object)
```python
a = [1, 2, 3]
b = [1, 2, 3]
print(a == b)  # True  (values are same)
print(a is b)  # False (different objects)
```
**3. Difference between list, tuple, and set in Python**

| Type      | Mutable | Ordered | Allows Duplicates | Example                      |
| --------- | ------- | ------- | ----------------- | ---------------------------  |
| **list**  | ✅       | ✅       | ✅                 | `['dev', 'qa', 'prod']` |
| **tuple** | ❌       | ✅       | ✅                 | `('dev', 'qa', 'prod')` |
| **set**   | ✅       | ❌       | ❌                 | `{'dev', 'qa', 'prod'}` |

- List → changeable collection (e.g., storing filenames to process)
- Tuple → fixed data (e.g., AWS region coordinates)
- Set → unique values (e.g., unique IP addresses)

**4. Read log file and print only error messages**
```python
with open("app.log") as f:
    for line in f:
        if "error" in line.lower():
            print(line.strip())
```
