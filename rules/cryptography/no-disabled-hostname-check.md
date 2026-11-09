---
$schema: https://straion.com/schemas/rule/v1.json
id: e61486c1-5198-472f-917f-b3f60a03e0d8
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT set `check_hostname = False` on SSL contexts.

## Examples

```python kind=violating
ctx.check_hostname = False
ctx.verify_mode = ssl.CERT_NONE
```
