---
$schema: https://straion.com/schemas/rule/v1.json
id: 25d081f6-a01e-4e23-98a7-09e542386f31
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST load third-party scripts on web pages only from trusted origins with Subresource Integrity, or self-host them.

## Examples

```html kind=compliant
<script src="https://cdn.example.com/lib.js" integrity="sha384-..." crossorigin="anonymous"></script>
```
