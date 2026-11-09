---
$schema: https://straion.com/schemas/rule/v1.json
id: 5e115fd7-61e4-40f7-9ae3-31f53623ab6b
meta:
  tags:
    - security
  languages:
    - python
provenance:
  updatedBy: <straion>
---

MUST NOT put user-writable or current-working directories on `sys.path` or `PYTHONPATH`.

## Examples

```python kind=violating
sys.path.insert(0, os.getcwd())
```

```python kind=violating
sys.path.append(request.args["plugin_dir"])
```
