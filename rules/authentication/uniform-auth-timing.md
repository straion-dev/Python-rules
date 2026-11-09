---
$schema: https://straion.com/schemas/rule/v1.json
id: 15bd7621-d9bd-4398-9de7-9ff8f7647a5d
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST keep response timing similar for existing and non-existing accounts.

## Examples

```python kind=compliant
DUMMY_HASH = ph.hash(secrets.token_urlsafe(16))

user = users.find_by_email(email)
try:
    ph.verify(user.password_hash if user else DUMMY_HASH, password)
except VerifyMismatchError:
    raise InvalidCredentials from None
if user is None:
    raise InvalidCredentials
```
