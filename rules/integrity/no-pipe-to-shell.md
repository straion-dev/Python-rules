---
$schema: https://straion.com/schemas/rule/v1.json
id: 4c304330-db6a-4044-8653-4f8670d68107
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT use `curl | sh` or `pip install <url>` patterns.

## Examples

```bash kind=violating
curl -sSL https://example.com/install.sh | sh
```
