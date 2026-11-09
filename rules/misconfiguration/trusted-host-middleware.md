---
$schema: https://straion.com/schemas/rule/v1.json
id: e0e3a30f-18c9-46bb-85ff-bddcb1ccf012
meta:
  tags:
    - security
  languages:
    - python
  frameworks:
    - fastapi
provenance:
  updatedBy: <straion>
---

MUST restrict accepted `Host` headers with `TrustedHostMiddleware`.

## Examples

```python kind=compliant
app.add_middleware(TrustedHostMiddleware, allowed_hosts=["api.example.com"])
```
