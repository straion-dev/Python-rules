---
$schema: https://straion.com/schemas/rule/v1.json
id: 490381e6-f12d-4c60-8536-8422213d3385
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST regenerate session IDs on login and privilege change.

## Examples

```python kind=compliant
request.session.cycle_key()  # after role change (Django)
```
