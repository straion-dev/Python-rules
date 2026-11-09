---
$schema: https://straion.com/schemas/rule/v1.json
id: a096f7b6-d353-4638-add3-37ee624998b7
meta:
  tags:
    - security
provenance:
  updatedBy: <straion>
---

MUST NOT use plaintext protocols (FTP, unencrypted or STARTTLS-optional SMTP) for sensitive data.

## Examples

```python kind=violating
ftplib.FTP(host)
```

```python kind=compliant
smtp = smtplib.SMTP_SSL(host, 465, context=ssl.create_default_context())
```
