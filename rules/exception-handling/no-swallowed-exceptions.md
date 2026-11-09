---
$schema: https://straion.com/schemas/rule/v1.json
id: 6ddaaf18-f663-4ae5-ae56-630fc42fb8b7
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT swallow exceptions with `except Exception: pass` or `continue`.

## Examples

```python kind=violating
try:
    send_email()
except Exception:
    pass
```
