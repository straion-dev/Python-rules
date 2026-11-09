---
$schema: https://straion.com/schemas/rule/v1.json
id: 7f9d9c95-71e0-4661-b9b7-90a2b3281223
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT build SQL with f-strings, `%`, `+` or `.format()` from any variable data.

## Examples

```python kind=violating
cur.execute("SELECT * FROM t WHERE name = '%s'" % name)
```

```python kind=violating
cur.execute("SELECT * FROM t WHERE name = '{}'".format(name))
```
