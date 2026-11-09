---
$schema: https://straion.com/schemas/rule/v1.json
id: 03c31a6e-ae5b-4bce-8a6d-1411aab60582
meta:
  tags:
    - security
  languages:
    - python
provenance:
  updatedBy: <straion>
---

MUST NOT make fields like `is_admin`, `role`, `owner_id` or `price` client-writable.

## Examples

```python kind=compliant
class UserUpdate(BaseModel):
    model_config = ConfigDict(extra="forbid")
    display_name: str = Field(max_length=100)
    # no role / is_admin / owner_id here
```
