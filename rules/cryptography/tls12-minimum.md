---
$schema: https://straion.com/schemas/rule/v1.json
id: 36058a25-5f3c-4a38-8615-56617de0152f
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST set `minimum_version = ssl.TLSVersion.TLSv1_2` wherever you configure a TLS context.

## Examples

```python kind=compliant
ctx = ssl.create_default_context()
ctx.minimum_version = ssl.TLSVersion.TLSv1_2
```
