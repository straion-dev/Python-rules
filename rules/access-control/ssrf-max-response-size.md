---
$schema: https://straion.com/schemas/rule/v1.json
id: 874b41b0-bb53-4e98-afa9-388dcd7fe918
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST set a maximum response size on outbound requests to user-influenced URLs.

## Examples

```python kind=compliant
with requests.get(url, stream=True, timeout=5, allow_redirects=False) as resp:
    resp.raise_for_status()
    body = bytearray()
    for chunk in resp.iter_content(65536):
        body += chunk
        if len(body) > MAX_BYTES:
            raise ValueError("response too large")
```
