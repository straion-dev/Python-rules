---
$schema: https://straion.com/schemas/rule/v1.json
id: 93a2932b-24b9-43c6-863e-6eba7b4a7d96
meta:
  tags:
    - observability
    - security
provenance:
  updatedBy: <straion>
---

MUST record log timestamps in UTC from a synchronized clock.

## Examples

```python kind=compliant
logging.Formatter.converter = time.gmtime
```
