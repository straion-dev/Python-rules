---
$schema: https://straion.com/schemas/rule/v1.json
id: b66e829b-2809-4e7e-8402-46d18f113f50
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT call `eval`, `exec` or `compile` on untrusted input.

## Examples

```python kind=violating
value = eval(request.args["data"])
```

```python kind=compliant
value = json.loads(request.args["data"])
```
