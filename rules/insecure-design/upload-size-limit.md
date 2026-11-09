---
$schema: https://straion.com/schemas/rule/v1.json
id: bd6fcfea-5a3e-423d-a445-fba7674a795f
meta:
  tags:
    - security
  languages:
    - python
provenance:
  updatedBy: <straion>
---

MUST enforce size limits on file uploads.

## Examples

```python kind=compliant
app.config["MAX_CONTENT_LENGTH"] = 10 * 1024 * 1024  # Flask
```

```python kind=compliant
DATA_UPLOAD_MAX_MEMORY_SIZE = 10 * 1024 * 1024  # Django
```
