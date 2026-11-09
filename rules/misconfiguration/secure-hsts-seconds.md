---
$schema: https://straion.com/schemas/rule/v1.json
id: 429f5c01-0426-41be-8211-a83b78c0b896
meta:
  tags:
    - security
  languages:
    - python
  frameworks:
    - django
provenance:
  updatedBy: <straion>
---

MUST set `SECURE_HSTS_SECONDS` in production.

## Examples

```python kind=compliant
SECURE_SSL_REDIRECT = True
SECURE_HSTS_SECONDS = 31536000
SECURE_HSTS_INCLUDE_SUBDOMAINS = True
SESSION_COOKIE_SECURE = True
CSRF_COOKIE_SECURE = True
```
