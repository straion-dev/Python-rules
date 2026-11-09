---
$schema: https://straion.com/schemas/rule/v1.json
id: 59737eb8-b0ac-4fbd-bb87-0cf991ce0435
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST check that every `zipfile` member's resolved path stays inside the target directory before extracting.

## Examples

```python kind=compliant
target = dest.resolve()
for member in zf.infolist():
    if not (dest / member.filename).resolve().is_relative_to(target):
        raise ValueError("unsafe zip member")
zf.extractall(dest)
```
