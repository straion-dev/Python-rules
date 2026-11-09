---
$schema: https://straion.com/schemas/rule/v1.json
id: 118606a8-ec14-404e-9cc8-fd12cbcdfcf2
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST redirect to user-supplied URLs only when the host is allowlisted (e.g. `url_has_allowed_host_and_scheme` in Django).

## Examples

```python kind=violating
return redirect(request.GET["next"])
```

```python kind=compliant
nxt = request.GET.get("next", "/")
if not url_has_allowed_host_and_scheme(nxt, allowed_hosts={request.get_host()}, require_https=True):
    nxt = "/"
return redirect(nxt)
```
