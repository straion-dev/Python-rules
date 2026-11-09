---
$schema: https://straion.com/schemas/rule/v1.json
id: 2b7400e0-edc7-4938-9a3f-5832b9552be9
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST sanitize user-supplied rich HTML with an allowlist sanitizer (e.g. `nh3`).

## Examples

```python kind=compliant
safe_html = nh3.clean(user_html)
```
