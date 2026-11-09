---
$schema: https://straion.com/schemas/rule/v1.json
id: 73fc64b1-e053-4f88-b4fa-3aef9a42f7d8
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST preserve the cause when re-raising or wrapping exceptions (`raise DomainError(...) from err`).

## Examples

```python kind=compliant
except KeyError as err:
    raise DomainError("missing field") from err
```
