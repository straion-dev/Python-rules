---
$schema: https://straion.com/schemas/rule/v1.json
id: 86ef582b-62c0-4c37-8af2-c1649558c876
meta:
  tags:
    - dependencies
    - security
  languages:
    - python
provenance:
  updatedBy: <straion>
---

SHOULD NOT use `--extra-index-url` for private packages because of dependency confusion.

## Examples

```bash kind=violating
pip install --extra-index-url https://pypi.internal.example.com/simple acme-auth
```
