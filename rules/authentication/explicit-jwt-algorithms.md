---
$schema: https://straion.com/schemas/rule/v1.json
id: f0646d0f-0a28-4c64-9c27-f43bf3945b19
meta:
  tags:
    - security
  frameworks:
    - pyjwt
provenance:
  updatedBy: <straion>
---

MUST pass an explicit `algorithms=[...]` list to `jwt.decode`.

## Examples

```python kind=violating
jwt.decode(t, key)
```

```python kind=compliant
jwt.decode(t, key, algorithms=["RS256"], audience=AUD, issuer=ISS, options={"require": ["exp", "iat"]})
```
