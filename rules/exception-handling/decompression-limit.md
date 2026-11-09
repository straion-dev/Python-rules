---
$schema: https://straion.com/schemas/rule/v1.json
id: 1c415b0d-d213-45b3-9d1a-c31a1701b0f6
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST bound the decompressed size when inflating untrusted archives or compressed streams.

## Examples

```python kind=compliant
if sum(m.file_size for m in zf.infolist()) > MAX_UNZIPPED_BYTES:
    raise ValueError("archive too large")
```
