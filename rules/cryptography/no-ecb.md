---
$schema: https://straion.com/schemas/rule/v1.json
id: 9f3ab427-7e90-4d52-a483-9e67ceb07e5f
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT use ECB mode.

## Examples

```python kind=violating
Cipher(algorithms.AES(key), modes.ECB())
```
