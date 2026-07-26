# [BOOTCAMP NAME]

## Project [X] — [TITLE]

**ID:** `PRJ-XX`  
**Version:** 1.2.0
**Status:** `PLANNED`  
**Type:** Integrating project  
**Estimated effort:** [MIN–MAX HOURS]

---

## 1. Professional context

[Describe the real-world setting and stakeholders.]

## 2. Objective

[Define the outcome and professional value.]

## 3. Scope

### Included

- [Item]

### Excluded

- [Item]

## 4. Requirements

### Functional

| ID | Requirement | Priority | Verification |
|---|---|---|---|
| `REQ-F-XXX` | [Requirement] | [Priority] | [Method] |

### Non-functional

| ID | Requirement | Metric | Verification |
|---|---|---|---|
| `REQ-NF-XXX` | [Requirement] | [Metric] | [Method] |

## 5. Constraints and assumptions

### Constraints

- [Constraint]

### Assumptions

- [Assumption]

## 6. Prerequisites

- [Unit or competency ID]

## 6.1 Workspace preparation

- Working surface: `[CHAT | EDITOR | IDE | TERMINAL | HARDWARE | MIXED]`
- Workspace manifest: `[PATH]/WORKSPACE.md`
- Project root to open: `[PATH]/workspace/`
- Environment verification required: `[YES | NO, with reason]`
- Environment readiness: `[NOT_ASSESSED | SETUP_REQUIRED | CONFIGURING | BLOCKED | READY_WITH_LIMITATIONS | READY]`

Before creating files, show the complete proposed tree, affected paths, setup
plan, installation scopes, student-required actions and exclusions. Wait for
explicit approval. The assistant then verifies existing tools and executes the
approved operational setup. Configuration is student-guided only when it is a
pending learning objective or requires user intervention.

## 7. Competencies integrated

| ID | Competency | Required level | Evidence |
|---|---|---|---|
| `CMP-XXX` | [Name] | [Level] | [Evidence] |

## 8. Architecture

### Context

```text
[CONTEXT DIAGRAM]
```

### Components

```text
[COMPONENT DIAGRAM]
```

### Data and control flows

[Description]

## 9. Design decisions

| ID | Decision | Alternatives | Trade-offs | Rationale |
|---|---|---|---|---|
| `ADR-XXX` | [Decision] | [Alternatives] | [Trade-offs] | [Reason] |

## 10. Milestones

| ID | Milestone | Deliverable | Exit criteria | Status |
|---|---|---|---|---|
| `PM-XXX` | [Milestone] | [Artifact] | [Criteria] | `PLANNED` |

## 11. Implementation plan

1. Elicit the student's design and expected behavior.
2. Review APIs and architectural choices interactively.
3. Have the student implement incremental milestones.
4. Validate each increment and give progressive hints rather than a solution.

### Assistance tracking

```yaml
implementation_learning:
  mode: "STUDENT_AUTHORED"
  assistance_level: "QUESTION"
  student_decisions: []
  student_explanations: []
  assistant_generated_solution_code: []
```

## 12. Test and validation strategy

### Test levels

- [Unit, integration, system or acceptance]

### Traceability

| Requirement | Test | Evidence |
|---|---|---|
| `REQ-XXX` | `TEST-XXX` | `EVD-XXX` |

## 13. Risks

| ID | Risk | Probability | Impact | Mitigation | Status |
|---|---|---|---|---|---|
| `RSK-XXX` | [Risk] | [Level] | [Level] | [Action] | `OPEN` |

## 14. Artifacts

- `[PATH]`

## 15. Results

[Record verified results.]

## 16. Technical review

### Architecture

[Review]

### Implementation

[Review]

### Reliability and maintainability

[Review]

## 17. Evidence

| ID | Artifact | Competencies | Status |
|---|---|---|---|
| `EVD-XXX` | [Artifact] | [IDs] | `PROPOSED` |

## 18. Professional presentation

### Problem

[Concise explanation]

### Contribution

[Student's actual contribution]

### Decisions

[Key decisions]

### Outcome

[Measured result]

### Limitations

[Honest limitations]

## 19. Retrospective

### What worked

- [Item]

### What did not work

- [Item]

### What would change

- [Item]

## 20. Completion criteria

- [ ] Mandatory requirements pass.
- [ ] Verification evidence exists.
- [ ] Architecture and decisions are documented.
- [ ] Risks and limitations are explicit.
- [ ] The student explains the project autonomously.
- [ ] Competency evidence is accepted.

## 21. Document history

### 1.2.0

- Added assistant-executed approved setup and student-authored implementation.

### 1.1.0

- Added approved workspace preparation and student-executed external setup.

### 1.0.0

- Initial project template instance.
