---
$schema: https://straion.com/schemas/rule/v1.json
id: b0ee3842-600a-4919-80fe-cf8646906f88
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST use HMAC and HS256 JWT signing secrets of at least 256 bits generated with `secrets`.

## Examples

```python kind=violating
jwt.encode(claims, "secret", algorithm="HS256")
```

```python kind=compliant
JWT_SECRET = secrets.token_bytes(32)  # generated once, stored in the secret manager
```
