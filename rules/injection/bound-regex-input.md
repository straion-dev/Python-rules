---
$schema: https://straion.com/schemas/rule/v1.json
id: 469e3c87-df44-4b46-a1e1-99d7c6480d49
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST bound input length before applying regexes to untrusted input.

## Examples

```python kind=compliant
if len(value) > 254:
    raise ValidationError("too long")
if not EMAIL_RE.fullmatch(value):
    raise ValidationError("invalid email")
```
