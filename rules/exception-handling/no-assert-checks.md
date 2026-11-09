---
$schema: https://straion.com/schemas/rule/v1.json
id: 55ffbce8-3d71-4700-b003-427d0ae0ac06
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT use `assert` for security or input checks.

## Examples

```python kind=violating
assert user.is_admin
```

```python kind=compliant
if not user.is_admin:
    raise PermissionDenied
```
