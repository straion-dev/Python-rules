---
$schema: https://straion.com/schemas/rule/v1.json
id: 6661cb24-871c-4b49-bec6-7da628db4385
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT use `tempfile.mktemp` or hand-built paths in `/tmp`.

## Examples

```python kind=violating
path = tempfile.mktemp()
```

```python kind=violating
path = f"/tmp/{user_id}.csv"
```

```python kind=compliant
with tempfile.NamedTemporaryFile(suffix=".csv") as f:
    f.write(data)
```
