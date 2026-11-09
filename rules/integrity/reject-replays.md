---
$schema: https://straion.com/schemas/rule/v1.json
id: 4e3a936f-0b7c-4d7a-94e8-dabc954638bc
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST reject replayed webhooks or signed messages by checking a timestamp or nonce.
