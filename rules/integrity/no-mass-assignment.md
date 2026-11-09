---
$schema: https://straion.com/schemas/rule/v1.json
id: ca4a60d2-a411-4a40-8aeb-04b437ea66cc
meta:
  tags:
    - security
  languages:
    - python
provenance:
  updatedBy: <straion>
---

MUST NOT assign request data via `setattr(obj, k, v)` loops or `Model(**request.json)`.

## Examples

```python kind=violating
for k, v in request.json.items():
    setattr(user, k, v)
```

```python kind=violating
Order(**request.json)
```
