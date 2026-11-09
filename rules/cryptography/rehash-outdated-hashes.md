---
$schema: https://straion.com/schemas/rule/v1.json
id: c0849071-2c17-4704-802d-eb4fb7940166
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

SHOULD rehash stored password hashes on successful login when `PasswordHasher.check_needs_rehash` reports outdated parameters.

## Examples

```python kind=compliant
ph.verify(user.password_hash, password)
if ph.check_needs_rehash(user.password_hash):
    user.password_hash = ph.hash(password)
```
