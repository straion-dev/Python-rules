---
$schema: https://straion.com/schemas/rule/v1.json
id: cffa71bd-7c3f-4416-a72a-889fa76bf4ef
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST name uploaded files with `werkzeug.utils.secure_filename` or server-generated names.
