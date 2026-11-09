---
$schema: https://straion.com/schemas/rule/v1.json
id: 94865ce5-df68-4cef-823a-0dae28e3b34a
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT ignore `None` results from lookups.

## Examples

```python kind=compliant
user = session.get(User, uid)
if user is None:
    raise NotFound
```
