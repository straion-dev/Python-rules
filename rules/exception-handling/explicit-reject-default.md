---
$schema: https://straion.com/schemas/rule/v1.json
id: 61de1c73-fa00-4774-bdfe-d6307915e541
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST give every `match` statement and `if/elif` chain over security-relevant states an explicit default that rejects.

## Examples

```python kind=compliant
match role:
    case "admin":
        return FULL_ACCESS
    case "member":
        return READ_WRITE
    case _:
        raise PermissionDenied(role)
```
