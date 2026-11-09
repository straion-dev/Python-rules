---
$schema: https://straion.com/schemas/rule/v1.json
id: d7616795-f9cb-4b2e-81f4-102244cd0144
meta:
  tags:
    - security
  frameworks:
    - pandas
provenance:
  updatedBy: <straion>
---

MUST NOT pass user input to `pandas.eval`, `DataFrame.eval` or `DataFrame.query`.

## Examples

```python kind=violating
df.query(request.args["filter"])
```

```python kind=compliant
df[df["status"] == validated_status]
```
