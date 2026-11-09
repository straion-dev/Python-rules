---
$schema: https://straion.com/schemas/rule/v1.json
id: 435cc73f-5cd4-4fb1-8725-5d3e8a7c4ae5
meta:
  tags:
    - security
  languages:
    - python
provenance:
  updatedBy: <straion>
---

MUST sign and verify data the client round-trips (cookies, hidden fields, state tokens) with `itsdangerous` or `django.core.signing`.

## Examples

```python kind=compliant
signer = URLSafeTimedSerializer(settings.secret_key.get_secret_value(), salt="email-confirm")
token = signer.dumps({"uid": user.id})
data = signer.loads(token, max_age=3600)  # raises on tampering or expiry
```
