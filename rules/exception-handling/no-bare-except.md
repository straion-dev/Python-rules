---
$schema: https://straion.com/schemas/rule/v1.json
id: 9d94f3d7-5cbd-42bc-a832-8196db1ee2dd
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT use bare `except:`.

## Examples

```python kind=violating
try:
    do()
except:
    pass
```
