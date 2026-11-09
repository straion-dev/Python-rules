---
$schema: https://straion.com/schemas/rule/v1.json
id: 73fc6551-fab0-4ef9-90d2-f3586bf822ce
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT serve uploaded files inline from the app's origin.

## Examples

```python kind=compliant
return FileResponse(path, as_attachment=True, filename=download_name)
```
