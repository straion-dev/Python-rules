---
$schema: https://straion.com/schemas/rule/v1.json
id: dcc43409-ca57-4691-8a19-9d83db5f1192
meta:
  tags:
    - security
  languages:
    - python
provenance:
  updatedBy: <straion>
---

SHOULD prefer `safetensors` for ML model weights.

## Examples

```python kind=compliant
from safetensors.torch import load_file
state = load_file(path)
```
