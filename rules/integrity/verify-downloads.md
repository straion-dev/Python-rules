---
$schema: https://straion.com/schemas/rule/v1.json
id: 0470ffb2-d7e7-41a1-ae1a-6cb2fad12aaf
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST verify code, plugins, models or updates downloaded at runtime or in build scripts by pinned hash or signature before use.

## Examples

```python kind=compliant
digest = hashlib.sha256(blob).hexdigest()
if not hmac.compare_digest(digest, PINNED_SHA256):
    raise IntegrityError("checksum mismatch")
```
