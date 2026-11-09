---
$schema: https://straion.com/schemas/rule/v1.json
id: 79fb98ed-e0dc-4a0d-a1b1-b1e2a11d6a39
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST send `Cache-Control: no-store` on responses containing sensitive data.

## Examples

```python kind=compliant
response.headers["Cache-Control"] = "no-store"
```
