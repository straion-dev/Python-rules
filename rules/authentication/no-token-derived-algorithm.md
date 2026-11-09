---
$schema: https://straion.com/schemas/rule/v1.json
id: 45cfb9c8-100c-4a4b-92d9-cdfba3ef8374
meta:
  tags:
    - security
  frameworks:
    - pyjwt
provenance:
  updatedBy: <straion>
---

MUST NOT derive the JWT verification algorithm from the token.

## Examples

```python kind=violating
jwt.decode(t, key, algorithms=[jwt.get_unverified_header(t)["alg"]])
```
