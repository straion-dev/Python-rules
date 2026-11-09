---
$schema: https://straion.com/schemas/rule/v1.json
id: c8659e2f-6a9f-4712-8d11-ee345db85d63
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST use `hmac` for keyed integrity.

## Examples

```python kind=violating
tag = hashlib.sha256(key + message).hexdigest()
```

```python kind=compliant
tag = hmac.new(key, message, hashlib.sha256).hexdigest()
```
