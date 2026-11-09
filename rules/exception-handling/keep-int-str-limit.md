---
$schema: https://straion.com/schemas/rule/v1.json
id: 3b273106-d524-492a-b9a3-49754c7883c6
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT disable Python's int-string conversion limit (`sys.set_int_max_str_digits(0)`).

## Examples

```python kind=violating
sys.set_int_max_str_digits(0)
```
