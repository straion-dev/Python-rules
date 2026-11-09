---
$schema: https://straion.com/schemas/rule/v1.json
id: 049f542b-80ab-494b-bc90-ad1cb17a91b1
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST allowlist URL schemes (e.g. `https`, `http`, `mailto`) for user-supplied URLs rendered into `href` or `src` attributes.

## Examples

```python kind=compliant
if urlsplit(url).scheme not in {"https", "http", "mailto"}:
    raise ValidationError("unsupported link")
```
