---
$schema: https://straion.com/schemas/rule/v1.json
id: 8191cc57-c602-4827-b765-7dea045ee3c4
meta:
  tags:
    - security
  frameworks:
    - flask
provenance:
  updatedBy: <straion>
---

MUST NOT store sensitive data in Flask's default client-side session cookie, which is signed but not encrypted.

## Examples

```python kind=violating
session["ssn"] = form.ssn.data
```
