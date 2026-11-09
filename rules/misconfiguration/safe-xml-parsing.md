---
$schema: https://straion.com/schemas/rule/v1.json
id: d45b58f1-84d4-4fb9-a03d-2c71f160f187
meta:
  tags:
    - security
  languages:
    - python
provenance:
  updatedBy: <straion>
---

MUST parse XML only with `defusedxml` or lxml configured with `resolve_entities=False` and `no_network=True`.

## Examples

```python kind=violating
import xml.etree.ElementTree as ET
ET.fromstring(data)
```

```python kind=compliant
import defusedxml.ElementTree as ET
ET.fromstring(data)
```
