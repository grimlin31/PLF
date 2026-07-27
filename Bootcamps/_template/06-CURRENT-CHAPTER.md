# Current Chapter Checkpoint

**Version:** 2.0.0
**Status:** `NOT_STARTED`  
**Bootcamp:** `POR DEFINIR`  
**Last updated:** `POR DEFINIR`

## Active unit

```yaml
checkpoint:
  unit_id: "POR DEFINIR"
  unit_type: "CHAPTER | LAB | PROJECT | INTERVIEW"
  title: "POR DEFINIR"
  partial_status: "NOT_STARTED | READY_TO_RESTART | IN_PROGRESS | BLOCKED | PAUSED | INVALID_METHOD | READY_TO_CLOSE"
  last_completed_point: "POR DEFINIR"
  current_point: "POR DEFINIR"
  pending_question: null
  next_action: "POR DEFINIR"
  completion_criteria_remaining: []
```

## Methodology

```yaml
methodology:
  protocol: "THEORY | PRACTICAL"
  documentation_mode: "DEFERRED_UNTIL_CLOSURE"
  current_phase: "ACTIVE_RECALL"
  current_concept: null
  pending_question: null

turn_contract:
  action: "ASK"
  phase: "ACTIVE_RECALL"
  question_allowed: true
  student_response_expected: true
  next_phase: "PANORAMA"
```

This file is normally consolidated at closure. `/sincronizar-capitulo`
explicitly authorizes a minimal continuity checkpoint.

## Active artifacts

```yaml
artifacts:
  notes: []
  exercises: []
  code: []
  evidence: []
```

## Workspace

```yaml
workspace:
  preparation_status: "NOT_REQUIRED | PROPOSED | APPROVED | READY | BLOCKED"
  primary_surface: "CHAT | EDITOR | IDE | TERMINAL | HARDWARE | MIXED"
  manifest: null
  relative_path: null
  absolute_path: null
  open_target: null
  environment_verification_required: false
  readiness_status: "NOT_ASSESSED | SETUP_REQUIRED | CONFIGURING | BLOCKED | READY_WITH_LIMITATIONS | READY"
  readiness_blockers: []
  accepted_limitations: []
  setup_executor: "ASSISTANT | GUIDED_STUDENT | STUDENT_REQUIRED"
  configuration_learning_status: "NOT_TAUGHT | GUIDED | DEMONSTRATED | MASTERED | NOT_REQUIRED"
  implementation_mode: "STUDENT_AUTHORED"
  assistance_level: "QUESTION | HINT | API_GUIDANCE | PSEUDOCODE | INCOMPLETE_FRAGMENT | LOCAL_CORRECTION | REFERENCE_SOLUTION"
```

## Dialogue

```yaml
dialogue:
  mode: "LEARNING | CONSULTATION"
  consultation_topic: null
  suspended_current_point: null
  suspended_pending_question: null
  resume_action: null
```

## Confirmed session time

```yaml
session_time:
  mentoring_minutes: 0
  self_study_minutes: 0
  practice_minutes: 0
  documentation_minutes: 0
  total_minutes: 0
```

Do not infer unreported time.

## Synchronization

```yaml
sync:
  source_device: null
  checkpoint_created_at: null
  remote_name: "origin"
  target_branch: "main"
  commit: null
  push_status: "NOT_SYNCED"
```

## Resume instruction

```text
Resume the active unit at [current_point].

Last completed:
[last_completed_point]

Pending question:
[NONE or exact question]

Next action:
[next_action]

Do not close the unit or advance the curriculum unless its closure criteria
are explicitly verified.
```

## Checkpoint history

| Date | Unit | Partial status | Commit | Next action |
|---|---|---|---|---|
| — | — | — | — | — |
