---
$schema: https://straion.com/schemas/rule/v1.json
id: 6625396c-3bbb-42df-8e9c-6e95e9ba2af1
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST create temporary files with `tempfile.NamedTemporaryFile`, `mkstemp` or `TemporaryDirectory`.
