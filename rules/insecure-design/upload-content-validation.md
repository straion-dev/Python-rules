---
$schema: https://straion.com/schemas/rule/v1.json
id: ecb41013-3826-4e84-bf49-a22fc35947ba
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST validate upload file type by content (magic bytes), not by filename or `Content-Type`.

## Examples

```python kind=violating
if upload.filename.endswith(".png"): save(upload)
```

```python kind=compliant
kind = filetype.guess(upload.stream.read(261))
if kind is None or kind.mime not in {"image/png", "image/jpeg"}:
    raise ValidationError("unsupported file type")
```
