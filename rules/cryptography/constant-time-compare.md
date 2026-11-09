---
$schema: https://straion.com/schemas/rule/v1.json
id: 2c879aac-2fda-46bb-825d-86343a593639
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST compare secrets, tokens, MACs and signatures with `hmac.compare_digest`.

## Examples

```python kind=violating
if token == expected: ...
```

```python kind=compliant
if hmac.compare_digest(token, expected): ...
```
