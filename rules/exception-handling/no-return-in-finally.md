---
$schema: https://straion.com/schemas/rule/v1.json
id: 860bf06c-3e96-49ce-8a12-86bb123f477f
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT `return`, `break` or `continue` inside a `finally` block.

## Examples

```python kind=violating
try:
    charge(card)
finally:
    return True  # swallows any exception
```
