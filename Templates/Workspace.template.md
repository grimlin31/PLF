# [UNIT TITLE] — Workspace

**Unit:** `[UNIT ID]`
**Status:** `PROPOSED | APPROVED | CONFIGURING | READY_WITH_LIMITATIONS | READY | BLOCKED`
**Last verified:** `[DATE]`

## Working surface

```yaml
workspace:
  primary_surface: "CHAT | EDITOR | IDE | TERMINAL | HARDWARE | MIXED"
  editor_or_ide: "POR DEFINIR"
  relative_path: "POR DEFINIR"
  absolute_path: "POR DEFINIR"
  open_target: "POR DEFINIR"
```

## Runtime environment

```yaml
environment:
  operating_system: "POR DEFINIR"
  version: "POR DEFINIR"
  architecture_observed: "POR DEFINIR"
  verification_required: false
  verification_reason: null
```

## Approved tree

```text
[TREE]
```

## External prerequisites

- [Tool or framework installed by the student]

## Student-executed setup

Group independent actions into the largest safe block. Record purpose,
location, dependencies, expected and unacceptable results, evidence and the
condition that requires a response.

## Environment readiness

```yaml
readiness:
  status: "NOT_ASSESSED | SETUP_REQUIRED | CONFIGURING | BLOCKED | READY_WITH_LIMITATIONS | READY"
  required_checks: []
  completed_checks: []
  blockers: []
  limitations: []
  verified_versions: {}
  verified_at: null
  evidence_source: "STUDENT_REPORTED | EXISTING_VALID_EVIDENCE | NOT_VERIFIED"
```

## Setup blocks

| Block | Objective | Dependency | Status | Evidence or failure |
|---|---|---|---|---|
| `SETUP-01` | [Objective] | [NONE or block] | `PENDING` | [Evidence] |

## Generated or local-only content

- `[PATH]` — `[TRACKED | IGNORED | LOCAL_ONLY]`

## Verification

- [ ] Approved tree was created without overwriting user work.
- [ ] Working path was reported.
- [ ] External actions remain student-executed.
- [ ] Operating-system instructions match the active environment.
- [ ] Toolchain, dependencies and project references are resolved.
- [ ] Editor or IDE diagnostics applicable to the unit are working.
- [ ] Linter, build, tests or smoke check applicable to the unit passed.
- [ ] No implementation began before the readiness gate.
