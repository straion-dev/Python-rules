---
$schema: https://straion.com/schemas/rule/v1.json
id: d665cd84-41b2-4d49-ba91-a4f115705749
meta:
  tags:
    - security
  languages:
    - python
provenance:
  updatedBy: <straion>
---

MUST bind request data to explicit schemas (Pydantic `ConfigDict(extra="forbid")`, DRF serializer `fields`/`read_only_fields`, Django `ModelForm.fields`).

## Examples

```python kind=compliant
class OrderIn(BaseModel):
    model_config = ConfigDict(extra="forbid")
    quantity: int
```
