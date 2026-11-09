---
$schema: https://straion.com/schemas/rule/v1.json
id: ca77dae9-bd55-47be-a9c5-e51bb3201249
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST validate all input at the boundary with strict schemas (Pydantic, DRF serializers, marshmallow) covering types, lengths, ranges, formats and allowlists.

## Examples

```python kind=compliant
class SignupIn(BaseModel):
    model_config = ConfigDict(extra="forbid")
    email: EmailStr
    name: str = Field(min_length=1, max_length=100)
    plan: Literal["free", "pro"]
```
