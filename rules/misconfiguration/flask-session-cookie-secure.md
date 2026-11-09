---
$schema: https://straion.com/schemas/rule/v1.json
id: d1627633-2d29-42ca-89b4-6d351478edb0
meta:
  tags:
    - security
  languages:
    - python
  frameworks:
    - flask
provenance:
  updatedBy: <straion>
---

MUST set `SESSION_COOKIE_SECURE = True` in production.

## Examples

```python kind=compliant
app.config.update(SESSION_COOKIE_SECURE=True, SESSION_COOKIE_HTTPONLY=True, SESSION_COOKIE_SAMESITE="Lax")
```
