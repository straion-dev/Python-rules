---
$schema: https://straion.com/schemas/rule/v1.json
id: 213e5c40-9621-449b-80f5-f5e92abe6b90
meta:
  tags:
    - security
  languages:
    - python
provenance:
  updatedBy: <straion>
---

MUST check function-level permissions (roles or scopes) on privileged and administrative operations, not only authentication.

## Examples

```python kind=violating
@login_required
def issue_refund(request, oid): ...
```

```python kind=compliant
@permission_required("billing.issue_refund", raise_exception=True)
def issue_refund(request, oid): ...
```
