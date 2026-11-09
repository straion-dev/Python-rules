---
$schema: https://straion.com/schemas/rule/v1.json
id: c4dd6be9-4405-4706-88e7-722e3b69059d
meta:
  tags:
    - security
  frameworks:
    - sqlalchemy
provenance:
  updatedBy: <straion>
---

MUST use SQLAlchemy `text()` only with bound parameters.

## Examples

```python kind=compliant
session.execute(text("SELECT * FROM t WHERE id = :id"), {"id": oid})
```
