---
$schema: https://straion.com/schemas/rule/v1.json
id: b9abb385-8aed-4cb9-b788-e49f9ea73e14
meta:
  tags:
    - security
  frameworks:
    - pyjwt
provenance:
  updatedBy: <straion>
---

MUST NOT disable JWT signature verification.

## Examples

```python kind=violating
jwt.decode(t, options={"verify_signature": False})
```
