---
$schema: https://straion.com/schemas/rule/v1.json
id: 3d2ad579-d41d-46ba-a1e4-0f77b8eb9fd2
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST resolve the hostname of a user-influenced URL and reject the request unless every resolved address satisfies `ipaddress.ip_address(a).is_global`.

## Examples

```python kind=compliant
infos = socket.getaddrinfo(host, port, type=socket.SOCK_STREAM)
addrs = {info[4][0] for info in infos}
if not addrs or not all(ipaddress.ip_address(a).is_global for a in addrs):
    raise ValueError("destination not allowed")
```
