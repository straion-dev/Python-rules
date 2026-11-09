---
$schema: https://straion.com/schemas/rule/v1.json
id: 3f286a50-cafc-4ba5-85e1-9618563caa84
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST call `tarfile.extractall` with `filter="data"`.

## Examples

```python kind=violating
tar.extractall(path)
```

```python kind=compliant
tar.extractall(path, filter="data")
```
