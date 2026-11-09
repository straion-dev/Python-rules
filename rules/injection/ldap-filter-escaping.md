---
$schema: https://straion.com/schemas/rule/v1.json
id: 8b66b66b-1457-4393-a0e1-a25139678bb1
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST escape user input placed in LDAP filters with `ldap3.utils.conv.escape_filter_chars`.

## Examples

```python kind=violating
conn.search(base, f"(uid={username})")
```

```python kind=compliant
conn.search(base, f"(uid={escape_filter_chars(username)})")
```
