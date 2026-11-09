---
$schema: https://straion.com/schemas/rule/v1.json
id: e7e67355-f202-4860-b82c-e6a69678b515
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST store uploaded files under generated names.

## Examples

```python kind=compliant
stored_name = f"{uuid.uuid4().hex}.{kind.extension}"
```
