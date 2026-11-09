---
$schema: https://straion.com/schemas/rule/v1.json
id: 5de8c5cd-d74a-4831-87cc-da6af681edae
meta:
  tags:
    - dependencies
    - security
  languages:
    - python
provenance:
  updatedBy: <straion>
---

MUST NOT `pip install` from arbitrary URLs, unpinned git refs or random wheels.

## Examples

```bash kind=violating
pip install git+https://github.com/someone/lib
```

```bash kind=violating
pip install https://example.com/lib-1.0-py3-none-any.whl
```
