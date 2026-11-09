---
$schema: https://straion.com/schemas/rule/v1.json
id: 6f7b6e79-d6c3-4f8c-b660-670f8f7ea910
meta:
  tags:
    - security
  frameworks:
    - django
provenance:
  updatedBy: <straion>
---

MUST NOT apply `@csrf_exempt` to a cookie-authenticated view.
