---
$schema: https://straion.com/schemas/rule/v1.json
id: 23024622-28dc-4b32-b0fd-10f3801e90f2
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST derive keys from passwords only via a KDF (Argon2, scrypt, PBKDF2 or HKDF as appropriate).

## Examples

```python kind=compliant
salt = os.urandom(16)
key = Scrypt(salt=salt, length=32, n=2**17, r=8, p=1).derive(password.encode())
```
