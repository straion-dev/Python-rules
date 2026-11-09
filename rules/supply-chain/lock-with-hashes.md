---
$schema: https://straion.com/schemas/rule/v1.json
id: f63a4df6-7d8c-472f-8ab4-1a1a0f1432a6
meta:
  tags:
    - dependencies
    - security
  languages:
    - python
provenance:
  updatedBy: <straion>
---

MUST lock dependencies with hashes (`uv.lock` or `pip-compile --generate-hashes`).

## Examples

```bash kind=compliant
uv lock
# or
pip-compile --generate-hashes -o requirements.txt pyproject.toml
```
