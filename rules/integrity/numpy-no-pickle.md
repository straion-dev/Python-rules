---
$schema: https://straion.com/schemas/rule/v1.json
id: c5a587f8-0bb2-427e-aa9f-42f50601b6e2
meta:
  tags:
    - security
  languages:
    - python
  frameworks:
    - numpy
provenance:
  updatedBy: <straion>
---

MUST call `numpy.load` with `allow_pickle=False`.

## Examples

```python kind=violating
arr = np.load(path, allow_pickle=True)
```

```python kind=compliant
arr = np.load(path, allow_pickle=False)
```
