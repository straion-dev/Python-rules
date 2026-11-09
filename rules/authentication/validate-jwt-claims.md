---
$schema: https://straion.com/schemas/rule/v1.json
id: 92291c90-0f25-47e5-8fe9-60038b72adc1
meta:
  tags:
    - security
  frameworks:
    - pyjwt
provenance:
  updatedBy: <straion>
---

MUST validate the `exp`, `aud` and `iss` claims of JWTs.
