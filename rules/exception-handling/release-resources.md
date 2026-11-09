---
$schema: https://straion.com/schemas/rule/v1.json
id: 32655b1e-5898-4192-926b-20d2748a1e05
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST release resources on every path with `with`, `try/finally` or `contextlib.ExitStack`.

## Examples

```python kind=violating
f = open(path)
data = f.read()
```

```python kind=compliant
with open(path) as f:
    data = f.read()
```
