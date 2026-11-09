---
$schema: https://straion.com/schemas/rule/v1.json
id: 9f4bc1b6-dc49-4556-a4f2-cbeaea8f415c
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST return uniform responses for login, registration and password reset to prevent account enumeration.

## Examples

```python kind=violating
return error("No account registered with this email")
```

```python kind=compliant
return error("Invalid username or password")
```
