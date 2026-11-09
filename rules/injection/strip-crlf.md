---
$schema: https://straion.com/schemas/rule/v1.json
id: 95de2d7d-4116-468e-893d-02760f81b23a
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST strip or reject CR/LF in values placed into HTTP headers, emails and log lines.

## Examples

```python kind=compliant
if "\r" in filename or "\n" in filename:
    raise ValidationError("invalid filename")
response.headers["Content-Disposition"] = f'attachment; filename="{filename}"'
```
