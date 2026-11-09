---
$schema: https://straion.com/schemas/rule/v1.json
id: 38115dfc-cb7b-4780-b23d-bd3a3a07a442
meta:
  tags:
    - observability
    - security
provenance:
  updatedBy: <straion>
---

MUST neutralize CR/LF in logged values to prevent log injection.

## Examples

```python kind=compliant
safe = value.replace("\r", "\\r").replace("\n", "\\n")
```
