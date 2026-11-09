---
$schema: https://straion.com/schemas/rule/v1.json
id: 7f3b6ee4-5598-494e-9db3-d94e2819b0c9
meta:
  tags:
    - observability
    - security
provenance:
  updatedBy: <straion>
---

MUST redact sensitive data via a logging filter rather than by convention.

## Examples

```python kind=compliant
class RedactFilter(logging.Filter):
    PATTERN = re.compile(r"(?i)(authorization|password|token|api_key)=\S+")

    def filter(self, record):
        record.msg = self.PATTERN.sub(r"\1=[REDACTED]", record.getMessage())
        record.args = ()
        return True
```
