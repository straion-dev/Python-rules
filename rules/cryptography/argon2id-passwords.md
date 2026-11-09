---
$schema: https://straion.com/schemas/rule/v1.json
id: b07f3738-873e-4656-bbd4-779c14bf55d6
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST hash passwords with Argon2id (`argon2-cffi` `PasswordHasher`, or Django's `Argon2PasswordHasher` first in `PASSWORD_HASHERS`).

## Examples

```python kind=compliant
ph = PasswordHasher()  # argon2-cffi, Argon2id by default
stored = ph.hash(password)
ph.verify(stored, candidate)  # raises VerifyMismatchError on mismatch
```

```python kind=compliant
PASSWORD_HASHERS = ["django.contrib.auth.hashers.Argon2PasswordHasher", ...]
```
