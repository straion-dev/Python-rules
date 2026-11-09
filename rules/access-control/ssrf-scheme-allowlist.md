---
$schema: https://straion.com/schemas/rule/v1.json
id: c99372a1-71df-493d-909d-d460e9b67a3a
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST allowlist URL schemes (`https`, maybe `http`) for outbound requests to user-influenced URLs.

## Examples

```python kind=compliant
parts = urlsplit(url)
if parts.scheme != "https" or not parts.hostname:
    raise ValueError("unsupported URL")
```
