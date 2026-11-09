---
$schema: https://straion.com/schemas/rule/v1.json
id: ef0d6635-3d5d-43af-b430-dbce589a60bc
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST resolve file paths built from user input and reject any path that is not inside the base directory.

## Examples

```python kind=compliant
p = (BASE / name).resolve()
if not p.is_relative_to(BASE.resolve()):
    raise PermissionError(name)
```
