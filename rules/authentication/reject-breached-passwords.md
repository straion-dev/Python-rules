---
$schema: https://straion.com/schemas/rule/v1.json
id: 3dc732d1-10e8-4514-8b9d-2fa74318462b
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST reject common and known-breached passwords (e.g. via the HIBP k-anonymity range API) on signup and password change.

## Examples

```python kind=compliant
digest = hashlib.sha1(password.encode(), usedforsecurity=False).hexdigest().upper()
resp = requests.get(f"https://api.pwnedpasswords.com/range/{digest[:5]}", timeout=5)
resp.raise_for_status()
breached = any(line.split(":")[0] == digest[5:] for line in resp.text.splitlines())
```
