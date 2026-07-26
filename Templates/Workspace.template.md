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

- [Shared or project-local tool, scope and version requirement]

## Approved setup execution

```yaml
setup_execution:
  executor: "ASSISTANT | GUIDED_STUDENT | STUDENT_REQUIRED"
  approved_global_changes: []
  approved_project_local_changes: []
  excluded_actions: []
  environment_registry: "[BOOTCAMP PATH]/07-ENVIRONMENT-REGISTRY.md"
```

The assistant verifies before installing and executes approved operational
setup. Use guided student execution only when configuration is a pending
learning objective or requires credentials, system confirmation or hardware.

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

## Implementation learning

```yaml
implementation_learning:
  mode: "STUDENT_AUTHORED"
  assistance_level: "QUESTION | HINT | API_GUIDANCE | PSEUDOCODE | INCOMPLETE_FRAGMENT | LOCAL_CORRECTION | REFERENCE_SOLUTION"
  student_decisions: []
  student_explanations: []
  student_authored_artifacts: []
  assistant_generated_solution_code: []
```

## Generated or local-only content

- `[PATH]` — `[TRACKED | IGNORED | LOCAL_ONLY]`

## Verification

- [ ] Approved tree was created without overwriting user work.
- [ ] Working path was reported.
- [ ] Existing compatible shared tools were reused.
- [ ] Global installations are strictly necessary and reusable.
- [ ] Reproducible dependencies remain project-local.
- [ ] Operating-system instructions match the active environment.
- [ ] Toolchain, dependencies and project references are resolved.
- [ ] Editor or IDE diagnostics applicable to the unit are working.
- [ ] Linter, build, tests or smoke check applicable to the unit passed.
- [ ] No implementation began before the readiness gate.
- [ ] Evaluated solution code remains student-authored.
- [ ] Assistance level and actual authorship were recorded.
