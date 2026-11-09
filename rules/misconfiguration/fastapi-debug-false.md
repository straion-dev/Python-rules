---
$schema: https://straion.com/schemas/rule/v1.json
id: b1458d1e-05ef-4f6a-890e-87532a39cb2a
meta:
  tags:
    - security
  languages:
    - python
  frameworks:
    - fastapi
provenance:
  updatedBy: <straion>
---

MUST set `debug=False` in production.

## Examples

```python kind=compliant
app = FastAPI(debug=False)
```
