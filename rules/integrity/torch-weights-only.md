---
$schema: https://straion.com/schemas/rule/v1.json
id: cde2038c-bcd5-44e5-8ca2-17020fbfcc3b
meta:
  tags:
    - security
  languages:
    - python
  frameworks:
    - pytorch
provenance:
  updatedBy: <straion>
---

MUST load PyTorch models with `torch.load(..., weights_only=True)`.

## Examples

```python kind=violating
model = torch.load(path)
```

```python kind=compliant
state = torch.load(path, weights_only=True)
```
