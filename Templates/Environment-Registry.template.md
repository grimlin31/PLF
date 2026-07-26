# [BOOTCAMP NAME] — Environment Registry

**Version:** 1.0.0
**Framework version:** 1.5.0
**Last verified:** `POR DEFINIR`

## Runtime

```yaml
runtime:
  operating_system: "POR DEFINIR"
  version: "POR DEFINIR"
  architecture_observed: "POR DEFINIR"
  status: "UNKNOWN | DECLARED | CONFIRMED"
```

## Shared tools

```yaml
tools:
  example:
    purpose: "POR DEFINIR"
    installation_scope: "SHARED | VERSION_MANAGED | PROJECT_LOCAL"
    status: "UNKNOWN | MISSING | INSTALLED | READY | INCOMPATIBLE | BLOCKED"
    version: null
    installation_path: null
    verified_on: null
    verified_by: "ASSISTANT | STUDENT | EXISTING_EVIDENCE"
    reusable: true
    recheck_when: []
    evidence: []
```

## Configuration learning

```yaml
configuration_learning:
  example:
    relevance: "CORE | USEFUL | OPERATIONAL_ONLY"
    status: "NOT_TAUGHT | GUIDED | DEMONSTRATED | MASTERED | NOT_REQUIRED"
    evidence: []
    last_practiced: null
```

## Rules

- Verify before installing.
- Reuse compatible shared tools.
- Keep reproducible dependencies project-local.
- Do not store secrets.
- Do not elevate learning status without evidence.
