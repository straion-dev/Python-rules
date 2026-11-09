---
$schema: https://straion.com/schemas/rule/v1.json
id: 8906c757-b448-4f34-a16f-9c34d0d6a41d
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT apply regexes vulnerable to catastrophic backtracking to untrusted input.

## Examples

```python kind=violating
re.compile(r"^(\w+\s?)*$")
```
