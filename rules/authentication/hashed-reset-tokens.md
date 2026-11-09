---
$schema: https://straion.com/schemas/rule/v1.json
id: 2e0d3398-1022-496a-91ac-893daa70b8c4
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST store password-reset and email-verification tokens hashed.

## Examples

```python kind=compliant
token = secrets.token_urlsafe(32)
PasswordReset.objects.create(
    user=user,
    token_hash=hashlib.sha256(token.encode()).hexdigest(),
    expires_at=timezone.now() + timedelta(minutes=30),
)
```
