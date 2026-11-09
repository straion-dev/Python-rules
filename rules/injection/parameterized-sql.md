---
$schema: https://straion.com/schemas/rule/v1.json
id: c38fef6d-4c97-4c60-89fc-93374cb2736e
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST use parameterized queries or ORM APIs for SQL.

## Examples

```python kind=violating
cur.execute(f"SELECT * FROM users WHERE id = {uid}")
```

```python kind=compliant
cur.execute("SELECT * FROM users WHERE id = %s", (uid,))
```
