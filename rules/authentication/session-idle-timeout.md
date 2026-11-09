---
$schema: https://straion.com/schemas/rule/v1.json
id: a63f94d2-fbdf-4721-b9fe-416d544210e9
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST enforce an idle timeout on sessions.

## Examples

```python kind=compliant
SESSION_COOKIE_AGE = 30 * 60
SESSION_SAVE_EVERY_REQUEST = True  # sliding idle timeout (Django)
```
