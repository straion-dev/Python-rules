---
$schema: https://straion.com/schemas/rule/v1.json
id: 13534ebd-2886-4a4a-9c0a-008c71ca9e56
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT use `ssl._create_unverified_context`.

## Examples

```python kind=violating
ctx = ssl._create_unverified_context()
```
