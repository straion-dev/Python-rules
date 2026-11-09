---
$schema: https://straion.com/schemas/rule/v1.json
id: 782c7b49-92f3-4cb8-bb1d-bc9ba7944b2a
meta:
  tags:
    - security
  languages:
    - python
provenance:
  updatedBy: <straion>
---

MUST load secrets from the environment or a secret manager (e.g. pydantic-settings with `SecretStr`).

## Examples

```python kind=violating
DATABASE_PASSWORD = "hunter2"
```

```python kind=compliant
class Settings(BaseSettings):
    database_password: SecretStr
    api_key: SecretStr

settings = Settings()  # read from environment / secret store
```
