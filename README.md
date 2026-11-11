# Python Security Rules

Security rules for Python services, grouped by the OWASP Top 10 (2025) categories. Connect this repository to your Straion organization as a central rule source, and your coding agents check their work against these rules in every repository.

## Get started

You need:

- A [Straion account](https://straion.app/auth/signup) with organization admin rights. Only an admin can connect a central source.
- Node.js v22 or newer.
- git 2.42 or newer, with `user.name` and `user.email` set.
- A supported coding agent: Claude Code, Codex, Cursor or GitHub Copilot.

> [!IMPORTANT]
> Do you want to change, add or remove rules? Then fork this repository or copy it to your own git host first, and do the steps below with your copy. You cannot push changes to this repository, and Straion syncs only what is in the connected repository. To use the rules without changes, connect this repository directly.

1. Install the Straion CLI. Follow the prompts to log in and create a token.

   ```bash
   npm install -g @straion/cli
   ```

2. Configure your coding agents. The wizard installs the Straion skills and hooks for each agent you select.

   ```bash
   straion setup
   ```

3. Clone this repository, or your fork or copy of it.

   ```bash
   git clone https://github.com/straion-dev/python-rules.git
   ```

   ```bash
   cd Python-rules
   ```

4. Connect it as a central rule source.

   ```bash
   straion source repo connect --central
   ```

   The command registers the repository with your organization and runs the first sync. The collections from a central source apply to every repository in your organization, unless a [binding](https://straion.com/docs/rule-bindings/) limits them to specific repositories.

5. Open your coding agent in one of your Python projects and use the Straion skills:

   - `/straion-implement` plans and implements a feature or an issue, and checks each step against the rules.
   - `/straion-check-compliance` checks existing code changes, a pull request or a spec against the rules.

   ```text
   /straion-implement Add a password reset flow with email verification
   ```

   ```text
   /straion-check-compliance Check the changes on this branch against our rules
   ```

More example prompts are in the [Straion docs](https://straion.com/docs/example-prompts/).

## Collections

| Directory | Collection | Rules |
| --- | --- | ---: |
| [`rules/access-control`](rules/access-control) | A01 Broken Access Control | 40 |
| [`rules/misconfiguration`](rules/misconfiguration) | A02 Security Misconfiguration | 37 |
| [`rules/supply-chain`](rules/supply-chain) | A03 Software Supply Chain Failures | 8 |
| [`rules/cryptography`](rules/cryptography) | A04 Cryptographic Failures | 39 |
| [`rules/injection`](rules/injection) | A05 Injection | 28 |
| [`rules/insecure-design`](rules/insecure-design) | A06 Insecure Design | 17 |
| [`rules/authentication`](rules/authentication) | A07 Authentication Failures | 39 |
| [`rules/integrity`](rules/integrity) | A08 Software or Data Integrity Failures | 17 |
| [`rules/logging`](rules/logging) | A09 Security Logging and Alerting Failures | 14 |
| [`rules/exception-handling`](rules/exception-handling) | A10 Mishandling of Exceptional Conditions | 26 |
| [`rules/tooling`](rules/tooling) | Security Tooling and CI Gates | 3 |

The `README.md` in each collection describes its scope.

## Rule format

Each rule is one Markdown file. The YAML front matter holds the metadata. The body holds the requirement and examples:

````markdown
---
$schema: https://straion.com/schemas/rule/v1.json
id: <uuid>
meta:
  tags:
    - security
---

MUST NOT use `tempfile.mktemp` or hand-built paths in `/tmp`.

## Examples

```python kind=violating
path = tempfile.mktemp()
```

```python kind=compliant
with tempfile.NamedTemporaryFile(suffix=".csv") as f:
    f.write(data)
```
````

- Start the requirement with an RFC 2119 keyword: `MUST`, `MUST NOT`, `SHOULD`, `SHOULD NOT` or `MAY`.
- Mark each code example `kind=violating` or `kind=compliant`.
- Do not change the `id` of a published rule. Give a new rule a new UUID.

The [rule file format](https://straion.com/docs/rule-file-format/) page has the full reference.

## Change the rules

To change the rules, you must have your own fork or copy of this repository, connected to Straion as shown in [Get started](#get-started). Make the changes in your copy:

1. Create a branch from `straion/rules/v1`.
2. Add or edit rule files in the correct collection folder. Give each file a short kebab-case name that says what the rule enforces, for example `no-mktemp.md`.
3. Validate the rules locally. This uploads nothing.

   ```bash
   straion source repo sync --dry-run
   ```

4. Open a pull request against `straion/rules/v1`.

After the merge, run `straion source repo sync` (or let your CI run it) to send the changes to Straion.
