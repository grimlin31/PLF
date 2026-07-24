# [BOOTCAMP NAME]

**Bootcamp ID:** `[ID]`  
**Version:** 1.0.0  
**Status:** `NOT_STARTED`  
**Framework version:** 1.2.0  
**Target profession:** `[PROFESSION]`  
**Target level:** `[LEVEL]`

## Objective

[Define the primary professional objective.]

## Profiles

- Mentor: `[ROLE AND EXPERIENCE PARAMETER]`
- Student: `[CURRENT PROFILE]`

## Current state

See `05-BOOTCAMP-STATE.md`.

For the exact partial checkpoint, see `06-CURRENT-CHAPTER.md`.

## Curriculum

See `04-CURRICULUM-MAP.md`.

## Structure

```text
Chapters/   Theory chapters and associated laboratories
Projects/   Integrating professional projects
Interviews/ Role-specific preparation
Assets/     Bootcamp-specific diagrams and media
```

## Multi-device continuity

When this instance is stored in a private Bootcamp repository:

- `origin` points to the private repository;
- `upstream` points to the public PLF;
- `/sincronizar-capitulo` saves and publishes a partial checkpoint;
- `/reanudar-capitulo` obtains the latest checkpoint safely;
- `/estado-capitulo` reports progress without changing files.

See `Framework/10-MULTI-DEVICE-SYNC.md`.

## Starting a session

Provide:

1. `Framework/00-MASTER-CONTEXT.md`
2. this Bootcamp's `05-BOOTCAMP-STATE.md`
3. any additional files listed under `required_context`

Then request the unit indicated by `current_focus`.
